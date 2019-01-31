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

   [新闻报道](https://cloud.tencent.com/developer/news/113204)
   
   [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Prediction%20of%20cardiovascular%20risk%20factors%20from%20retinal%20fundus%20photographs%20via%20deep%20learning.pdf)
   
   **数据**: 284335志愿者的视网膜眼底图像
   
   **模型**: CNN模型
   
   **亮点**：能够高准确度预测病人的性别，年龄，心血管疾病风险因素等
   
   ![Figure1.2.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.2.1.jpg)
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
  
### 1.5 通过面部图像诊断遗传疾病(DeepGestalt)
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Identifying%20facial%20phenotypes%20of%20genetic%20disorders%20using%20deep%20learning.pdf)
  [新闻报道](https://mp.weixin.qq.com/s?__biz=MzA3MzQyNjY1MQ==&mid=2652465617&idx=3&sn=10e81925507c0bc0314b33e968fa9379&chksm=84e2fa65b3957373c900632118eb9ed75023660e8c9ac347c7bd352d9efb7f09eb3cfc0aaec4&scene=0&xtrack=1#rd)
  
  **数据**: 超过17,000个图像；包含上百种遗传病
  
  **模型**：首先在Casia-WebFace数据上pretrain，然后在fune-tunning
  
  **亮点**: 数据量大；精确度很高；同时找了phenotype和genetype之间的关联
   ![Fig.1.5.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.5.1.jpg)

### 1.6 通过心电图数据监测心律失常 （斯坦福大学）
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Cardiologist-level%20arrhythmia%20detection%20and%20classification%20in%20ambulatory%20electrocardiograms%20using%20a%20deep%20neural%20network.pdf)
  
  [新闻报道](https://www.chainnews.com/articles/847671770585.htm)
  
  **数据**: 包含53549名患者的91232的心电图数据，分(1s)时间段切割
  
  **模型**: CNN网络，总共34层
  
  **亮点**: Andrew NG的工作；首次对心电图构建了神经网络，达到了超过人类的精确度；心电图在医学中应用中很多，可以方便的智能检测或者智能监护

### 1.7 人工智能的心电图筛查心脏收缩功能障碍 （梅奥诊所）
 [文献]（https://github.com/snower2010/snower2010.github.io/blob/master/img/Screening%20for%20cardiac%20contractile%20dysfunction%20using%20an%20artificial%20intelligence%E2%80%93enabled%20electrocardiogram.pdf）
  
  [新闻报道](https://mp.weixin.qq.com/s?__biz=MzU1MzMxMzcyMg==&mid=2247488480&idx=1&sn=f370a78537f944c457a88794bd4e6e23&chksm=fbf5e735cc826e23b6949349efb8255dd5c9f4f85eb519958e1225cad1f41c111947a3348bc1&mpshare=1&scene=1&srcid=0109LUrnK69V1BT1q2DptPpd#rd)
  
  **数据**: 来自梅奥诊所的44,959名患者心电图谱
  
  **模型**：CNN网络
  
  **亮点**：便宜快速的检测心脏疾病；数据量大

### 1.8 通过病理图像鉴别转移性乳腺癌
  
  [新闻报道](https://mp.weixin.qq.com/s?__biz=MzU3MTM5OTk2OA==&mid=2247485830&idx=1&sn=8bcd2e9aeba9a8844db131b732b28752&chksm=fce183c9cb960adf535f395d30377525c807072ab829018ad911a48328980be13d0de8a3e3f6&scene=0#rd)
  
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Development%20and%20Validation%20of%20a%20Deep%20Learning%20Algorithm%20for%20Improving%20Gleason%20Scoring%20of%20Prostate%20Cancer.pdf)
  
  **数据**: 399张淋巴结图片
  
  **模型**: Inception V3
  
  **亮点**: 达到了比较高的准确度99.3%；并且可以识别出肿瘤区域
  
  ![Figure.1.8.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.8.1.jpg)

### 1.9 针对X光胸片诊断

  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Learning%20what%20to%20look%20in%20chest%20X-rays%20with%20a%20recurrent%20visual%20attention%20model.pdf)
  
  **数据**: 47万张胸片X光图像和对应的诊断报告
  
  **模型**：结合CNN和LSTM的模型，学习X光图像和诊断报告的关系，将X光片分为了四种等级：危险、紧急、不紧急、正常
  
  **亮点**: AI报告的阴性预测率高达99%，也就是说，AI基本不会漏掉有问题的胸片，并确保这些有问题的胸片优先被医生查看。在AI系统的帮助下，紧急状况的胸片病例处理时间从11.2天缩短至2.7天，所需时间仅为原来的1/4。
  
  ![Figure.1.9.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/1.9.1.jpg)

## 二. 组学数据类

### 2.1 基于基因组数据通过随机森林寻找腹泻中的病菌
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Zoonotic%20Source%20Attribution%20of.pdf)
  
  [新闻报道](https://www.jiqizhixin.com/articles/2018-12-19-11)
  
  **数据**: 1,400多种沙门氏菌的基因组的序列
  
  **模型**: 随机森林做分类和特征提取
  
  **亮点**: 通过基因组进行分类，找到干扰源
  
### 2.2 通过VAE对转录组数据进行降维
  
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/VAE%20For%20Single%20Cell.pdf)
  
  **数据**: TCGA下载的转录组数据
  
  **模型**: 通过一层/两层的VAE模型将转录组数据降维，并进而进行分类，找到对应的coding的的基因
  
  **亮点**: 提供了一个转录组学降维的学习框架
  
  ![Figure.2.2.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/2.2.1.jpg)

### 2.3 构建人类大脑的多组学数据
   [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Comprehensive%20functional%20genomic%20resource%20and%20integrative%20model%20for%20the%20human%20brain.pdf)
   
   **数据**： 包含有RNA-seq, ATAC-seq，modification等
   
   **模型**: genetic variants来预测brain disease phenotypes
   
## 三. 其他类数据
### 3.1 通过指甲判断检测身体状况
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Wearable%20Nail%20Deformation%20Sensing%20for%20Behavioral%20and%20Biomechanical%20Monitoring%20and%20Human-Computer%20Interaction.pdf)
  
  [新闻报道](https://www.jiqizhixin.com/articles/2018-12-28-20)
  
  **数据**: 通过可穿戴传感器采集指甲盖上面的信息
  
  **模型**: 传统机器学习方法，类似最近邻
  
  **亮点**: 可穿戴设备的健康监测

### 3.2 谷歌通过电子病历做预测

  [新闻报道](https://www.leiphone.com/news/201801/geD2NyxSigWBUmHB.html)
  
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/Scalable%20and%20accurate%20deep%20learning%20with%20electronic%20health.pdf)
  
  **数据**: 114,003个病人的216,221条住院记录
  
  **模型**: 首先将数据投影到低维空间，接下来分别采用了LSTM,前馈神经网络和决策树
  
  **亮点**：首先用了FHIR组件将数据标准化，并在CSF和UChicago的电子病历数据上，用深度学习模型预测四件事情：住院期间的死亡风险、规划之外的再住院风险、长时间的住院天数以及出院的疾病诊断。 
  ![Figure.3.2.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/3.2.1.jpg)
  
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

## 五. 其他
### 5.1 Nature medicine综述AI+医疗
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/The%20practical%20implementation%20of%20artificial%20intelligence%20technologies%20in%20medicine.pdf)
  [新闻报道](https://mp.weixin.qq.com/s?__biz=MzI5MDQzNjY2OA==&mid=2247490973&idx=1&sn=85e616485be03f3addbd864a24970087&chksm=ec1ebecedb6937d814fb748d283985f035a59133f23fd934c0d2465d4baf2cdcfbb53f9e8e58&scene=0&xtrack=1#rd)
  
  ![Fig.5.1.1](https://github.com/snower2010/snower2010.github.io/blob/master/img/5.1.1.jpg)
### 5.2 Nature medicine 综述AI医疗
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/A%20guide%20to%20deep%20learning%20in%20healthcare.pdf)
  
  [文献](https://github.com/snower2010/snower2010.github.io/blob/master/img/High-performance%20medicine%20the%20convergence%20of%20human%20and%20artificial%20intelligence.pdf)
  
  
