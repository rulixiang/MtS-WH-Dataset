### Description of the Hanyang dataset
This dataset consists of two large-size VHR images, which have a size of 7200x600 and are respectively acquired by IKONOS sensors in Feb, 2002 and Jun, 2009. The images cover the the Hanyang District, Wuhan City, CHina and contains 4 spectral bands (R, G, B and Near-Infrared). The spatial resolution of the images is 1m.

### Generation of Training Set


### Generation of Testing Set


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
│      hanyang2009      ====> Raw imagery of Hanyang in 2002, formatted in HDR.  
│      hanyang2009.hdr    
│      hanyang2009label.mat  ====> The labels of images in testing set of Hanyang in 2002, represented by a matrix with size of 48x40. Each element denote the Scene Class Number of an image of corresponding position. 
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
[1] Wu, Chen, Lefei Zhang, and Liangpei Zhang. "A scene change detection framework for multi-temporal very high resolution remote sensing images." Signal Processing 124 (2016): 184-197.
[2] Wu, Chen, Liangpei Zhang, and Bo Du. "Kernel slow feature analysis for scene change detection." IEEE Transactions on Geoscience and Remote Sensing 55.4 (2017): 2367-2384.
Please cite the abovementioned articles should you used this dataset in your research.
