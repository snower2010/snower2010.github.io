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
   
## 二. 组学数据类
### 2.1 DeepVariant

### 2.2 通过随机森林寻找腹泻中的病菌

## 三. 身体其他类数据
### 3.1 通过指甲判断检测身体状况

## 四. Drug discovery
### 4.1 神经系统药物的Drug Discovery

