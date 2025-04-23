# 01 sensor_msgs/Image to OpenCV

使用 `cv_bridge` 进行转换，可以将 `sensor_msgs/msg::Image` 或是 `ImageCompressed` 转化为 `cv::Mat` 的格式，也可以将 `cv::Mat` 的格式转化为 ROS 的格式

# 02 python 多文件程序 #problem #solved 

在 ros2 中，我们需要规定 python 源文件的程序入口才能被识别并编译，然而，如果我们想要多文件编写代码，使用没有程序入口的文件，这个时候在编译/运行的时候就会报错 **找不到要导入的文件** 。

这个时候，我们只需要在要导入的包前 **加上当前 ros 包名** 即可。例如有如下文件结构 : 

```

```

这个是 `zhipu_vision` 包， 其中 `img_sub.py` 中导入了 `zhipuapi.py` ，而 `zhipuapi.py` 则导入了 `utils.py` 。这个时候，我们应该在代码中这样写 :

```Python
# img_sub.py
import zhipu_vision.zhipuapi as zhipuapi
```

```Python
# zhipuapi.py
import zhipu_vision.utils as utils
```

只有规定了包名，我们才能正常通过 `colcon` 编译使用。