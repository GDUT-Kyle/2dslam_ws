# 本项目可应用于机器狗实现2D激光导航

安装串口通讯库：

```sh
git clone git@github.com:GDUT-Kyle/2dslam_ws.git
cd ./2dslam_ws/env/env/CppLinuxSerial
mkdir build
cd build
cmake ..
make
sudo make install
```

编译：

```
catkin build
```

与机器狗通过USB线连接后，在`src/ros_gogodog_bridge/launch/dog_driver.launch`配置好USB端口号：

```xml
<param name="dog_device" value="/dev/pts/3" />
```

启动驱动程序：

```sh
roslaunch ros_gogodog_bridge dog_driver.launch
```

