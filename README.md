# Nvidia-Nano-cuda9.0-cudnn7.0-tensorflow1.7-py2-
Because of some reasons, I must install the dev including the cuda9, cudnn7, tensorflow-1.7(py2) and opencv4<br>

Before do that, I found that if you install jetpack4.2 from SDK(not including other components such as computer vision), the nano just use about 16G in the SD card. I also found that if you install from the about 5G .img to install JP4.2 and will install cuda 10.0. I have no way to uninstall the cuda10 during that version.<br>

# STEP1<br>
In order to install the cuda9, you can download the L4T and change 16 to 32 in .common.conf file(you will found it)<br>


Then you will see the size of the SD card about 23G:<br>
![image](https://github.com/zhucheng725/Nvidia-Nano-cuda9.0-cudnn7.0-tensorflow1.7-py2-/blob/master/Screenshot%20from%202019-06-28%2010-55-07.png)<br>
 
# STEP2<br>
 follow the link:https://github.com/zhucheng725/Nvidia-Nano-Install-OpenCv4.0 to install the opencv4<br>
 ![image](https://github.com/zhucheng725/Nvidia-Nano-cuda9.0-cudnn7.0-tensorflow1.7-py2-/blob/master/Screenshot%20from%202019-06-28%2015-32-14.png)
 <br>
# STEP3<br>
## Download the cuda9.0:<br>
1. https://developer.download.nvidia.com/devzone/devcenter/mobile/jetpack_l4t/3.2.1/m8u2ki/JetPackL4T_321_b23/cuda-repo-l4t-9-0-local_9.0.252-1_arm64.deb <br>

## Download the cudnn7.0:<br>
1. https://developer.download.nvidia.cn/devzone/devcenter/mobile/jetpack_l4t/3.2.1/m8u2ki/JetPackL4T_321_b23/libcudnn7_7.0.5.15-1+cuda9.0_arm64.deb <br>
 
2. https://developer.download.nvidia.com/devzone/devcenter/mobile/jetpack_l4t/3.2.1/m8u2ki/JetPackL4T_321_b23/libcudnn7-dev_7.0.5.15-1+cuda9.0_arm64.deb <br>
 
3. https://developer.download.nvidia.com/devzone/devcenter/mobile/jetpack_l4t/3.2.1/m8u2ki/JetPackL4T_321_b23/libcudnn7-doc_7.0.5.15-1+cuda9.0_arm64.deb <br>

```
sudo dpkg -i cuda-repo-l4t-9-0-local_9.0.252-1_arm64.deb
sudo apt-key add /xxx/xxx(you terminal command can found it)
sudo apt-get update

sudo dpkg -i libcudnn7_7.0.5.15-1+cuda9.0_arm64.deb
sudo dpkg -i libcudnn7-dev_7.0.5.15-1+cuda9.0_arm64.deb
sudo dpkg -i libcudnn7-doc_7.0.5.15-1+cuda9.0_arm64.deb

sudo apt update
sudo apt install cuda-toolkit-9.0
```
This website maybe can help you :<br>
https://blog.csdn.net/m0_37718269/article/details/83901861<br>
![image](https://github.com/zhucheng725/Nvidia-Nano-cuda9.0-cudnn7.0-tensorflow1.7-py2-/blob/master/Screenshot%20from%202019-07-01%2014-29-57.png)
<br>

# STEP4<br>
## Download the tensorflow1.7 :<br>
1. https://nvidia.app.box.com/v/TF170-Py27-wTRT<br>
2. https://devtalk.nvidia.com/default/topic/1031300/jetson-tx2/tensorflow-1-8-wheel-with-jetpack-3-2-/<br>

```
pip2 install xxx.whl
```
![image](https://github.com/zhucheng725/Nvidia-Nano-cuda9.0-cudnn7.0-tensorflow1.7-py2-/blob/master/Screenshot%20from%202019-07-01%2014-29-17.png)


# STEP5<br>
## Install keras :<br>

```
sudo apt-get install libblas-dev liblapack-dev libatlas-base-dev gfortran 
sudo apt-get install libhdf5-serial-dev
sudo pip2 install keras
```

```
pip2 install serial
pip2 install pyserial
```
