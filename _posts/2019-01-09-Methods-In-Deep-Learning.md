---
layout:     post
title:      总结自己学习到的东西
subtitle:   
date:       2019-01-09
author:     Denghui Liu
header-img: img/home-bg-art.jpg
catalog: true
tags:
    - AI
    - Deep Learning
---
总结一下自己学到的知识点

** Layer Normaliztion

相比于batch normalization
batch是“竖”着来的，各个维度做归一化，所以与batch size有关系。
layer是“横”着来的，对一个样本，不同的神经元neuron间做归一化。

![Figure](https://github.com/snower2010/snower2010.github.io/blob/master/img/Layer%20Normalization.png)
