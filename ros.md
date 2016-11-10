#Ubuntu-14.04 安装ROS
##安装源列表
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'</br>
##设置密钥</br>
 sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 0xB01FA116</br>
##安装</br>
sudo apt-get update</br>
选择Desktop-Full Install</br>
sudo apt-get install ros-jade-desktop-full</br>
apt-cache search ros-jade</br>
##初始化
sudo rosdep init
rosdep update
##配置环境
echo "source /opt/ros/jade/setup.bash" >> ~/.bashrc
source ~/.bashrc
source /opt/ros/jade/setup.bash
##安装rosinstall
sudo apt-get install python-rosinstall
##获得包的源代码
$ apt-get source ros-jade-laser-pipeline