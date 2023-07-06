# ros2使用手册



## 一、benginner 

创建工作空间

~~~
mkdir -r workspace/src && cd workspace/src
~~~
创建功能包
~~~
ros2 pkg create package_name --build-type ament_cmake --dependencies rclcpp
~~~
补全依赖

~~~
rosdep install -i --from-path src --rosdistro humble -y
~~~

编译

~~~
cd .. && colcon build
~~~

## 二、ros2 cli

### 2.1 ros2

~~~
Commands:
  action     Various action related sub-commands
  bag        Various rosbag related sub-commands
  component  Various component related sub-commands
  daemon     Various daemon related sub-commands
  doctor     Check ROS setup and other potential issues
  interface  Show information about ROS interfaces
  launch     Run a launch file
  lifecycle  Various lifecycle related sub-commands
  multicast  Various multicast related sub-commands
  node       Various node related sub-commands
  param      Various param related sub-commands
  pkg        Various package related sub-commands
  run        Run a package specific executable
  security   Various security related sub-commands
  service    Various service related sub-commands
  topic      Various topic related sub-commands
  wtf        Use `wtf` as alias to `doctor`
~~~



### 2.2  colcon 

下载colcon

~~~
sudo apt install python3-colcon-common-extensions
~~~

使用colcon

~~~
 colcon build后边还可以跟一些常用的参数：  

--packages-up-to ：编译指定的功能包，而不是整个工作空间
--symlink-install ：节省每次重建python脚本的时间
--event-handlers console_direct+ ：在终端中显示编译过程中的详细日志
~~~





