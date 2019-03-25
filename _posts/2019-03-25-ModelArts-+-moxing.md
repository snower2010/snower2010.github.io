---
layout:     post
title:      ModelArts and Moxing
subtitle:   
date:       2019-03-25
author:     Denghui Liu
header-img: img/home-bg-art.jpg
catalog: true
tags:
    - modelArts
    - moxing
---
总结学习到的有关modelArts和moxing的知识点。

## 一. moxing
### 1.1. moxing的文件操作系统
MoXing支持本地和S3路径的读取，为了同时使用，可以import如下语句

import moxing as mox

mox.file.shift('os', 'mox')
