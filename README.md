# RMdemo

## 一、简要说明

RMdemo是RM上层代码（包括视觉处理）框架例程demo。机器人需要mini计算机提供计算辅助功能，或全自动运行功能，为了使开发者集中精神开发算法，特地设计了一个简单的开发框架RMdemo，为开发者提供开发便利，其中不包含具体算法。

### a.运行环境

* ubuntu 16.04
* opencv3.0及以上
* cmake3.5及以上

### b.实现功能

* 基本程序框架（基于状态机模型）
* 基本外设控制模块（串口通信模块，usb免驱ov2710摄像头模块）

### b.详细文档

* 框架说明文档：[框架文档](doc/framework_CN.md)

## 二、项目运行

### a.配置文件

根据自身情况，修改配置文件内容（res/main_config.yaml）

```yaml
%YAML:1.1
robot_id: 1
#1 define enemy is red......0 define enemy is blue.
enemy_is_red : 1
#dev path
serial_path: "/dev/xRMRobotSP" ##串口路径
capture_path : "/dev/xRMVideo" ##摄像头路径
```

### b.编译与运行

__新建编译目录__

```bash
mkdir build & cd build
```

__编译__

```bash
cmake ..
make 
```

__运行 __

```bash
./example
```


## 三、版权及许可证

uestc robomaster2018

* gezp email:1350824033@qq.com

RMdemo is provided under the [GPL-v3](COPYING).
