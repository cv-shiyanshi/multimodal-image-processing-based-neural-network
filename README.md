主要是对多模态视觉图像的网络架构进行综述，同时对大家当前使用的模型结构进行总结，方便今后的使用。

# 综述文章
综述文章指的是多模态机器学习方法的综述文章。

## 图像融合
下面是多模态融合的综述文章：
1. Ramachandram D, Taylor G W. **Deep multimodal learning: A survey on recent advances and trends **[J]. IEEE Signal Processing Magazine, 2017, 34(6): 96-108.
深度学习提供了方便的融合机制，这篇文章将多模态信息融合分为early fusion,intermediate fusion 和late or decision-level fusion。
![Fusion Struture](https://raw.githubusercontent.com/cv-shiyanshi/multimodal-image-processing-based-neural-network/master/images/fusion.png)

2. James A P, Dasarathy B V. **Medical image fusion: A survey of the state of the art**[J]. Information Fusion, 2014, 19: 4-19. 
这篇文章综述了医学图像融合的方法，主要按照Morphology(形态，纹理，颜色等),Knowledge, Wavelets, Artificial neural networks, Fuzzy logic 这样进行分类。

# 特征级融合
## 前端融合
前端融合指的是经过一定的特征提取过程进行的特征融合，或者是完全不做处理进行特征融合。
1. Dong H, Yang G, Liu F, et al. **Automatic brain tumor detection and segmentation using U-Net based fully convolutional networks**[C]//Annual Conference on Medical Image Understanding and Analysis. Springer, Cham, 2017: 506-517.[**github**](https://github.com/zsdonghao/u-net-brain-tumor)
这篇文章将MRI的不同模态看作是图片不同的通道，可以看作是前端融合。

## 中端融合
经过了一些神经网络的层，比如卷积层池化层后进行融合。
1. Liu J, Zhang S, Wang S, et al. **Multispectral Deep Neural Networks for Pedestrian Detection**[J]. (BMVC, 2016)  
这篇是讲双谱行人检测的，基于fasterrcnn方法，提出了4种将红外图像和彩色图像融合的方法，最终实验得出结论，在特征提取的中期，也就是在vgg16的第四层卷积层的时候融合效果最佳。
## 后端融合
在进行决策之前进行融合，通过对融合的信息进行处理，最后得到分类分割或者检测的结果。  
1. Wagner J, Fischer V, Herman M, et al. **Multispectral Pedestrian Detection using Deep Fusion Convolutional Neural Networks** (ESANN, 2016)  
这篇是讲双谱行人检测的，基于caffenet提取特征，实验对比了前端融合和后端融合，得出结论，在全连接层（f7）对红外图像和彩色图像融合效果最佳。
