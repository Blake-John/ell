ROS 2 图像与 OpenCV 图像之间的转换方法，是机器人视觉开发中的核心技能。

# 00 核心概念

## 两种图像格式的本质区别

| 特性       | ROS 2 图像 (`sensor_msgs/Image`) | OpenCV 图像 (`numpy.ndarray`) |
| -------- | ------------------------------ | --------------------------- |
| **数据存储** | 一维字节数组 (`data`)                | 多维 NumPy 数组                 |
| **内存布局** | 行优先的连续字节流                      | 灵活的数组结构                     |
| **编码信息** | 通过 `encoding` 字段指定             | 通过数组 `dtype` 和 `shape` 隐含   |
| **用途**   | 网络传输、序列化                       | 算法处理、可视化                    |

## 关键编码对应关系

```
ROS 2 encoding    ↔    OpenCV 格式
─────────────────────────────────────────
"bgr8"           ↔    cv2.CV_8UC3 (BGR)
"rgb8"           ↔    cv2.CV_8UC3 (RGB)
"mono8"          ↔    cv2.CV_8UC1 (灰度)
"mono16"         ↔    cv2.CV_16UC1 (16位深度)
"bgra8"          ↔    cv2.CV_8UC4 (BGRA)
"rgba8"          ↔    cv2.CV_8UC4 (RGBA)
"32FC1"          ↔    cv2.CV_32FC1 (32位浮点深度图)
"16UC1"          ↔    cv2.CV_16UC1 (16位深度图)
```

---

# 01 使用 cv_bridge（推荐）

`cv_bridge` 是 ROS 官方提供的专用转换库，处理所有编码细节。

### 安装

```bash
# Ubuntu/Debian
sudo apt install ros-$ROS_DISTRO-cv-bridge

# 同时安装 OpenCV
sudo apt install libopencv-dev python3-opencv
```

### Python 实现

```python
#!/usr/bin/env python3
import rclpy
from rclpy.node import Node
from sensor_msgs.msg import Image
from cv_bridge import CvBridge
import cv2
import numpy as np

class ImageConverter(Node):
    def __init__(self):
        super().__init__('image_converter')
        
        # 核心：创建 CvBridge 实例（线程安全，可复用）
        self.bridge = CvBridge()
        
        # 订阅 ROS 图像
        self.subscription = self.create_subscription(
            Image,
            '/camera/image_raw',
            self.image_callback,
            10
        )
        
        # 发布转换后的图像
        self.publisher = self.create_publisher(Image, '/processed/image', 10)
        
    def image_callback(self, msg: Image):
        try:
            # ████████████████████████████████████████
            # ROS → OpenCV 转换（核心API）
            # ████████████████████████████████████████
            
            # 方式1：自动推断编码（推荐）
            cv_image = self.bridge.imgmsg_to_cv2(msg, desired_encoding='passthrough')
            
            # 方式2：强制指定目标编码（如需要特定格式）
            # cv_image = self.bridge.imgmsg_to_cv2(msg, desired_encoding='bgr8')
            # cv_image = self.bridge.imgmsg_to_cv2(msg, desired_encoding='mono8')
            
            # 此时 cv_image 是 numpy.ndarray
            self.get_logger().info(f"转换成功: shape={cv_image.shape}, dtype={cv_image.dtype}")
            
            # ═══════════════════════════════════════════════════
            # 在这里进行 OpenCV 处理
            # ═══════════════════════════════════════════════════
            processed = self.process_image(cv_image)
            
            # ████████████████████████████████████████
            # OpenCV → ROS 转换（核心API）
            # ████████████████████████████████████████
            
            # 方式1：自动推断编码
            out_msg = self.bridge.cv2_to_imgmsg(processed, encoding='passthrough')
            
            # 方式2：强制指定编码
            # out_msg = self.bridge.cv2_to_imgmsg(processed, encoding='bgr8')
            
            # 保留原始消息的元数据
            out_msg.header = msg.header
            
            self.publisher.publish(out_msg)
            
        except Exception as e:
            self.get_logger().error(f'转换失败: {str(e)}')
    
    def process_image(self, img: np.ndarray) -> np.ndarray:
        """示例处理：边缘检测"""
        gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) if len(img.shape) == 3 else img
        edges = cv2.Canny(gray, 100, 200)
        return cv2.cvtColor(edges, cv2.COLOR_GRAY2BGR)

def main(args=None):
    rclpy.init(args=args)
    node = ImageConverter()
    rclpy.spin(node)
    node.destroy_node()
    rclpy.shutdown()

if __name__ == '__main__':
    main()
```

### C++ 实现

```cpp
#include <rclcpp/rclcpp.hpp>
#include <sensor_msgs/msg/image.hpp>
#include <cv_bridge/cv_bridge.h>
#include <opencv2/opencv.hpp>

class ImageConverter : public rclcpp::Node {
public:
    ImageConverter() : Node("image_converter") {
        // CvBridge 不需要显式实例化，使用静态函数
        
        subscription_ = this->create_subscription<sensor_msgs::msg::Image>(
            "/camera/image_raw", 10,
            std::bind(&ImageConverter::imageCallback, this, std::placeholders::_1));
            
        publisher_ = this->create_publisher<sensor_msgs::msg::Image>("/processed/image", 10);
    }

private:
    void imageCallback(const sensor_msgs::msg::Image::SharedPtr msg) {
        try {
            // ████████████████████████████████████████
            // ROS → OpenCV 转换（C++版）
            // ████████████████████████████████████████
            
            // 使用 cv_bridge::toCvCopy 创建副本（修改不影响原消息）
            cv_bridge::CvImagePtr cv_ptr = cv_bridge::toCvCopy(msg, "bgr8");
            // 或 "passthrough" 保持原始编码
            
            // cv_ptr->image 是 cv::Mat
            cv::Mat& cv_image = cv_ptr->image;
            
            RCLCPP_INFO(this->get_logger(), "转换成功: %dx%d", 
                       cv_image.cols, cv_image.rows);
            
            // ═══════════════════════════════════════════════════
            // OpenCV 处理
            // ═══════════════════════════════════════════════════
            cv::Mat processed;
            cv::cvtColor(cv_image, processed, cv::COLOR_BGR2GRAY);
            cv::Canny(processed, processed, 100, 200);
            cv::cvtColor(processed, processed, cv::COLOR_GRAY2BGR);
            
            // ████████████████████████████████████████
            // OpenCV → ROS 转换
            // ████████████████████████████████████████
            
            // 方式1：从 CvImage 对象转换
            cv_bridge::CvImage out_msg;
            out_msg.header = msg->header;
            out_msg.encoding = "bgr8";
            out_msg.image = processed;
            publisher_->publish(*out_msg.toImageMsg());
            
            // 方式2：使用 cv_bridge::toImageMsg
            // auto out_msg = cv_ptr->toImageMsg();
            // publisher_->publish(*out_msg);
            
        } catch (cv_bridge::Exception& e) {
            RCLCPP_ERROR(this->get_logger(), "cv_bridge 异常: %s", e.what());
        }
    }
    
    rclcpp::Subscription<sensor_msgs::msg::Image>::SharedPtr subscription_;
    rclcpp::Publisher<sensor_msgs::msg::Image>::SharedPtr publisher_;
};

int main(int argc, char** argv) {
    rclcpp::init(argc, argv);
    rclcpp::spin(std::make_shared<ImageConverter>());
    rclcpp::shutdown();
    return 0;
}
```

---

# 02 手动转换（理解原理）

当你无法使用 cv_bridge 时，或者需要深度定制时，可以手动转换。

### Python 手动转换

```python
import numpy as np
from sensor_msgs.msg import Image

def manual_imgmsg_to_cv2(msg: Image) -> np.ndarray:
    """
    手动将 sensor_msgs/Image 转换为 OpenCV 格式
    """
    # 1. 解析编码确定 dtype 和 通道数
    encoding_to_dtype = {
        'bgr8': (np.uint8, 3),
        'rgb8': (np.uint8, 3),
        'mono8': (np.uint8, 1),
        'mono16': (np.uint16, 1),
        'bgra8': (np.uint8, 4),
        'rgba8': (np.uint8, 4),
        '32FC1': (np.float32, 1),
        '16UC1': (np.uint16, 1),
    }
    
    if msg.encoding not in encoding_to_dtype:
        raise ValueError(f"未知编码: {msg.encoding}")
    
    dtype, channels = encoding_to_dtype[msg.encoding]
    
    # 2. 将一维字节流转换为 numpy 数组
    # 注意：msg.data 是 bytes 对象，需要转换为 numpy
    img_array = np.frombuffer(msg.data, dtype=dtype)
    
    # 3. 重塑为图像维度 (height, width, channels)
    if channels == 1:
        img = img_array.reshape((msg.height, msg.width))
    else:
        img = img_array.reshape((msg.height, msg.width, channels))
    
    # 4. 处理步长（step）问题：如果图像有对齐填充
    # ROS 的 step 是每行的字节数
    expected_step = msg.width * channels * np.dtype(dtype).itemsize
    if msg.step != expected_step:
        # 存在填充字节，需要去除
        img = img[:, :msg.width]  # 裁剪掉填充部分
    
    return img

def manual_cv2_to_imgmsg(img: np.ndarray, encoding: str = None) -> Image:
    """
    手动将 OpenCV 图像转换为 sensor_msgs/Image
    """
    msg = Image()
    
    # 1. 推断编码
    if encoding is None:
        if img.dtype == np.uint8:
            if len(img.shape) == 2:
                encoding = 'mono8'
            elif img.shape[2] == 3:
                encoding = 'bgr8'  # 假设 BGR，OpenCV 默认
            elif img.shape[2] == 4:
                encoding = 'bgra8'
        elif img.dtype == np.uint16:
            encoding = 'mono16' if len(img.shape) == 2 else '16UC1'
        elif img.dtype == np.float32:
            encoding = '32FC1'
    
    msg.encoding = encoding
    msg.height = img.shape[0]
    msg.width = img.shape[1]
    
    # 2. 计算步长（考虑内存对齐）
    channels = 1 if len(img.shape) == 2 else img.shape[2]
    msg.step = img.shape[1] * channels * img.dtype.itemsize
    
    # 3. 确保数据连续并转换为一维
    if not img.flags['C_CONTIGUOUS']:
        img = np.ascontiguousarray(img)
    
    # 4. 转换为字节流
    msg.data = img.tobytes()
    
    return msg
```

### C++ 手动转换

```cpp
#include <sensor_msgs/msg/image.hpp>
#include <opencv2/opencv.hpp>
#include <vector>

cv::Mat manualImgMsgToCv2(const sensor_msgs::msg::Image::SharedPtr& msg) {
    // 确定 CV 类型
    int cv_type;
    if (msg->encoding == "bgr8") cv_type = CV_8UC3;
    else if (msg->encoding == "rgb8") cv_type = CV_8UC3;
    else if (msg->encoding == "mono8") cv_type = CV_8UC1;
    else if (msg->encoding == "mono16") cv_type = CV_16UC1;
    else if (msg->encoding == "bgra8") cv_type = CV_8UC4;
    else if (msg->encoding == "32FC1") cv_type = CV_32FC1;
    else throw std::runtime_error("未知编码");
    
    // 创建 cv::Mat（不复制数据，使用指针）
    cv::Mat img(msg->height, msg->width, cv_type, 
                const_cast<unsigned char*>(msg->data.data()), 
                msg->step);
    
    // 必须克隆，因为 msg->data 的生命周期由 ROS 管理
    return img.clone();
}

sensor_msgs::msg::Image::SharedPtr manualCv2ToImgMsg(const cv::Mat& img, 
    const std::string& encoding = "bgr8") {
    
    auto msg = std::make_shared<sensor_msgs::msg::Image>();
    
    msg->encoding = encoding;
    msg->height = img.rows;
    msg->width = img.cols;
    msg->step = img.step;  // OpenCV 的 step 已经是每行字节数
    
    // 复制数据
    size_t data_size = img.step * img.rows;
    msg->data.resize(data_size);
    memcpy(msg->data.data(), img.data, data_size);
    
    return msg;
}
```

---

## 关键细节与陷阱

### 1. 内存共享 vs 复制

```python
# ⚠️ 危险：共享内存（修改会影响原消息）
cv_image = self.bridge.imgmsg_to_cv2(msg, desired_encoding='passthrough')

# ✅ 安全：创建副本（独立内存）
cv_image = self.bridge.imgmsg_to_cv2(msg, desired_encoding='passthrough')
cv_image = cv_image.copy()  # 显式复制

# 或使用 toCvCopy（C++）自动创建副本
```

### 2. 编码转换的性能代价

```python
# 高性能：passthrough（无转换）
cv_image = self.bridge.imgmsg_to_cv2(msg, 'passthrough')

# 低性能：色彩空间转换（CPU 计算）
cv_image = self.bridge.imgmsg_to_cv2(msg, 'mono8')  # BGR→灰度，耗时
cv_image = self.bridge.imgmsg_to_cv2(msg, 'rgb8')   # BGR→RGB，耗时
```

### 3. 大端序/小端序问题（跨平台）

```python
# 如果 ROS 消息来自不同架构（如 ARM 机器人 ↔ x86 电脑）
# 注意 16bit/32bit 图像的字节序

import numpy as np

# 手动处理字节序
if msg.is_bigendian:
    img_array = np.frombuffer(msg.data, dtype=np.uint16)
    img_array = img_array.byteswap()  # 转换字节序
```

### 4. 压缩图像处理

```python
# 对于 sensor_msgs/CompressedImage
from sensor_msgs.msg import CompressedImage

def compressed_to_cv2(msg: CompressedImage) -> np.ndarray:
    # 直接解码，无需 cv_bridge
    np_arr = np.frombuffer(msg.data, np.uint8)
    cv_image = cv2.imdecode(np_arr, cv2.IMREAD_COLOR)
    return cv_image

def cv2_to_compressed(cv_image: np.ndarray, format: str = 'jpeg') -> CompressedImage:
    msg = CompressedImage()
    msg.format = format
    encode_param = [int(cv2.IMWRITE_JPEG_QUALITY), 90]
    success, encoded = cv2.imencode(f'.{format}', cv_image, encode_param)
    if not success:
        raise RuntimeError("编码失败")
    msg.data = encoded.tobytes()
    return msg
```

---

# 完整工具类封装

```python
#!/usr/bin/env python3
"""
ROS 2 ↔ OpenCV 图像转换工具类
"""

import cv2
import numpy as np
from cv_bridge import CvBridge
from sensor_msgs.msg import Image, CompressedImage
from typing import Union, Optional

class ROSImageConverter:
    _bridge = CvBridge()  # 单例模式
    
    @classmethod
    def to_cv2(cls, msg: Union[Image, CompressedImage], 
               encoding: str = 'passthrough') -> np.ndarray:
        """统一入口：自动处理压缩和非压缩图像"""
        if isinstance(msg, CompressedImage):
            return cls._compressed_to_cv2(msg)
        return cls._bridge.imgmsg_to_cv2(msg, encoding)
    
    @classmethod
    def from_cv2(cls, img: np.ndarray, 
                 encoding: str = 'passthrough',
                 header=None) -> Image:
        """OpenCV → ROS Image"""
        msg = cls._bridge.cv2_to_imgmsg(img, encoding)
        if header:
            msg.header = header
        return msg
    
    @classmethod
    def _compressed_to_cv2(cls, msg: CompressedImage) -> np.ndarray:
        """解码压缩图像"""
        np_arr = np.frombuffer(msg.data, np.uint8)
        flag = cv2.IMREAD_COLOR if 'png' in msg.format or 'jpg' in msg.format else cv2.IMREAD_UNCHANGED
        return cv2.imdecode(np_arr, flag)
    
    @staticmethod
    def get_image_info(msg: Image) -> dict:
        """获取图像元信息"""
        return {
            'width': msg.width,
            'height': msg.height,
            'encoding': msg.encoding,
            'step': msg.step,
            'is_bigendian': msg.is_bigendian,
            'data_size': len(msg.data)
        }
```

---

# 总结速查表

| 场景 | 推荐方法 | 代码片段 |
|------|----------|----------|
| 标准转换 | cv_bridge | `bridge.imgmsg_to_cv2(msg, 'passthrough')` |
| 需要特定格式 | cv_bridge + 编码 | `bridge.imgmsg_to_cv2(msg, 'mono8')` |
| 实时性能关键 | 零拷贝（谨慎） | `np.frombuffer` + 共享内存 |
| 压缩图像传输 | CompressedImage | `cv2.imdecode` / `cv2.imencode` |
| 自定义消息 | 手动转换 | 参考上方手动实现 |

**最佳实践**：
1. 始终使用 `passthrough` 除非确实需要格式转换
2. 在回调中尽早转换，避免持有 ROS 消息引用
3. 对 `CvBridge` 异常进行捕获处理
4. 发布时保留原始消息的 `header` 以保持时间戳同步