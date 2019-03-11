## 汉阳（Hanyang）场景变化检测数据集 （[English](https://github.com/rulixiang/HanyangDataset/blob/master/README.md)）
:smile: 链接：[Google Drive]() || [Baidu Yun](https://pan.baidu.com/s/1mSAqD2GbOsgdjKqspydkTg). 提取码: 3t4i

### 数据集描述
本数据集主要包括两张由IKONOS传感器获得的，大小为7200*6000的大尺寸VHR影像。覆盖范围为中国武汉市汉阳区。影像分别获取于2002年2月和2009年6月，分辨率为1m，包含4个波段（蓝，绿，红和近红外波段）。每个时相训练集包括190张影像，测试集包括1920张影像。训练集和测试集的场景图片共划分为以下几个类别：

```
1-parking            停车场    2-water             水体
3-sparse houses      稀疏房屋  4-dense houses      稠密房屋
5-residential region 居民区    6-idle region       空置地
7-vegetation region  农田      8-industrial region 工业区
0-undefined 未定义区域（不使用）
```

### 训练集产生方式

通过选择典型区域来产生训练集样本。训练集每个时相均包含190张图像，大小为150x150。但不同时相的训练样本并不对应相同位置。

### 测试集产生方式

对大尺寸影像通过大小为150x150互不重叠的网格划分产生测试集样本。每个时间可以获得1920（48x40）张场景图片，目视解译为以上几个类别。

### 数据集目录描述

```
./hanyang_data  
│  hanyang2002.jpg  ====> 汉阳区2002年的整体影像伪彩色图;  
│  hanyang2009.jpg  ====> 汉阳区2009年的整体影像伪彩色图;  
│  README.md  
│  
├─test  
│      hanyang2002      ====> 汉阳区2002年的整体影像，HDR格式;  
│      hanyang2002.hdr  
│      hanyang2002label.mat  ====> 汉阳区2002年的整体影像标签，大小为48*40的矩阵，每个矩阵元素代表对应位置场景图片的类别;  
│      hanyang2009      ====> 汉阳区2009年的整体影像，HDR格式;  
│      hanyang2009.hdr    
│      hanyang2009label.mat  ====> 汉阳区2009年的整体影像标签，大小为48*40的矩阵，每个矩阵元素代表对应位置场景图片的类别;  
│  
└─train  
    ├─first  
    │      l1_n1_x2987_y3748.tif      ====> 汉阳区2002年的一个训练图像，l表示类别，n表示编号;  
    │      l1_n2_x3141_y3753.tif  
    │      l1_n3_x3280_y3787.tif  
    │      ...  
    │  
    └─second  
            l1_n10_x3748_y5322.tif      ====> 汉阳区2009年的一个训练图像，l表示类别，n表示编号;  
            l1_n11_x3825_y5166.tif  
            l1_n1_x3237_y3772.tif  
            ...  
```
### 引用

本数据集最先被如下文章用于场景变化检测:  
[1] Wu, Chen, Lefei Zhang, and Liangpei Zhang. "[A scene change detection framework for multi-temporal very high resolution remote sensing images](https://www.sciencedirect.com/science/article/pii/S0165168415003229)." Signal Processing 124 (2016): 184-197.  
[2] Wu, Chen, Liangpei Zhang, and Bo Du. "[Kernel slow feature analysis for scene change detection](https://ieeexplore.ieee.org/document/7817860)." IEEE Transactions on Geoscience and Remote Sensing 55.4 (2017): 2367-2384.  
如果您在研究中用到了本数据集, 请引用以上文章
