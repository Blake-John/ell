通过 Gazebo 模拟激光雷达传感器，并在 Rviz 中显示激光数据。

**实现流程:**

雷达仿真基本流程:

1. 已经创建完毕的机器人模型，编写一个单独的 xacro 文件，为机器人模型添加雷达配置；
2. 将此文件集成进xacro文件；
3. 启动 Gazebo，使用 Rviz 显示雷达信息。

# 01 Gazebo 仿真雷达

## 1.1 配置雷达传感器

```xml
<?xml version="1.0"?>
<robot xmlns:xacro="http://www.ros.org/wiki/xacro" name="lidar">
    <gazebo reference="rada">
        <sensor type="ray" name="rplidar">
            <pose>0 0 0 0 0 0</pose>
            <visualize>true</visualize>
            <update_rate>5</update_rate>
            <ray>
                <scan>
                    <horizontal>
                        <samples>360</samples>
                        <resolution>1</resolution>
                        <min_angle>-3</min_angle>
                        <max_angle>3</max_angle>
                    </horizontal>
                </scan>
                <range>
                    <min>0.10</min>
                    <max>30.0</max>
                    <resolution>0.01</resolution>
                </range>
                <noise>
                    <type>gaussian</type>
                    <mean>0.0</mean>
                    <stddev>0.01</stddev>
                </noise>
            </ray>
            <plugin name="gazebo_rplidar" filename="libgazebo_ros_laser.so">
                <topicName>scan</topicName>
                <frameName>lidar</frameName>
            </plugin>
        </sensor>
    </gazebo>
</robot>
```

> [!attention] 
> 其中， `<gazebo>` 节点的 `reference` 属性应该和我们前面设置的 `rada` link一致。
> 这是因为我们的雷达传感器不是一个独立的模块，而是依附于某一实体，简单来说我们需要有一个物体来贴上我们的雷达模块，因此，我们要保证 `reference` 和我们要贴的物体一致

## 1.2 模型集成

```xml
<!-- 组合小车底盘与传感器 -->
<robot name="my_car_camera" xmlns:xacro="http://wiki.ros.org/xacro">
    <xacro:include filename="inertial.xacro" />
    <xacro:include filename="car.xacro" />
    <xacro:include filename="camera.xacro" />
    <xacro:include filename="rada.xacro" />
    <xacro:include filename="move.xacro" />
    <!-- 雷达仿真的 xacro 文件 -->
    <xacro:include filename="lidar.xacro" />
</robot>
```

## 1.3 launch

```xml
<?xml version="1.0"?>
<launch>

    <param name="robot_description" command="$(find xacro)/xacro $(find lidar)/urdf/robot.xacro" />
    <include file="$(find gazebo_ros)/launch/empty_world.launch">
        <arg name="world_name" value="$(find lidar)/worlds/mw.sdf"/>
    </include>

    <node name="rviz" pkg="rviz" type="rviz"  output="screen" />
    <!-- <node name="rviz" pkg="rviz" type="rviz"  output="screen" args="-d $(find lidar)/config/rviz.rviz" /> -->
    <node name="joint_state_publisher" pkg="joint_state_publisher" type="joint_state_publisher" output="screen"/>
    <node name="robot_state_publisher" pkg="robot_state_publisher" type="robot_state_publisher" output="screen"/>
    
    <node name="model" pkg="gazebo_ros" type="spawn_model" output="screen" args="-urdf -model myrobot -param robot_description" />
    

</launch>
```

# 02 Rviz

添加 `LaserScan` 模块，并选择 `/scan` 话题，就可以看到雷达扫描的信息