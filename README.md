## 汉阳（Hanyang）场景变化检测数据集
:smile: 链接：[Google Drive]() || [Baidu Yun]()

### 数据集描述
本数据集主要包括两张由IKONOS传感器获得的，大小为7200x6000的VHR影像。覆盖范围为中国武汉市汉阳区。影像分别获取于2002年2月和2009年6月，分辨率为1m，包含4个波段（蓝，绿，红和近红外波段）。

### 训练集产生方式
我们定义了8种场景类别，分别是：

```
1-parking            停车场    2-water             水体
3-sparse houses      稀疏房屋  4-dense houses      稠密房屋
5-residential region 居民区    6-idle region       空置地
7-vegetation region  农田      8-industrial region 工业区
0-undefined 未定义区域
```

通过选择典型区域来产生训练集。

### 测试集产生方式


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
│      hanyang2002.mat  ====> 汉阳区2002年的整体影像标签，大小为48x40的矩阵，每个矩阵元素代表对应patch的类别编号;  
│      hanyang2009      ====> 汉阳区2009年的整体影像，HDR格式;  
│      hanyang2009.hdr    
│      hanyang2009.mat  ====> 汉阳区2009年的整体影像标签，大小为48x40的矩阵，每个矩阵元素代表对应patch的类别编号;  
│  
└─train  
    ├─first  
    │      l1_n1_x2987_y3748.tif      ====> 汉阳区2002年的训练集图像，l表示类别编号，n表示编号;  
    │      l1_n2_x3141_y3753.tif  
    │      l1_n3_x3280_y3787.tif  
    │      ...  
    │  
    └─second  
            l1_n10_x3748_y5322.tif      ====> 汉阳区2009年的训练集图像，l表示类别编号，n表示编号;  
            l1_n11_x3825_y5166.tif  
            l1_n1_x3237_y3772.tif  
            ...  
```
### 引用

本数据集最先被如下文章用于场景变化检测:  
[1] Wu, Chen, Lefei Zhang, and Liangpei Zhang. "[A scene change detection framework for multi-temporal very high resolution remote sensing images](https://www.sciencedirect.com/science/article/pii/S0165168415003229)." Signal Processing 124 (2016): 184-197.  
[2] Wu, Chen, Liangpei Zhang, and Bo Du. "[Kernel slow feature analysis for scene change detection](https://ieeexplore.ieee.org/document/7817860)." IEEE Transactions on Geoscience and Remote Sensing 55.4 (2017): 2367-2384.  
如果您在研究中用到了本数据集, 请引用以上文章
