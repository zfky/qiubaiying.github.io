---
layout:     post                       # 使用的布局（不需要改）
title:   协同过滤推荐算法测试               # 标题 
subtitle:   Recommender Algorithm for Collaborative filtering   #副标题
date:       2017-05-06                 # 时间
author:     ZFKY                         # 作者
header-img: img/post-bg-2015.jpg     #这篇文章标题背景图片
catalog: true                         # 是否归档
tags:                                #标签
    - 推荐算法
---
>  Recommender Algorithm for Collaborative filtering

# Recommender Algorithm #

Data: movielens   

- All dataset files size 22593713. 
- Data size of training is 900425.
- Data size of testing is 99784

Code: [librec](http://www.librec.net/ "librec1")

|  Recommender Algorithm  |          RMSE           |
| :---------------------: | :---------------------: |
| AspectModelRecommender  |   0.9273950652614509    |
| ASVDPlusPlusRecommender |   1.1151694495469084    |
|   BiasedMFRecommender   |   0.8636817659221292    |
|     BPMFRecommender     |                         |
|   BPoissMFRecommender   |    1.80545031663211     |
|    FMALSRecommender     |                         |
|    FMSGDRecommender     |                         |
|    GPLSARecommender     | 0.927811768257633/slow  |
|     LDCCRecommender     |   1.1151694495469084    |
|    LLORMARecommender    |   0.8617437187493111    |
|    MFALSRecommender     |   0.8680327278346128    |
|     NMFRecommender      |   0.9482805092307253    |
|     PMFRecommender      | 0.8900394037453517/fast |
|     RBMRecommender      |    1.45823346673343     |
|    RFRecRecommender     |                         |
| SVDPlusPlusRecommender  |   0.8678199152757183    |
|     URPRecommender      |  1.1151694495469084/f   |



