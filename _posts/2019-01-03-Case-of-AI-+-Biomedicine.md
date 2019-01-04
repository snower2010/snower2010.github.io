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
### 1. 通过小样本学习诊断颅内出血
[文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/An%20explainable%20deep-learning%20algorithm%20for%20the%20detection%20of%20acute%20intracranial%20haemorrhage%20from%20small%20datasets.pdf)

[新闻报道](https://www.jiqizhixin.com/articles/2018-12-26)

  **数据**：904个颅内出血的CT,包含五种类型
  
  **模型**：Ensemble model: VGG167, ResNet-508, Inception-v39 and
Inception-ResNet-v2

  **亮点**：在测试集上面达到了98%的灵敏度和95%的精确度；同时添加了一个attention map用于特异的检测出血点
  ![Figure1.1.1](img/1.1.1.jpg)

