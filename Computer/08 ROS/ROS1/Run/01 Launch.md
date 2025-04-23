> 一个程序中可能需要启动多个节点，比如:ROS 内置的小乌龟案例，如果要控制乌龟运动，要启动多个窗口，分别启动 roscore、乌龟界面节点、键盘控制节点。如果每次都调用 rosrun 逐一启动，显然效率低下，如何优化?

采用的优化策略便是使用roslaunch 命令集合 launch 文件启动管理节点，并且在后续教程中，也多次使用到了 launch 文件。

launch 文件是一个 XML 格式的文件，可以启动本地和远程的多个节点，还可以在参数服务器中设置参数。

在包下添加 `launch/` 目录，并新建 `run.launch` 文件 : 

```launch
<launch>
    <node pkg="turtlesim" type="turtlesim_node" name="myTurtle" output="screen" />
    <node pkg="turtlesim" type="turtle_teleop_key" name="myTurtleContro" output="screen" />
</launch>
```

然后在命令行中调用 : 

```bash
roslaunch <package_name> <launch_file>
```

