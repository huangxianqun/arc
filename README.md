# arc
Code for Amazon Robot Challenge <br>

## Platform
Ubuntu 14.04 STL + ROS indigo + UR5 + Moveit <br>

## Install

```
1. git clone https://github.com/qqfly/arc.git
2. rosdep install --from-paths . --ignore-src --rosdistro indigo (前两步在src里运行)
3. catkin_make（在工作空间内编译，例如catkin_ws）
```

## 使用步骤
### 仿真
```
1. roslaunch ur5_moveit_config demo.launch
2. rosrun moveit_ur5_interface planning
3. 参照moveit_ur5_interface/planning/src/planning.cpp写自己的代码，控制机器人
```
### 真实机器人
```
1. 网线连接UR5，设置电脑IP(192.168.11.104)
2. 初始化UR5，默认IP（192.168.11.102），如果IP变了，请修改ur_modern_driver里的ur5_bringup_joint_limited.launch
3. roslaunch ur_modern_driver ur5_bringup_joint_limited.launch
4. roslaunch ur5_moveit_config demo_actual.launch
5. 之后就可以自己写代码控制了。
```
## 其他
有需要改进的地方可以直接提交一个PR，如果代码未实现，可以先提交观点到tips.txt <br>

## 最后
我要测试下github放图片功能 <br>
![logo](https://raw.githubusercontent.com/qqfly/hello-world/master/pic/qrcode_for_gh_e4a5e3dc2cde_258.jpg "我的公众号")
