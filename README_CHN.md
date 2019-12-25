## Multi-temporal Scene WuHan (MtS-WH) Dataset（[English](https://github.com/rulixiang/HanyangDataset/blob/master/README.md)）
:smile: 下载链接：[谷歌硬盘](https://drive.google.com/open?id=1gIW35zkRA-s0nA7mx8KHiXZDSln9Wxy0) || [小组网站](http://sigma.whu.edu.cn/resource.php).

## 数据集描述
Multi-temp Scene Wuhan(MtS-WH)数据集主要用于进行场景变化检测的方法理论研究与验证。场景变化检测就是在场景语义的层次上，对一定范围区域的土地利用属性变化情况进行检测和分析。
本数据集主要包括两张由IKONOS传感器获得的，大小为7200x6000的大尺寸高分辨率遥感影像。覆盖范围为中国武汉市汉阳区。影像分别获取于2002年2月和2009年6月，经过GS算法融合，分辨率为1m，包含4个波段（蓝，绿，红和近红外波段）。
整个数据集的训练样本和测试样本都是在大尺度高分辨率遥感影像中选取产生的。每个时相训练集包括190张影像，测试集包括1920张影像。训练集和测试集的场景图片共划分为以下几个类别：

```
1-parking            停车场    2-water             水体
3-sparse houses      稀疏房屋  4-dense houses      稠密房屋
5-residential region 居民区    6-idle region       空置地
7-vegetation region  农田      8-industrial region 工业区
0-undefined 未定义区域（不使用）
```

## 训练集产生方式

通过选择典型区域来产生训练集样本。训练集每个时相均包含190张图像，大小为150x150。但不同时相的训练样本并不对应相同位置。

## 测试集产生方式

对大尺寸影像通过大小为150x150互不重叠的网格划分产生测试集样本。每个时间可以获得1920（48x40）张场景图片，目视解译为以上几个类别。其中0-undefined是难以区分土地利用属性的场景块，不参与精度测试。

## 数据集目录描述

```
./hanyang_data  
│  hanyang2002.jpg  ====> 汉阳区2002年的整体影像伪彩色图;  
│  hanyang2009.jpg  ====> 汉阳区2009年的整体影像伪彩色图;  
│  README.md  
│  
├─test  
│      hanyang2002      ====> 汉阳区2002年的整体影像，HDR格式，可用ENVI等遥感软件查看;  
│      hanyang2002.hdr  
│      hanyang2002label.mat  ====> 汉阳区2002年的整体影像标签，MATLAB矩阵格式，大小为48*40的矩阵，每个矩阵元素代表对应位置场景图片的类别;  
│      hanyang2009      ====> 汉阳区2009年的整体影像，HDR格式，可用ENVI等遥感软件查看;  
│      hanyang2009.hdr    
│      hanyang2009label.mat  ====> 汉阳区2009年的整体影像标签，MATLAB矩阵格式，大小为48*40的矩阵，每个矩阵元素代表对应位置场景图片的类别;  
│  
└─train  
    ├─first  
    │      l1_n1_x2987_y3748.tif      ====> 汉阳区2002年的一个训练图像，l表示类别，n表示编号，x和y分别对应着整体影像内的坐标;  
    │      l1_n2_x3141_y3753.tif  
    │      l1_n3_x3280_y3787.tif  
    │      ...  
    │  
    └─second  
            l1_n10_x3748_y5322.tif      ====> 汉阳区2009年的一个训练图像，l表示类别，n表示编号，x和y分别对应着整体影像内的坐标;  
            l1_n11_x3825_y5166.tif  
            l1_n1_x3237_y3772.tif  
            ...  
```

## 引用

本数据集最先被如下文章用于场景变化检测:  
[1] Wu, Chen, Liangpei Zhang, and Bo Du. "Kernel slow feature analysis for scene change detection." IEEE Transactions on Geoscience and Remote Sensing 55.4 (2017): 2367-2384.   
[2] Wu, Chen, Lefei Zhang, and Liangpei Zhang. "A scene change detection framework for multi-temporal very high resolution remote sensing images." Signal Processing 124 (2016): 184-197.   
如果您在研究中用到了本数据集, 请引用以上文章

## 版权说明

本数据集的版权属于武汉大学地学智能感知与机器学习研究组[SIGMA](http://sigma.whu.edu.cn/)(Sensing Intelligence, Geoscience and MAchine learning lab)。MtS-WH数据集仅被授权应用于公开发表的科学研究和学术论文中。
如果您在研究中有其它问题，请联系武汉大学SIGMA小组。联系方式：chen.wu@whu.edu.cn
