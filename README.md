# Gardener
## Gardener for agricultural!!!

The main repository of [SUSTech-Gardener](https://github.com/SUSTech-Gardener), which is An autonomous mobile agricultural robot can collect agriculture-related information, as well as weeding and other work to serve the future agriculture. 
<iframe width="560" height="315" src="https://www.youtube.com/embed/GjDMmWxaL50" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

![image-20210606134722046](https://raw.githubusercontent.com/zhuhu00/img/master/20210606134730.png)

![image-20210606134850746](https://raw.githubusercontent.com/zhuhu00/img/master/20210606134854.png)

![image-20210606134529791](https://raw.githubusercontent.com/zhuhu00/img/master/20210606134534.png)

The whole project has these parts. 

## Sensors
1. Camera: Realsense D435i
2. Lidar: Livox avia
3. Soilsensor

## [硬件部分](https://github.com/SUSTech-Gardener/3d-solidworks)
1. 履带车
2. 喷头控制
3. 车辆架子
4. 云台
5. 土壤传感器伸缩机构
6. 电机部分
7. 电路

# Build and Run

## 1. Prerequisties

### 1.1 Ubuntu and ROS

Ubuntu 64-bit 16.04 or 18.04. ROS Kinetic or Melodic. Follow [ROS Installation](http://wiki.ros.org/ROS/Installation).
### 1.2 Deep Learning requirements

In this part, Using YOLO V3 to detect weed and crop. The learning model we also transfer to ROS package, it is very easy to use.

- ROS package:  https://github.com/SUSTech-Gardener/WeedDetection_ros
- Without ROS: https://github.com/SUSTech-Gardener/WeedDetection

### 1.3 SLAM and other

- [x] (Livox 的SLAM的部分)[https://github.com/SUSTech-Gardener/car_relocalization]

## 2. Build Gardener

### 2.1 3d_solidworks in Gardener

The whole 3d solidworks model is in the [repository](https://github.com/SUSTech-Gardener/3d-solidworks), contains these items:

- A some tracked car
- Some extended structure on the car
- Base for Livox lidar and RealSense camera D435i.
- The head of the sprinkler

### 2.2 Sensors

- Livox lidar: for SLAM and navigation.
- D435i: [detect weed and crop](https://github.com/SUSTech-Gardener/WeedDetection). 
- Soil moisture sensor: add the soil moisture data in map(In **soilsensor** fold).

## 3. Run with hardware

# TODO 
- [x] 硬件部分：小车的速度，转向控制，
- [x] 杂草识别的模型，第八周结束需要搞完
- [x] SLAM和navigation
- [x] 机械硬件结构搭建和喷头系统的构建
- [x] 土壤检测器的插入设计
- [x] 最终的系统框架构建！！

# Acknowledgment

