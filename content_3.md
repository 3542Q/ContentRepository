<div style="text-align:center;font-weight:bold;font-size:2em"> opencv-python基本操作 </div>

<div style="text-align:center;">2024-11-26</div>

<!-- TOC -->
- [内容简介](#内容简介)
- [如何安装](#如何安装)
- [图像基本操作](#图像基本操作)
- [读入图片](#读入图片)
<!-- /TOC -->

# 内容简介<a name="内容简介"></a>
OpenCV（open source computer vision library）是一个基于BSD许可（开源）发行的跨平台计算机视觉库，可以运行在Linux、Windows、Android和Mac OS操作系统上。
它轻量级而且高效——由一系列 C 函数和少量 C++ 类构成，同时提供了Python、Ruby、MATLAB等语言的接口，实现了图像处理和计算机视觉方面的很多通用算法。
OpenCV用C++语言编写，它的主要接口也是C++语言，但是依然保留了大量的C语言接口。
在计算机视觉项目的开发中，OpenCV作为较大众的开源库，拥有了丰富的常用图像处理函数库，采用C/C++语言编写，可以运行在Linux/Windows/Mac等操作系统上，能够快速的实现一些图像处理和识别的任务。

# 如何安装<a name="如何安装"></a>

```
pip install opencv-python
```

# 图像基本操作<a name="图像基本操作"></a>

# 读入图片<a name="读入图片"></a>

```python
import cv2 #opencv读取的格式是BGR
import matplotlib.pyplot as plt
import numpy as np 
%matplotlib inline 
img=cv2.imread('image.jpg')
cv2.imshow("img",img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<img src="https://s2.loli.net/2024/11/27/6g1snCuLHFlix9J.png"/>

```
> img.shape
(414, 500, 3)
```
图片是一个矩阵, 每个像素点对应矩阵里的一个值，对于彩色图片，每个像素点都有3个通道，在此处是BGR，简单理解就是一个彩色图片由三个矩阵构成。

上面的img.shape就说明是414x500大小的彩色图片

---
**封面图片**: [https://s2.loli.net/2024/11/27/q3leSAbaBOLIn1K.png]

**标签**: [计算机视觉 , opencv , 学习 , python]

**分类**: [文章]
