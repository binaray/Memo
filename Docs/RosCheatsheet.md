## ROS2
### Building workspace
```
# catkin_make for ROS2
colcon build
# build specific package only
colcon build --packages-select my_package
```

### Creating new package with node in src
```
ros2 pkg create --build-type ament_cmake --node-name my_node my_package
```

### Adding dependencies
#### 1. package.xml
In package.xml, add a new line after the ament_cmake buildtool dependency and paste the following dependencies corresponding to your node’s include statements:
```
...
<buildtool_depend>ament_cmake</buildtool_depend>
# end of pre-existing lines

<depend>rclcpp</depend>
<depend>std_msgs</depend>
```
#### 2. CMakeLists.txt
In CMakeLists.txt, Below the existing dependency find_package(ament_cmake REQUIRED), add the lines:
```
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)
```
Then, add the executable and name it talker so you can run your node using ros2 run:
```
add_executable(talker src/publisher_member_function.cpp)
ament_target_dependencies(talker rclcpp std_msgs)
```
Finally, add the install(TARGETS...) section so ros2 run can find your executable:
```
install(TARGETS
  talker
  DESTINATION lib/${PROJECT_NAME})
```
The final CMakeLists.txt should look like this:
```
cmake_minimum_required(VERSION 3.5)
project(cpp_pubsub)

# Default to C++14
if(NOT CMAKE_CXX_STANDARD)
  set(CMAKE_CXX_STANDARD 14)
endif()

if(CMAKE_COMPILER_IS_GNUCXX OR CMAKE_CXX_COMPILER_ID MATCHES "Clang")
  add_compile_options(-Wall -Wextra -Wpedantic)
endif()

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)

add_executable(talker src/publisher_member_function.cpp)
ament_target_dependencies(talker rclcpp std_msgs)

install(TARGETS
  talker
  DESTINATION lib/${PROJECT_NAME})

ament_package()
```
