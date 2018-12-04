# Face-Liveness_detection

## 下载数据集
 
下载地址：https://pan.baidu.com/s/1A3vQHUbuCjpv5zigfKKwhA  
200张人脸深度图.raw文件在face文件夹，200纸张攻击深度图.raw文件在non-face文件夹，人脸位置标注信息在同标题txt文件第一行

## 运行

Func_liveness_detection.c为函数形式，调用处理单一文件  

liveness_detection.c为批处理，修改文件夹路径后直接运行  
批量处理文件夹中所有.raw深度图文件，在命令行中输出结果，给定人脸活体检测结果  
输出结果如RESULT.txt所示  

RAW_PATH = '/home/zhoujie/liveness detection/raw文件/non-face/';  
![image](https://github.com/zj19941113/Face-Liveness_detection/blob/master/images/2018-10-19%2011-55-09%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png) 

RAW_PATH = '/home/zhoujie/liveness detection/raw文件/face/';  
![image](https://github.com/zj19941113/Face-Liveness_detection/blob/master/images/2018-10-19%2011-58-47%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE.png) 

## 补充

本算法检测类型范围：张照片攻击，视频攻击  
核心算法：RANSAC随机一致性采样  
Matlab版本：https://github.com/zj19941113/Deep-Img-Liveness-Detection  

## 深度图

![image](https://github.com/zj19941113/Deep-Img-Liveness-Detection/blob/master/Image/%E4%BA%BA%E8%84%B8%E6%B7%B1%E5%BA%A6%E5%9B%BE.jpg)  

# 近红外人脸定位与活体检测  
通过深度相机的红外图进行人脸位置定位，传给深度图进行活体检测  
## 运行  
Ubuntu下编译Dlib库参考这里 https://blog.csdn.net/ffcjjhv/article/details/84660869  
修改CMakeLists.txt相应路径  
`cmake .`  
`make`  
`./dlib_test`  

## 运行结果  
![image](https://github.com/zj19941113/Face-Liveness_detection/blob/master/images/result.png) 
