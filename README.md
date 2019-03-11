## Hanyang Dataset for Scene Change Detection ([中文](https://github.com/rulixiang/HanyangDataset/edit/master/README_CHN.md))
:smile: Avaliable: [Google Drive]() || [Baidu Yun](https://pan.baidu.com/s/1mSAqD2GbOsgdjKqspydkTg). Password: 3t4i
### Description of the Hanyang dataset
This dataset consists of two large-size VHR images, which have a size of 7200x600 and are respectively acquired by IKONOS sensors in Feb, 2002 and Jun, 2009. The images cover the the Hanyang District, Wuhan City, China and contain 4 spectral bands (R, G, B and Near-Infrared). The spatial resolution of the images is 1m. For each large-size image, we generated 190 scene images as training set and 1920 images as testing set. These images are labeled as following classes:
```
1-parking              2-water             
3-sparse houses        4-dense houses      
5-residential region   6-idle region       
7-vegetation region    8-industrial region 
0-undefined (Not Used)
```

### Generation of Training Set
We generate training samples by clipping images from typical regions. Training set of each time includes 190 scene images with size of 150x150. It's noticed that training samples of different time do not correspond to the same position.

### Generation of Testing Set
We obtained the scenes from the large image by a non-over lapping grid with a cell size of 150x150. In this way, we generated 1920 (48x40) test scenes for each time point. Then they are categorized to the above classes by visual interpretation.

### Description of the content

```
./hanyang_data  
│  hanyang2002.jpg  ====> An overall pseudo-color image of Hanyang in 2002.  
│  hanyang2009.jpg  ====> An overall pseudo-color image of Hanyang in 2009.  
│  README.md  
│  
├─test  
│      hanyang2002      ====> Raw imagery of Hanyang in 2002, formatted in HDR. 
│      hanyang2002.hdr  
│      hanyang2002label.mat  ====> The labels of images in testing set of Hanyang in 2002, represented by a matrix with size of 48x40. Each element denote the Scene Class Number of an image of corresponding position.  
│      hanyang2009      ====> Raw imagery of Hanyang in 2009, formatted in HDR.  
│      hanyang2009.hdr    
│      hanyang2009label.mat  ====> The labels of images in testing set of Hanyang in 2009, represented by a matrix with size of 48x40. Each element denote the Scene Class Number of an image of corresponding position. 
│  
└─train  
    ├─first  
    │      l1_n1_x2987_y3748.tif      ====> A sample image of training set in 2002, where l denotes the Class Number, and n denotes the Number. 
    │      l1_n2_x3141_y3753.tif  
    │      l1_n3_x3280_y3787.tif  
    │      ...  
    │  
    └─second  
            l1_n10_x3748_y5322.tif      ====> A sample image of training set in 2009, where l denotes the Class Number, and n denotes the Number. 
            l1_n11_x3825_y5166.tif  
            l1_n1_x3237_y3772.tif  
            ...  
```
## Citation
This dataset was firstly used in the following work about scene change detection:  
[1] Wu, Chen, Lefei Zhang, and Liangpei Zhang. "[A scene change detection framework for multi-temporal very high resolution remote sensing images](https://www.sciencedirect.com/science/article/pii/S0165168415003229)." Signal Processing 124 (2016): 184-197.  
[2] Wu, Chen, Liangpei Zhang, and Bo Du. "[Kernel slow feature analysis for scene change detection](https://ieeexplore.ieee.org/document/7817860)." IEEE Transactions on Geoscience and Remote Sensing 55.4 (2017): 2367-2384.  
Please cite the abovementioned articles should you used this dataset in your research.
