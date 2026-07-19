# 使用功能包组织C++节点。

## 1.构建功能包

      ros2 pkg create --build-type ament_cmake --license Apache-2.0 demo_cpp_pkg


## 2.在demo_cpp_pkg/src新建文件cpp_node.cpp

![alt text](pic/442f3433cd47408a529a8dd4dd7c7602.png)

## 3.修改CMakeLists.txt

在/home/lenovo2/chapt2/demo_cpp_pkg/CMakeLists.txt中添加add--target的内容

![alt text](pic/6bda0154e89e3ab01531c53dd075374c.png)

简略版：

![alt text](pic/b9a4a81581d6ef4e8135544325da33a8.png)

## 4.新建build，建立可执行文件。

     cd demo_cpp_pkg

     mkdir build

     cd build

     cmake ../

     make

     ./cpp_node

     ctrl+C 退出

一行一行输

## 5.构建

![alt text](pic/d6f55ef32bc65fcf38e519d7afd7c11e.png)

![alt text](pic/a445d0b3ad3c967d78d19fbc365e69d0.png)

查看cpp_node依赖那些库以及有没有链接上

      ldd cpp_node 


## 6.ros2 run demo_cpp_pkg cpp_node运行

手动拷贝lib

![alt text](pic/96d1960eb377f279a39a6db776013713.png)

      source install/setup.bash

     colcon build

     ros2 run demo_cpp_pkg cpp_node


## 7.添加依赖声明。

chapt2/demo_cpp_pkg/package.xml中

![alt text](pic/86aa06a924cc39f0a25c152aefce9083.png)

     <depend>rclcpp</depend>

## 8.功能包分析。

![alt text](pic/64e78fc0c5082bd12c1b9495db8ea829.jpg)

