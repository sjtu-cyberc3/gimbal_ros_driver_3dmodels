# gimbal_ros_driver_3dmodels
随动云台的驱动程序和相关3D模型文件

## 使用驱动程序
驱动遵循PELCO-D协议，在ros noetic测试可用

编译：catkin_make

运行：
连接云台，更改串口的调用权限：sudo chmod 666 /dev/ttyUSB0（临时）

或者（永久更改权限）

查看串口信息：ls -l /dev/ttyUSB0
crw-rw---- 1 root dialout 4, 64 Jun  2 18:39 /dev/ttyUSB0

查看当前用户名：whoami

当前用户加入到dialout用户组：
sudo usermod -aG dialout username

最后重启系统

rosrun pelco_ws pelco_node
