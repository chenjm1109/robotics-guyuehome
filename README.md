# 小明工坊-古月居 代码仓库

存放一些实验代码，用于配套在古月居发表的文章

## 文件说明

### s_arm：ROS实验 | PID控制在做什么

编译与启动

```shell
cd ~/catkin_ws
catkin_make
roslaunch s_arm s_arm_gazebo.launch
```

发布关节位置

```shell
rostopic pub /s_arm/joint1_position_controller/command std_msgs/Float64 "data: -1.5707"
```



### ROS-Behavior-Tree：ROS实验 | 行为树实现机器人智能

编译与启动

```shell
cd ~/catkin_ws
catkin_make
roslaunch behavior_tree_leaves guard_robot_behavior_tree.launch
```

一共弹出了两个界面，一个界面展示了行为树的结构，另一个界面为仿真界面。**使启动终端处于激活状态**，用键盘的方向键控制己方小乌龟靠近和远离敌方小乌龟