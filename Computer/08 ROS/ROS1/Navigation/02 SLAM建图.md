SLAM算法有多种，当前我们选用 `gmapping` ，后续会再介绍其他几种常用的SLAM实现。

# 01 `gmapping` 简介

`gmapping` 是ROS开源社区中较为常用且比较成熟的SLAM算法之一，`gmapping` 可以根据 **移动机器人里程计数据** 和 **激光雷达数据** 来绘制 **二维的栅格地图**，对应的，`gmapping` 对硬件也有一定的要求:

- 该移动机器人可以发布里程计消息
- 机器人需要发布雷达消息(该消息可以通过水平固定安装的雷达发布，或者也可以将深度相机消息转换成雷达消息)

# 02 `gmapping` 节点说明

`gmapping` 功能包中的 **核心节点** 是 : `slam_gmapping` 。为了方便调用，需要先了解该节点订阅的话题、发布的话题、服务以及相关参数。

## 2.1 Topic

### 2.1.1 Subscribe

- `tf (tf/tfMessage)` - 用于雷达、底盘与里程计之间的坐标变换消息。
- `scan(sensor_msgs/LaserScan)` - SLAM所需的雷达信息。

### 2.1.2 Publish

- `map_metadata(nav_msgs/MapMetaData)` - 地图元数据，包括地图的宽度、高度、分辨率等，该消息会固定更新。
- `map(nav_msgs/OccupancyGrid)` - 地图栅格数据，一般会在rviz中以图形化的方式显示。
- `~entropy(std_msgs/Float64)` - 机器人姿态分布熵估计(值越大，不确定性越大)。

## 2.2 Service

- `dynamic_map(nav_msgs/GetMap)` - 用于获取地图数据。

## 2.3 Parameter

- `~base_frame(string, default:"base_link")` - 机器人基坐标系。

- `~map_frame(string, default:"map")` - 地图坐标系。

- `~odom_frame(string, default:"odom")` - 里程计坐标系。

- `~map_update_interval(float, default: 5.0)` - 地图更新频率，根据指定的值设计更新间隔。

- `~maxUrange(float, default: 80.0)` - 激光探测的最大可用范围(超出此阈值，被截断)。

- `~maxRange(float)` - 激光探测的最大范围。

> 参数较多，上述是几个较为常用的参数，其他参数介绍可参考官网。

## 2.4 Frame Transformation

- `雷达坐标系→基坐标系` - 一般由 robot_state_publisher 或 static_transform_publisher 发布。

- `基坐标系→里程计坐标系` - 一般由里程计节点发布。

## 2.5 发布的坐标变换

- `地图坐标系→里程计坐标系` - 地图到里程计坐标系之间的变换。

# 03 using `gmapping` 

## 3.1 编写 `gmapping` 节点相关 `launch` 文件

launch文件编写可以参考 github 的演示 [launch文件](https://github.com/ros-perception/slam_gmapping/blob/melodic-devel/gmapping/launch/slam_gmapping_pr2.launch)

修改如下 : 

```xml
<launch>
<param name="use_sim_time" value="true"/>
    <node pkg="gmapping" type="slam_gmapping" name="slam_gmapping" output="screen">
      <remap from="scan" to="scan"/><!-- 雷达话题 -->
      <param name="base_frame" value="base_footprint"/><!--底盘坐标系-->
      <param name="odom_frame" value="odom"/> <!--里程计坐标系-->
      <param name="map_update_interval" value="5.0"/>
      <param name="maxUrange" value="16.0"/>
      <param name="sigma" value="0.05"/>
      <param name="kernelSize" value="1"/>
      <param name="lstep" value="0.05"/>
      <param name="astep" value="0.05"/>
      <param name="iterations" value="5"/>
      <param name="lsigma" value="0.075"/>
      <param name="ogain" value="3.0"/>
      <param name="lskip" value="0"/>
      <param name="srr" value="0.1"/>
      <param name="srt" value="0.2"/>
      <param name="str" value="0.1"/>
      <param name="stt" value="0.2"/>
      <param name="linearUpdate" value="1.0"/>
      <param name="angularUpdate" value="0.5"/>
      <param name="temporalUpdate" value="3.0"/>
      <param name="resampleThreshold" value="0.5"/>
      <param name="particles" value="30"/>
      <param name="xmin" value="-50.0"/>
      <param name="ymin" value="-50.0"/>
      <param name="xmax" value="50.0"/>
      <param name="ymax" value="50.0"/>
      <param name="delta" value="0.05"/>
      <param name="llsamplerange" value="0.01"/>
      <param name="llsamplestep" value="0.01"/>
      <param name="lasamplerange" value="0.005"/>
      <param name="lasamplestep" value="0.005"/>
    </node>

    <node pkg="joint_state_publisher" name="joint_state_publisher" type="joint_state_publisher" />
    <node pkg="robot_state_publisher" name="robot_state_publisher" type="robot_state_publisher" />

    <node pkg="rviz" type="rviz" name="rviz" />
    <!-- 可以保存 rviz 配置并后期直接使用-->
    <!--
    <node pkg="rviz" type="rviz" name="rviz" args="-d $(find my_nav_sum)/rviz/gmapping.rviz"/>
    -->
</launch>
```

## 3.2 执行

1. 先启动 Gazebo 仿真环境(此过程略)
2. 然后再启动地图绘制的 launch 文件
3. 启动键盘键盘控制节点，用于控制机器人运动建图 - `rosrun teleop_twist_keyboard teleop_twist_keyboard.py`
4. 在 rviz 中添加组件，显示栅格地图

最后，就可以通过键盘控制gazebo中的机器人运动，同时，在rviz中可以显示gmapping发布的栅格地图数据了，下一步，还需要将地图单独保存。

![](imgs/gmapping.png)

