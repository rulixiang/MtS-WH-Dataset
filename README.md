## Multi-temporal Scene WuHan (MtS-WH) Dataset([中文](https://github.com/rulixiang/HanyangDataset/blob/master/README_CHN.md))
Avaliable: [Google Drive](https://drive.google.com/open?id=1gIW35zkRA-s0nA7mx8KHiXZDSln9Wxy0) || [Our Group Website](http://sigma.whu.edu.cn/resource.php).
### Description of the dataset
The Wuhan multi-temperature scene (MtS-WH) data set is mainly used for theoretical research and verification of scene change detection methods. Scene change detection is  detecting and analyzing the changes of land-use in a certain area at the scene semantic level.  
This dataset consists of two large-size VHR images, which have a size of 7200x6000 and are respectively acquired by IKONOS sensors in Feb, 2002 and Jun, 2009. The images cover the Hanyang District, Wuhan City, China and contain 4 spectral bands (Blue, Green, Red and Near-Infrared). The spatial resolution of the images is 1m after fusion by the Gram–Schmidt algorithm.  
For each large-size image, we generated 190 scene images as training set and 1920 images as testing set. These images are labeled as following classes:
```
1-parking              2-water             
3-sparse houses        4-dense houses      
5-residential region   6-idle region       
7-vegetation region    8-industrial region 
0-undefined (Not Used)
```
0-undefined represents scene images that are difficult to distinguish the land-use classes and don't participate in the accuracy evaluation.
### Generation of Training Set
We generate training samples by cropping images from typical regions. Training set of each time includes 190 scene images with size of 150x150. It's noticed that training samples of different time do not correspond to the same position.

### Generation of Testing Set
We obtained the scenes from the large image by a non-over lapping grid with a cell size of 150x150. In this way, we generated 1920 (48x40) test scenes for each time point. Then they are categorized to the above classes by visual interpretation.

### Description of the content

```
./hanyang_data  
│  hanyang2002.jpg  ====> The overall pseudo-color image of Hanyang in 2002.  
│  hanyang2009.jpg  ====> The overall pseudo-color image of Hanyang in 2009.  
│  README.md  
│  
├─test  
│      hanyang2002      ====> Raw imagery of Hanyang in 2002, formatted in HDR. 
│      hanyang2002.hdr  
│      hanyang2002label.mat  ====> The labels of images in testing set of Hanyang in 2002, represented by a matrix with size of 48x40. Each element denote the Scene Class Number of an image of corresponding position.  
│      hanyang2009      ====> Raw imagery of Hanyang in 2009, formatted in HDR, and can be viewed by remote sensing softwares such as ENVI;  
│      hanyang2009.hdr    
│      hanyang2009label.mat  ====> The labels of images in testing set of Hanyang in 2009, represented by a matrix with size of 48x40. Each element denote the Scene Class Number of an image of corresponding position. 
│  
└─train  
    ├─first  
    │      l1_n1_x2987_y3748.tif      ====> A scene image of training set in 2002, where l denotes the Class Number, and n denotes the Number. 
    │      l1_n2_x3141_y3753.tif  
    │      l1_n3_x3280_y3787.tif  
    │      ...  
    │  
    └─second  
            l1_n10_x3748_y5322.tif      ====> A scene image of training set in 2009, where l denotes the Class Number, and n denotes the Number. 
            l1_n11_x3825_y5166.tif  
            l1_n1_x3237_y3772.tif  
            ...  
```
### Citation
Please consider citing the abovementioned articles if you used this dataset in your research.
```
@article{wu2016scene,
  title={A scene change detection framework for multi-temporal very high resolution remote sensing images},
  author={Wu, Chen and Zhang, Lefei and Zhang, Liangpei},
  journal={Signal Processing},
  volume={124},
  pages={184--197},
  year={2016},
  publisher={Elsevier}
}

@article{wu2017kernel,
  title={Kernel slow feature analysis for scene change detection},
  author={Wu, Chen and Zhang, Liangpei and Du, Bo},
  journal={IEEE Transactions on Geoscience and Remote Sensing},
  volume={55},
  pages={2367--2384},
  year={2017},
  publisher={IEEE}
}
```


### Copyright
Copyright &copy; 2019 [SIGMA Lab](http://sigma.whu.edu.cn/) (Sensing Intelligence, Geoscience and MAchine learning lab, Wuhan University, China).   

The MtS-WH dataset is only aothurized to be used in scientific research and academic papers. If you have any other questions about this dataset in your research, please contact us: chen.wu@whu.edu.cn
