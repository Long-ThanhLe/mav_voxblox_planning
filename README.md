
# Build
```bash
sudo apt-get install ros-melodic-cmake-modules python-wstool python-catkin-tools libyaml-cpp-dev protobuf-compiler autoconf
sudo apt-get install liblapacke-dev


mkdir -p ~/catkin_ws/src
cd ~/catkin_ws
catkin init
catkin config --extend /opt/ros/melodic
catkin config --cmake-args -DCMAKE_BUILD_TYPE=Release
catkin config --merge-devel


cd ~/catkin_ws/src/
git clone https://github.com/ethz-asl/mav_voxblox_planning.git
wstool init . ./mav_voxblox_planning/install/install_https.rosinstall
wstool update
git clone https://github.com/ethz-asl/protobuf_catkin.git
git clone https://github.com/ethz-asl/rotors_simulator.git
git clone https://github.com/ethz-asl/catkin_boost_python_buildtool.git
git clone https://github.com/ethz-asl/numpy_eigen.git
git clone https://github.com/ethz-asl/mav_control_rw.git
catkin build mav_voxblox_planning
```