# XTDrone_yolov8ros_tool

## 项目简介
对XTDrone目标检测模块设计由darknet升级支持至Ultralytics，目前已测试YOLOv8使用。完成仿真环境下目标检测与无人机跟踪控制。因时间问题并未对模型结构进行调整，后续工作可以基于此项目开展。
（觉得有用可以点个star，qq了）

## 使用说明
本项目是基于XTDrone的目标检测与跟踪模块做出的修改，原有使用方案可参考[XTDrone语雀-目标检测与跟踪](https://www.yuque.com/xtdrone/manual_cn/target_detection_tracking)。
运行时使用
```
roslaunch yolov8_ros yolov8_launch.launch
```
替代原有的darknet模块。

同时修改xtdrone的controller的yolo_human_tracking.py代码为本项目中的文件

项目在outdoor1.launch和修改的test.world世界上进行了测试。
## XTDrone
XTDrone是基于PX4、ROS与Gazebo的无人机通用仿真平台。支持多旋翼飞行器（包含四轴和六轴）、固定翼飞行器、复合翼飞行器（包含quadplane，tailsitter和tiltrotor）与其他无人系统（如无人车、无人船与机械臂）。在XTDrone上验证过的算法，可以方便地部署到真实无人机上。https://github.com/robin-shaun/XTDrone