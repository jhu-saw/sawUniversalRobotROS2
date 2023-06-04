# sawUniversalRobotROS2

ROS 2 node for sawUniversalRobot (https://github.com/jhu-saw/sawUniversalRobot).

Ubuntu 20.04 packages required:
```sh
sudo apt install libxml2-dev swig sox espeak cmake-curses-gui cmake-qt-gui git subversion gfortran libcppunit-dev libqt5xmlpatterns5-dev
```

You can use the ROS 2 VCS python-based tool (`sudo apt install
python3-vcstool`) to download all the cisst, sawUniversalRobot and ROS
2 specific packages needed for the sawUniversalRobot ROS 2 node.  Look
for the `.repos` file in this repository and find the link to the raw
content.  Then in your ROS 2 workspace, under the `src` directory,
use:
```sh
vcs import --input https://raw.githubusercontent.com/jhu-saw/sawUniversalRobotROS2/master/ur.repos
```
Then go back to the root of your ROS 2 workspace and build using:
```sh
colcon build
```

Once the code is compiled, you can start the ROS 2 Universal Robot using:
```
ros2 run universal_robot universal_robot -i <robot_ip>
```
