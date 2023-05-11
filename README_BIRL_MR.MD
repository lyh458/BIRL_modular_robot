## 压缩包说明： 
- ``BIRL_modular_robot-master.tar.gz``是基于原来的包的修改版，rviz的配置文件做了修改，建议使用我发给你的这个
- ``universal_robot.tar.gz``压缩包是UR机器人的ROS包。我在[UR官方ROS包](https://github.com/ros-industrial/universal_robot)中加了``ur_move_demo``package

## 相关API例程位于：``/universal_robot/ur_move_demo/src``文件夹中，其中：
- ``ur_move_demo.cpp``是UR机器人的moveit控制例程
- ``mr_move_demo.cpp``是UR机器人的moveit控制例程

## 使用方法
- 解压缩包，然后在你的workspace中``catkin_make``
- 使用UR API实例：
```
roslaunch ur5_moveit_config demo.launch
rosrun ur_move_demo ur_move_demo
```
- 使用模块 API实例：
```
roslaunch manipulator5d_moveit_config demo.launch 
rosrun ur_move_demo mr_move_demo
```
> 目前使用UR的API实例效果很完整（关节空间、笛卡尔空间的规划都可以出来），但是模块的笛卡尔空间还有点问题。