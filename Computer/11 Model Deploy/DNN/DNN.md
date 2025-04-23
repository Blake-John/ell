OpenCV 提供了一个 `cv::dnn` 模块供我们使用，我们可以通过这个模块部署并推理模型。使用 `dnn` 模块部署模型主要分为以下几个步骤 : 

1. 加载模型
2. 设置输入并推理
3. 处理结果

# 1. 加载模型

`dnn` 模块提供了许多加载模型的方法，可以读取 `Pytorch` , `TorchScript` , `tensorflow` , `caffe` , `onnx` 等模型，并存储于 `cv::dnn::Net` 这个类中 : 

```C++
cv::dnn::Net network = cv::dnn::readNetFromONNX("model.onnx");
```

# 2. 设置输入并推理

除了模型的加载， OpenCV 还提供了便捷的方法可以将我们读入的拥有 `HWC` 结构 `cv::Mat` 图像转化成可以输入网络的具有 `batch x channel x row x col` 结构的张量，但仍然存储在 `cv::Mat` 类中。此外，还能在转换结构的同时交换 `B` 和 `R` 通道，使 `BGR` 通道的图片转换为正常的 `RGB` 通道 : 

```C++
// 获取输入数据
cv::Mat img = cv::imread("test.png");
cv::dnn::blobFromImage(img, img, 1 / 255.f, cv::Size(), cv::Scalar(), true);
// true 是用于交换 B R 通道的选项

// 设置 CUDA 支持
network.setPreferableBackend(cv::dnn::Backend::DNN_BACKEND_CUDA);

// 设置输入数据
network.setInput(img);

// 执行推理
cv::Mat output = network.forward();
```

> OpenCV 的 CUDA 支持见 [Installation](../../12%20OpenCV/Installation.md) 

# 3. 处理结果

结果存储在 `cv::Mat` 中，是个和输出相同结构的矩阵，我们可以通过操作该矩阵来处理结果，也可以通过获取指针的方法，将其转换成普通数组来处理结果 : 

```C++
std::cout << output << std::endl;
std::cout << std::max_element(output.begin(), output.end()) - output.begin() << std::endl;
```