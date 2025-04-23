TensorRT 是 nvidia 专门用于模型推理加速的库。他通过 **设计独立的GPU算子来提高GPU的并行计算能力** ， **优化模型结构** 来加速模型的推理。

# 1. Installation

## 1.1 Ubuntu

安装 TensorRT 需要先安装 **显卡驱动** ， **Cuda Toolkit** ， **Cudnn (Optional)** 。可以通过 [script](https://gitee/blake-john/env-config) 中 ubuntu 的安装脚本来一键安装，也可以跟着官方的说明一步步安装。

### 1.1.1 Driver

Ubuntu-22.04 在官方包中提供了显卡驱动的安装包，可以通过 `apt` 直接下载，也可以在 **附加驱动** 中选择并安装推荐的显卡驱动。在下载之前，我们先查看系统推荐的显卡驱动 : 

```bash
ubuntu-drivers devices
```

输出结果为 :

```text
== /sys/devices/pci0000:00/0000:00:01.0/0000:01:00.0 ==
modalias : pci:v000010DEd000028A0sv00001558sd000025A1bc03sc00i00
vendor   : NVIDIA Corporation
driver   : nvidia-driver-550-open - third-party non-free
driver   : nvidia-driver-545-open - distro non-free
driver   : nvidia-driver-535-server-open - distro non-free
driver   : nvidia-driver-545 - distro non-free
driver   : nvidia-driver-535 - distro non-free
driver   : nvidia-driver-535-server - distro non-free
driver   : nvidia-driver-535-open - distro non-free
driver   : nvidia-driver-550 - distro non-free recommended
driver   : xserver-xorg-video-nouveau - distro free builtin
```

我们选择带有 `recommended` 字样的驱动进行安装 : 

```bash
sudo apt install nvidia-driver-550
```

安装并重启系统后，我们可以通过输入 `nvidia-smi` 命令来查看显卡驱动是否正常工作，并且能通过这里查看自己 `CUDA` 的版本 : 

```text
Fri Sep 20 03:27:47 2024       
+-----------------------------------------------------------------------------------------+
| NVIDIA-SMI 550.107.02             Driver Version: 550.107.02     CUDA Version: 12.4     |
|-----------------------------------------+------------------------+----------------------+
| GPU  Name                 Persistence-M | Bus-Id          Disp.A | Volatile Uncorr. ECC |
| Fan  Temp   Perf          Pwr:Usage/Cap |           Memory-Usage | GPU-Util  Compute M. |
|                                         |                        |               MIG M. |
|=========================================+========================+======================|
|   0  NVIDIA GeForce RTX 4060 ...    Off |   00000000:01:00.0 Off |                  N/A |
| N/A   42C    P8              2W /   85W |     109MiB /   8188MiB |      0%      Default |
|                                         |                        |                  N/A |
+-----------------------------------------+------------------------+----------------------+
                                                                                         
+-----------------------------------------------------------------------------------------+
| Processes:                                                                              |
|  GPU   GI   CI        PID   Type   Process name                              GPU Memory |
|        ID   ID                                                               Usage      |
|=========================================================================================|
|    0   N/A  N/A      1983      G   /usr/lib/xorg/Xorg                              4MiB |
|    0   N/A  N/A      2270    C+G   ...libexec/gnome-remote-desktop-daemon         94MiB |
+-----------------------------------------------------------------------------------------+
```

### 1.1.2 Cuda Toolkit

我们到 [官网](https://developer.download.nvidia.com) 查找 **对应驱动版本，对应CUDA版本的** 本地安装包 (.deb) 进行下载，例如，在 550 版本的驱动以及 12.4 版本的CUDA下，我所选择的是 [这个包](https://developer.download.nvidia.com/compute/cuda/12.4.1/local_installers/cuda-repo-ubuntu2204-12-4-local_12.4.1-550.54.15-1_amd64.deb) 进行下载，然后，我们就可以按照以下指令安装 : 

```bash
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2204/x86_64/cuda-ubuntu2204.pinsudo
mv cuda-ubuntu2204.pin /etc/apt/preferences.d/cuda-repository-pin-600

# 若没有下载安装包这可以通过下面的命令下载
# wget https://developer.download.nvidia.com/compute/cuda/12.4.1/local_installers/cuda-repo-ubuntu2204-12-4-local_12.4.1-550.54.15-1_amd64.deb

sudo dpkg -i cuda-repo-ubuntu2204-12-4-local_12.4.1-550.54.15-1_amd64.deb
sudo cp /var/cuda-repo-ubuntu2204-12-4-local/cuda-*-keyring.gpg /usr/share/keyrings/
sudo apt update
sudo apt install -y cuda-toolkit
```

安装完成后，我们需要将 CUDA 的路径加入到 `PATH` 和 `LD_LIBRARY_PATH` 中 : 

```bash
echo "export PATH=/usr/local/cuda-12.4/bin/:$PATH" >> ~/.bashrc
echo "export LD_LIBRARY_PATH=/usr/local/cuda-12.4/lib64/:$LD_LIBRARY_PATH" >> ~/.bashrc
```

### 1.1.3 Cudnn

Cudnn 的安装我们也采用本地安装，在官网找到对应版本的Cudnn安装包并下载，我使用的是 [这个版本的包](https://developer.download.nvidia.com/compute/cudnn/9.4.0/local_installers/cudnn-local-repo-ubuntu2204-9.4.0_1.0-1_amd64.deb) ，然后按照以下命令进行安装 : 

```bash
# 如果没有下载安装包则可以通过以下命令下载安装包
# wget https://developer.download.nvidia.com/compute/cudnn/9.4.0/local_installers/cudnn-local-repo-ubuntu2204-9.4.0_1.0-1_amd64.deb

sudo dpkg -i cudnn-local-repo-ubuntu2204-9.4.0_1.0-1_amd64.deb
sudo cp /var/cudnn-local-repo-ubuntu2204-9.4.0/cudnn-*-keyring.gpg /usr/share/keyrings/
sudo apt update
sudo apt install -y cudnn
```

### 1.1.4 TensorRT

我们依旧通过本地安装的方式安装TensorRT，不过这一次我们必须在官网下载安装包，而不能通过 `wget` 来获取，因为需要进行登陆验证 : 

```bash
sudo dpkg -i nv-tensorrt-local-repo-ubuntu2204-10.4.0-cuda-12.6_1.0-1_amd64.deb
sudo cp /var/nv-tensorrt-local-repo-ubuntu2204-10.4.0-cuda-12.6/*-keyring.gpg /usr/share/keyrings/
sudo apt update
sudo apt install tensorrt
```

## 1.2 Arch

Arch 可以通过 `pacman/yay` 一键安装 **所有我们需要的** : 

```bash
sudo pacman -S nvidia cuda cudnn
yay -S tensorrt
```

在安装 `nvidia` , `cuda` , `cudnn` 的过程中，我们大概率不会遇到问题，但是在安装 `tensorrt` 的时候，我们大概率会编译不成功，这是由于 Arch 中的 `gcc` 包太新了， `tensorrt` 暂时不支持，因此我们可以直接在官网下载。

我们通过 [下载](https://developer.nvidia.com/tensorrt/download/10x) `tar` 文件来安装 `tensorrt` 。

我下载的是 `TensorRT-10.7.0.23` `x86_64` 版本的，然后将其解压缩到我们想要安装的位置，再将其库目录加入路径当中 : 

```bash
sudo tar -xzvf TensorRT-10.7.0.23.Linux.x86_64-gnu.cuda-12.6.tar.gz -C /opt
echo "export LD_LIBRARY_PATH=/opt/TensorRT-10.7.0.23/lib:$LD_LIBRARY_PATH" >> ~/.bashrc
echo "export LIBRARY_PATH=/opt/TensorRT-10.7.0.23/lib:$LIBRARY_PATH" >> ~/.bashrc
echo "export PATH=/opt/TensorRT-10.7.0.23/bin:$PATH" >> ~/.bashrc
```

# 2. CMake

我们仍然选择使用 CMake 来管理我们的项目 : 

## 2.1 对于 Ubuntu

由于 Ubuntu 通过系统自动安装文件，其库文件及头文件均在系统路径中，因此我们只需要直接链接我们需要的库就可以了。

> [!attention] Attention
> `TensorRT` 依赖于 `CUDA` ，因此我们必须将 `CUDA` 的库和头文件路径链接到目标上

```CMake
cmake_minimum_required(VERSION 3.10)
project(RTTEST)

find_package(CUDA REQUIRED) # tensorrt 依赖于 cuda
# find_library(nvinfer nvonnxparser)
# tensorrt 没有专门的 CMake Package 来管理，但是却能通过 find_library 找到任何一个库文件
# nvinfer 用于环境部署以及推理
# nvonnxparser 用于加载 onnx 模型
# 但是我们不需要查找，直接链接即可

add_executable(main main.cpp)

target_include_directories(main PUBLIC ${CUDA_INCLUDE_DIRS})

target_link_libraries(main ${CUDA_LIBRARIES})
target_link_libraries(main nvinfer nvonnxparser)
```

## 2.2 对于 Arch

我们通过压缩包自定义安装位置，因此需要自己在 `CMake` 中设定 `TensorRT` 的位置 : 

```CMake
cmake_minimum_required(VERSION 3.10)
project(TRT_DEPLOY)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(TensorRT_INCLUDE_DIRS /opt/TensorRT-10.7.0.23/include)

find_package(CUDA REQUIRED)
find_package(OpenCV REQUIRED)

add_library(trtlib trt.cpp)

target_include_directories(trtlib PUBLIC include)

target_include_directories(trtlib PUBLIC ${CUDA_INCLUDE_DIRS})
target_link_libraries(trtlib ${CUDA_LIBRARIES})

target_link_libraries(trtlib nvinfer nvonnxparser)
target_include_directories(trtlib PUBLIC ${TensorRT_INCLUDE_DIRS})

target_include_directories(trtlib PUBLIC ${OpenCV_INCLUDE_DIRS})
target_link_libraries(trtlib ${OpenCV_LIBRARIES})

add_executable(main main.cpp)
target_link_libraries(main trtlib)
```

# 3. Deploy

TensorRT 用于部署的库在 `NvInfer.h` 中，拥有 `nvinfer1` 的命名空间，读取 onnx 模型的库在 `NvOnnxParser.h` 中，拥有 `onnxparser` 的命名空间 : 

```C++
#include <NvInfer.h>
#include <NvOnnxParser.h>

// using namespace nvinfer1;
// using namespace nvonnxparser;
```

通过 TensorRT 部署模型主要分为以下几个步骤 : 

1. 加载并构建，优化模型
2. 创建推理环境
3. 设置输入数据并推理
4. 处理结果

## 3.1 加载模型

TensorRT 通过 `nvinfer1::IBuilder` 来构建，配置整个模型，包括 : 

1. 创建一个空网络 `nvinfer1::INetworkDefinition` 用于存储网络的数据
2. 创建模型的配置文件 `nvinfer1::IBuilderConfig` 用于优化并设置模型的参数
3. 创建一个序列化模型 `nvinfer1::IHostMemory` 整合模型的设置参数和网络的数据

我们通过 `nvonnxparser::IParser` 来读取 onnx 模型并写入 `nvinfer1::INetworkDefinition` 中 

此外，我们还需要自己继承 `nvinfer1::ILogger` 类来实现一个 logger 用于日志文件的输出 : 

```C++
class Logger : public nvinfer1::ILogger
{
	public :
		void log(Severity severity, const char* msg) noexcept override
		{
			if (severity <= Severity::kWARNING)
			{
				std::cout << msg << std::endl;
			}
		}
} logger;
```

```C++
// 创建用于构建模型的 builder
nvinfer1::IBuilder* builder = nvinfer1::createInferBuilder(logger);

// 创建一个用于存储模型数据的空网络
nvinfer1::INetworkDefinition* network = builder->createNetworkV2(0);

// 创建一个 parser 用于读取 onnx 模型并解析
nvonnxparser::IParser* parser = nvonnxparser::createParser(*network, logger);
parser->parseFromFile(
	"model.onnx", static_cast<int32_t>(nvinfer1：：ILogger::Severity::kWARNING)
);
for (int32_t i = 0; i < parser->getNbErrors(); i++)
{
	std::cerr << parser->getError(i)->desc() << std::endl;
}

// 创建配置文件
nvinfer1::IBuilderConfig* config = builder->createBuilderConfig();

// 设置内存池的大小限制
config->setMemoryPoolLimit(nvinfer1::MemoryPoolType::kWORKSPACE, 1 << 30);

// 优化模型
if (builder->platformHasFastFp16())
{
	config->seFlag(nvinfer1::BuilderFlag::kFP16);
}

// 将网络数据和配置整合成一个序列化模型
nvinfer1::IHostMemory* serializedModel = builder->buildSerializedNetwork(
	*network, *config
);
```

## 3.2 创建推理环境

要创建推理环境，我们需要创建一个用于 TensorRT 的 runtime `nvinfer1::IRuntime` ，并且在这个之下将序列化模型解析成 TensorRT 所用的 engine `nvinfer1::ICudaEngine` 模型，最后我们还需要创建一个用于执行推理的上下文 context `nvinfer1::IExecutionContext` : 

```C++
// 创建 runtime
nvinfer1::IRuntime* runtime = nvinfer1::createInferRuntime(logger);

// 加载 engine 模型
nvinfer1::ICudaEngine* engine = runtime->deserializeCudaEngine(
	serializedModel->data(), serializedModel->size()
);

// 创建 context
nvinfer::IExecutionContext* context = engine->createExecutionContext();
```

## 3.3 设置输入数据并推理

我们需要手动在 GPU 上分配空间并载入数据，最后从GPU上读取推理结果 : 

```C++
// 读取图片
cv::Mat img = cv::imread("test.png");
img.convertTo(img, CV_32FC3);
cv::dnn::blobFromImage(img, img, 1 / 255.f, cv::Size(), cv::Scalar(), true);

int input_size = img.cols * img.rows * img.channels * sizeof(float);
int n_output = 6;
int output_size = n_output * sizeof(float);

// 设置输入输出数据
void* input = img.ptr(0);
std::vector<float> output(n_output);

void* GPU_input_ptr;
void* GPU_output_ptr;

// 在 GPU 上分配空间
cudaMalloc(&GPU_input_ptr, input_size);
cudaMalloc(&GPU_output_ptr, output_size);

// 在 GPU 上载入数据
cudaMemcpy(GPU_input_ptr, input, input_size, cudaMemcpyHostToDevice);
// cudaMemcpyHostToDevice 是从 host (cpu) 到 device (gpu)

// 设置用于推理的输入输出的结构
void* buffers[2] = {GPU_input_ptr, GPU_output_ptr};

// 执行推理
context->executeV2(buffers);
```

## 3.4 处理结果

我们需要手动将数据从 GPU 上复制回 CPU 才能进行处理 : 

```C++
cudaMemcpy(output.data(), GPU_output_ptr, output_size, cudaMemcpyDeviceToHost);
for (int i = 0; i < n_output; i++)
{
	std::cout << output[i] << " ";
}
std::cout << std::endl;
std::cout << "Prediction : " << std::max_element(output.begin(), output.end()) - output.begin() << std::endl;
```

## 3.5 释放内存

> [!attention] 
> 我们需要手动将我们占用的空间 **释放**，否则容易出现 **内存泄漏的现象**!!!

```C++
cudaFree(GPU_input_ptr)
cudaFree(GPU_output_ptr)

delete network;
delete config;
delete parser;
delete serializedModel;
delete builder;

delete context;
delete engine;
delete runtime;
```
