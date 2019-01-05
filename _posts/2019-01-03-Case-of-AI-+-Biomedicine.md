---
layout:     post
title:      Cases of AI+Biomedicine
subtitle:   
date:       2019-01-04
author:     Denghui Liu
header-img: img/home-bg-art.jpg
catalog: true
tags:
    - AI
    - Biomedicine
---
总结更新目前结合人工智能和生物医疗的一些研究案例。

## 一. 医疗图像类
### 1.1. 通过小样本学习诊断颅内出血
   [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/An%20explainable%20deep-learning%20algorithm%20for%20the%20detection%20of%20acute%20intracranial%20haemorrhage%20from%20small%20datasets.pdf)

   [新闻报道](https://www.jiqizhixin.com/articles/2018-12-26)

   **数据**：904个颅内出血的CT,包含五种类型
  
   **模型**：Ensemble model: VGG167, ResNet-508, Inception-v39 and Inception-ResNet-v2

   **亮点**：在测试集上面达到了98%的灵敏度和95%的精确度；同时添加了一个attention map用于特异的检测出血点
   
   ![Figure1.1.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.1.1.jpg)

### 1.2. 谷歌AI从视网膜图像识别心血管疾病
    
   **亮点**：通过对284335名患者的数据进行深度学习的算法研究，研究人员能以惊人的高准确度预测病人的心血管疾病风险因素
    
### 1.3. 通过病理图片诊断非小细胞癌症，以及通过病理图片预测基因突变类型 （Inception V3）
   
   [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Classification%20and%20mutation%20prediction%20from.pdf)
   
   **数据**: 总共1,634个从TCGA上下载的病理学数据
   
   **模型**: 先从高清病理图随机取样，再通过 Inception V3进行三分类，AUC达到0.97;另外，针对每一个位点的突变，分别做了一个通过图像鉴别mutation的分类模型。
   
   **亮点**：分类精度比较高；同时结合了图像和突变的数据
   
   ![Figure1.3.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.3.1.jpg)

### 1.4 通过OCT图像鉴别诊断眼部疾病
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/2018.Cell.pdf)
  
  **数据**: 总共207，130个OCT图像
  
  **模型**：通过迁移学习，将imageNet的参数迁移到新数据上
  
  **亮点**: 数据量大；精确度很高，达到了95%；比较早的做医疗图像的文章，所以可以发表在cell上面
   
  ![Fig.1.4.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.4.1.jpg) 
  
## 二. 组学数据类

### 2.1 基于基因组数据通过随机森林寻找腹泻中的病菌
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Zoonotic%20Source%20Attribution%20of.pdf)
  
  [新闻报道](https://www.jiqizhixin.com/articles/2018-12-19-11)
  
  **数据**: 1,400多种沙门氏菌的基因组的序列
  
  **模型**: 随机森林做分类和特征提取
  
  **亮点**: 通过基因组进行分类，找到干扰源
### 2.2 通过VAE对转录组数据进行降维

## 三. 身体其他类数据
### 3.1 通过指甲判断检测身体状况
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Wearable%20Nail%20Deformation%20Sensing%20for%20Behavioral%20and%20Biomechanical%20Monitoring%20and%20Human-Computer%20Interaction.pdf)
  
  [新闻报道](https://www.jiqizhixin.com/articles/2018-12-28-20)
  
  **数据**: 通过可穿戴传感器采集指甲盖上面的信息
  
  **模型**: 传统机器学习方法，类似最近邻
  
  **亮点**: 可穿戴设备的健康监测
  
## 四. Drug discovery
### 4.0 综述
  [The rise of deep learning in drug discovery](https://github.com/snower2010/snower2010.github.io/blob/master/img/The%20rise%20of%20deep%20learning%20in%20drug%20discovery.pdf)
  
  **CNN模型**
  ![Figure4.0.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/4.0.1.jpg)
  
  **VAE模型**
  ![Fig.4.0.2](https://github.com/snower2010/snower2010.github.io/blob/master/img/4.0.2.jpg)
  
  **RNN模型**
  ![Fig.4.0.3](https://github.com/snower2010/snower2010.github.io/blob/master/img/4.0.3.jpg)
  
### 4.1 AtomNet
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/AtomNet.pdf)
  
  **数据**: 分子的空间结构数据
  
  **模型**: 4层CNN模型
  
  **亮点**: 基于空间结构的drug discovery，准确率比较高
