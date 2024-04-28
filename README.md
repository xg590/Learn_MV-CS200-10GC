### MV-CS200-10GC is an industrial Area Scan Camera
* 线阵相机 vs 面阵相机：线阵相机进行线性拍照、适用于扫描条形码或加装机械导轨逐行扫描；面阵相机与传统相机功能接近。
#### Prerequisite
* [MV-CS200-10GC](https://www.hikrobotics.com/en/machinevision/productdetail?id=5794): a (20MP Area Scan Camera/GigE/IMX183/Color/Basic) camera
* [MVL-KF5028M-12MPE](https://www.hikrobotics.com/en/machinevision/productdetail?id=5743)：a (50mm/F2.4/1.2"/25MP Lens/C-Mount) lens
* Ubuntu 2204: x86-64 
#### 海康提供什么/What can we get from HIKROBOT
* Product Support Webpage: [CHN](https://www.hikrobotics.com/cn/machinevision/service/download?module=0) / [ENG](https://www.hikrobotics.com/en/machinevision/service/download?module=0)
* Machine Vision Studio客户端MVS (SDK Runtime Library included)：[MVS_STD_GML_V2.1.2_231011.zip](https://www.hikrobotics.com/cn2/source/support/software/MVS_STD_GML_V2.1.2_231011.zip)
* SDK Runtime组件包（uncessary if studio is installed）：[MvCamCtrlSDK_STD_V4.1.2_231011.zip](https://www.hikrobotics.com/cn2/source/support/software/MvCamCtrlSDK_STD_V4.1.2_231011.zip) 
#### For Beginer (Use the studio software)
1. Unzip MVS_STD_GML_V2.1.2_231011.zip and get a bunch of .deb
2. Install MVS-2.1.2_x86_64_20231011.deb 
3. Some environmental varibles
   ```shell
   cat << EOF >> ~/.bashrc
   export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/opt/MVS/bin
   export PATH=$PATH:/opt/MVS/bin
   EOF
   source ~/.bashrc
   ```
4. Run the studio software
   ```shell
   MVS # Start the GUI of Machine Vision Studio
   ```
#### For Python Programmer
* The Dev Guide can be found in `/opt/MVS/doc/Machine Vision Camera SDK (C)_Developer Guide_V4.1.0_EN/Machine Vision Camera SDK Developer Guide_Linux_(C) V4.1.0.html`
* Python Sample Code can be found in `/opt/MVS/Samples/64/Python`
* An example of setting camera parameters and getting image can be found in this [notebook](MV-CS200-10GC.ipynb) [Warning: The code is not for MV-CS200-10GM which is a monochrome camera]