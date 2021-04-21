# ROS and Pycharm - Step by step tutorial to link Pycharm with ROS  

## Ubuntu 

To install Ubuntu (desktop version), consult the following repository:  
https://github.com/DanielPalaio/Ubuntu_Setup  

## ROS

To install ROS, consult the following ROS.org page:  
http://wiki.ros.org/noetic/Installation/Ubuntu  

## Pycharm

**1.** In Ubuntu, search in the **Show Application** for **Ubuntu Software**  

**2.** Search for **Pycharm** and install it (**VSCode also recommended**)

**3.** To open Pycharm, type in the Ubuntu Terminal:  
> pycharm-community  

## ROS - Pycharm  

**1.** Go to the **Catkin Workspace src folder**. In the Ubuntu Terminal:  
> cd ~/catkin_ws/src  

**2.** Create a python virtual environment. In the Ubuntu Terminal:  
> sudo apt-get install virtualenv  
> virtualenv venv --system-site-packages

**3.** Activate the environment and install the project required packages. In the Ubuntu Terminal:  
> source venv/bin/activate  
> pip install -r requirements.txt  

**4.** Launch Pycharm. In the Ubuntu Terminal:  
> pycharm-community  

**5.** Open/Create a project and select the established python environment (step **2.**) as the project **Python Interpreter** following the steps below:  
> **File** -> **Settings** -> **Project** -> **Python Interpreter** -> **⚙️** -> **Add** -> **Virtualenv Environment** -> **Existing environment** -> **No interpreter ...** -> **~/catkin_ws/src/venv/bin/python**  

**6.** Define the **Content Roots** and **Source Folders** following the steps below:  
> **File** -> **Settings** -> **Project** -> **Python Interpreter**  
> Content Roots:  
>> /home/user/catkin_ws/src  
>> /home/user/catkin_ws/devel/lib/python/dist-packages  
>> /opt/ros/noetic/lib/python3/dist-packages  

> Under /home/user/catkin_ws/src:  
>> Excluded Folders: **venv** Package  
>> Source Folders: Package's **src** folders   

> Under /home/user/catkin_ws/devel/lib/python/dist-packages:  
>> Excluded Folders: Packages that don´t have any **msg** or **srv** files  
