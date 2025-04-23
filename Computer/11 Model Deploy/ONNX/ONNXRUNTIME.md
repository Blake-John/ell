**ONNXRuntime** 是一个用于部署网络并进行推理的环境，可以在 **多种设备**，**多种语言** 下进行部署。我们将在 Linux_x64 C++ 环境下部署导出的模型。

# 1. Installation

安装 ONNXRuntime 有两种方式，一种是通过克隆官方仓库并编译后安装，但这种方式较慢，而且并不方便，我们采用官方提供的 **预编译库** 来安装。

```bash
wget "https://github.com/microsoft/onnxruntime/releases/download/1.19.2/onnxruntime-linux-x64-1.19.2.tgz" # 获取压缩包
tar -xf onnxruntime-linux-x64-1.19.2.tgz # 解压缩

# 复制头文件
sudo cp -r onnxruntime-linux-x64-1.19.2/include /usr/local/include/onnxruntime
# 复制库文件
sudo cp -r onnxruntime-linux-x64-1.19.2/lib /usr/local/lib64
```

接下来，将安装文件夹加入 **系统库路径 `LD_LIBRARY_PATH`** : 

```bash
echo "export LD_LIBRARY_PATH=/usr/local/lib64/:$LD_LIBRARY_PATH" >> ~/.bashrc
```

安装就到此为止。

# 2. CMake

我们使用 CMake 来管理项目，并通过 CMake 来找 onnxruntime 的库 : 

```CMake
cmake_minimum_required(VERSION 3.10)
project(ONNXTEST)

set(CMAKE_PREFIX_PATH /usr/local/lib64/cmake/onnxruntime) # 设置 CMake 路径

find_package(onnxruntime REQUIRED) # 查找 onnxruntime 包

add_executable(main main.cpp)

target_link_libraries(main onnxruntime) # 链接 onnxruntime 库
```

> 记得要将 `/usr/local/lib64/cmake/onnxruntime` 设置为 prefix，因为 `/usr/local/lib64` 不在 `CMAKE_MODULE_PATH` 中

# 3. Deploy

onnxruntime 的接口主要存放在 `onnxruntime_cxx_api.h` 头文件中，并且使用 `Ort` 作为命名空间，我们可以先将头文件包括进来 : 

```C++
#include <onnxruntime/onnxruntime_cxx_api.h>
// using namespace Ort;
```

部署并推理onnx模型主要分为以下几个步骤 : 

1. 设置推理环境，用于部署onnx
2. 加载并设置onnx模型，获取模型信息
3. 加载输入数据并推理
4. 处理结果

## 3.1 设置推理环境

我们需要先创建一个用于推理的环境，并设置 **日志等级** ，同时也需要创建一个 MemoryInfo 来设置内存的读取规则 : 

```C++
Ort::Env env (OrtLoggingLevel::ORT_LOGGING_LEVEL_WARNING, "ONNXINFER");
Ort::MemoryInfo memInfo = Ort::MemoryInfo::CreateCpu(
	OrtAllocatorType::OrtArenaAllocator, OrtMemType::OrtMemTypeDefault
)
```

其中， `OrtAllocatorType` 和 `OrtMemType` 分别是用于设置内存分配的 enum 类型 : 

- `OrtAllocatorType` 
	- `OrtInvalidAllocator` 
	- `OrtDeviceAllocator` - 用于在特殊设备上 GPU 分配内存
	- `OrtArenaAllocator` - 自动分配
- `OrtMemType` 
	-  `OrtMemTypeCPUInput` - Any CPU memory used by non-CPU execution provider
	- `OrtMemTypeCPUOutput` - CPU accessible memory outputted by non-CPU execution provider, i.e. CUDA_PINNED
	-  `OrtMemTypeCPU = OrtMemTypeCPUOutput` - Temporary CPU accessible memory allocated by non-CPU execution provider, i.e. CUDA_PINNED
	- `OrtMemTypeDefault` - The default allocator for execution provider

## 3.2 加载并设置模型

我们通过创建一个 `Ort::SessionOptions` 和 `Ort::Session` 来加载并配置onnx模型 : 

```C++
Ort::SessionOptions session_opt;
session_opt.SetGraphOptimizationLevel(GraphOptimizationLevel::ORT_ENABLE_ALL);
// GraphOptimizationLevel 用于设置图像的优化等级

Ort::Session session (env, "model.onnx", session_opt);
```

然后，我们需要设置/获取一些模型数据用于推理，包括 `input/output_shape` , `input/output_names` :

```C++
// 设置 input/output_shape
std::vector<int64_t> input_shape = \
session.GetInputTypeInfo(0).GetTensorTypeAndShapeInfo().GetShape();
std::vector<int64_t> output_shape = \
session.GetOutputTypeInfo(0).GetTensorTypeAndShapeInfo().GetShape();
```

其中，`GetInputTypeInfo(0)` 中的 `0` 是 input 的 index ，不同的网络有不同的输入个数，可以通过 `session.GetInputCount()` 来查看该模型有多少个输入，输出也同理。这里只有一个输入和一个输出，故 index 为 0

```C++
// 设置 input/output_names
std::vector<const char*> input_names = {"input"};
std::vector<const char*> output_names = {"output"};
```

这是导出onnx模型时设置的输入和输出的名称，必须要同导出时设置的相同。这里的模型只有一个输入和一个输出，故容器中也只有一个名称。

如果不知道输入和输出的名称，可以通过以下代码来查看 : 

```C++
Ort::AllocatorWithDefaultOptions allocator;
std::cout << session->GetInputNameAllocated(0, allocator).get() << std::endl;
std::cout << session->GetOutputNameAllocated(0, allocator).get() << std::endl;
```

## 3.3 加载输入数据并推理

输入数据的类型为 `Ort::Value` ，可以通过 `Ort::Value::CreateTensor()` 来创建 : 

```C++
// 获取数据
cv::Mat img = cv::imread("test.png");
img.convertTo(img, CV_32FC3); // 输入数据要求为 float 类型
cv::dnn::blobFromImage(
	img, img, 1 / 255.f, cv::Size(), cv::Scalar(), true
);

float* input = img.ptr(0);
int input_size = img.rows * img.cols * img.channels

// 处理数据
Ort::Value input_tensor = Ort::Value::CreateTensor<float>(
	memInfo, input, input_length, input_shape.data(), input_shape.size()
);

int n_output = 6;
std::vector<float*> output(n_output)

Ort::Value output_tensor = Ort::Value::CreateTensor<float>(
	memInfo, output.data(), output.size(), output_shape.data(), output_shape.size()
);

// 进行推理
session.Run(
	Ort::RunOptions(), input_names.data(), &input_tensor, 1, output_names.data(), &output_tensor, 1
)
```

## 3.4 处理结果

我们需要处理输出的结果 `output_tensor` 。如果在前面有通过 `Ort::Value::CreateTensor()` 将 `output` 与 `output_tensor` 联系在一起，那么我们可以直接读取 `output` 来获得输出数据，否则就需要通过操作 `output_tensor` 来获取数据 : 

```C++
for (int i = 0; i < n_output; i++)
{
	std::cout << output[i] << " ";
	// 可以通过自定义一个 softmax 函数来计算概率，不过并不是必要的
}
std::cout << std::endl;
std::cout << "Prediction : " << std::max_element(output.begin(), output.end()) - output.begin() << std::endl;
```
