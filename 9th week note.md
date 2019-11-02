# 第9周笔记

## Talking  

Direction:  ***Weakly Supervised*** or ***Transfer Learning*** ?

 Mon, Oct 28 th 2019   

> - **独立思考**，提出自己的看法
> - **聚焦**在某一领域，**深入挖掘**
> - 要么不做，要做就要**考虑清楚**
> - 切记做无用功，自己感动自己
> - **坚持写笔记**，知道自己都干了些什么
> - Reading Paper: 先看**Abstract**和**Graphs**，**看对眼**再往下读
> - 提高英语，各方面的水平
> - 准确**表达**（多？ 什么是多？多少是多？）
>   + 用事实说话，通过数据来量化，例如图示

---

## Research Tips

+ [周志华教授报告：如何做研究与写论文？](https://mp.weixin.qq.com/s/h-sr__H7gNDO_aJc1IToWg)

![img](https://mmbiz.qpic.cn/mmbiz_jpg/vI9nYe94fsHwOxjk5vmKiaGWVswpMib5Baz9n6nI5zsicGhRyLcM2TbEzYrpJrhg5xkN8M8tEnJy7w1e9Qic9qdf7Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



> Try to avoid this scenario
>
> 1. Nothing special in data pipeline. Uses prepackaged source
> 2. Team starts late. Just instance and draft of code up by milestone
> 3. Explore 3 architectures with code that already exists 
>    + a. One RES-net, then a VGG, and then some slightly different thing
> 4. Only ran models until they got ~65% accuracy
> 5. Didn’t hyperparameter search much
> 6. A few standard graphs: loss curves, accuracy chart, simple architecture graphic
> 7. Conclusion doesn’t have much to say about the task besides that it didn’t work

---

>  Aim for this
>
> 1. Workflow set-up configured ASAP
> 2. Have running code and have baseline model running and fully-trained
> 3. Creative hypothesis is being tested
> 4. Mixing knowledge from different aspects in DL
> 5. Have a meaningful graphic (pretty or info rich)
> 6. Conclusion and Results teach me something
> 7. ++interactive demo
> 8. ++novel / impressive engineering feat
> 9. ++good results

---

##  Today Reading

Mon, Oct 28 th  2019 

### [Weakly Supervised Open-set Domain Adaptation by Dual-domain Collaboration](http://arxiv.org/abs/1904.13179)

### Original:

In conventional domain adaptation, a critical assumption is that there exists a fully labeled domain (source) that contains the same label space as another unlabeled or scarcely labeled domain (target). However, in the real world, there often exist application scenarios in which both domains are partially labeled and not all classes are shared between these two domains. Thus, it is meaningful to let partially labeled domains learn from each other to classify all the unlabeled samples in each domain under an open-set setting. We consider this problem as weakly super- vised open-set domain adaptation. To address this practical setting, we propose the Collaborative Distribution Alignment (CDA) method, which performs knowledge transfer bilaterally and works collaboratively to classify unlabeled data and identify outlier samples. Extensive experiments on the Office benchmark and an application on person re- identification show that our method achieves state-of-the- art performance.

### Extract

conventional domain adaption assumption source domain and target domain contains the same label space. However, in the real application scenarios is difficult to satisfy this condition. 



---

## Today Reading

Tue, Oct 29, 2019

发现一个知乎高赞回答读论文的方法，和李老师说的方法高度一致，文中还给出了详细的步骤，原文在[这里](https://www.zhihu.com/question/345516318)。以下是今天的内容，我尝试按照这个思路尝试挖掘文中信息

[Weakly Supervised Complementary Parts Models for Fine-Grained Image Classification from the Bottom Up](http://arxiv.org/abs/1903.02827)

### Original:

Given a training dataset composed of images and corresponding category labels, deep convolutional neural networks show a strong ability in mining discriminative parts for image classification. However, deep convolutional neural networks trained with image level labels only tend to focus on the most discriminative parts while missing other object parts, which could provide complementary information. In this paper, we approach this problem from a different perspective. We build complementary parts models in a weakly supervised manner to retrieve information suppressed by dominant object parts detected by convolutional neural networks. Given image level labels only, we first extract rough object instances by performing weakly supervised object detection and instance segmentation using Mask R-CNN and CRF-based segmentation. Then we estimate and search for the best parts model for each object instance under the principle of preserving as much diversity as possible. In the last stage, we build a bi-directional long short-termmemory (LSTM) network to fuze and encode the partial information ofthese complementary parts into a comprehensive feature for image classification. Experimental results indicate that the proposed method not only achieves significant improvement over our baseline models, but also outperforms state- of-the-art algorithms by a large margin (6.7%, 2.8%, 5.2% respectively) on Stanford Dogs 120, Caltech-UCSD Birds 2011-200 and Caltech 256.

### Extract 

+ Question:

  > Deep CNN trained with image level labels only tend to focus on the most discriminative parts while missing other object parts, which could provide complementary information. 

+ Method

  > The researchers build complementary parts models in a weakly supervised manner to retrieve information suppressed by dominant object parts detected by convolutional neural networks. Given image level labels only, we first extract rough object instances by performing weakly supervised object detection and instance segmentation using Mask R-CNN and CRF-based segmentation. 

+ Answer

  > They estimate and search for the best parts model for each object instance under the principle of preserving as much diversity as possible. In the last stage, we build a bi-directional long short termmemory (LSTM) network to fuze and encode the partial information of these complementary parts into a comprehensive feature for image classification. 

---

## Today Reading 

Wed, Oct 30, 2019

[Weakly Supervised Brain Lesion Segmentation via Attentional Representation Learning](https://link.springer.com/chapter/10.1007%2F978-3-030-32248-9_24)

MICCAI 2019, LNCS 11766, pp. 211–219, 2019

### Abstract

In this paper, we propose a new weakly supervised 3D brain lesion segmentation approach using attentional representation learning. Our approach only requires image-level labels, and is able to produce
accurate segmentation of the 3D lesion volumes. To achieve that, we design a novel dimensional independent attention mechanism on top of the Class Activation Maps (CAMs), which refines the 3D CAMs to obtain better estimates of the lesion volumes, without introducing significantly more trainable variables. The generated attentional CAMs are then used as a source of weak supervision signals to learn a representation model, which can reliably separate the voxels belong to the lesion volumes from
those of the normal tissues. The proposed approach has been evaluated on the publicly available BraTS and ISLES datasets. We show with comprehensive experiments that our approach significantly outperforms the competing weakly-supervised methods in both initial lesion localization and the final segmentation, and is able to achieve comparable Dice scores in segmentation comparing to the fully supervised baselines.

### Extract 

The researchers propise a new weakly supervised 3D brain lesion segmentation approach only requires image-level labels, which is able to produce accurate segmentation of the 3D lesion volumes. The proposed approach has been validated on **two public datasets**, the **BraTS** and **ISLES**, where experimental results showv that their approach offers superior performance to the state-of-the-art, and can achieve comparable segmentation accuracy with the fully supervised methods.



---

## Today Reading 

Thu, Oct 31, 2019

[Not All Areas Are Equal: Transfer Learning for Semantic Segmentation via Hierarchical Region Selection](http://openaccess.thecvf.com/content_CVPR_2019/papers/Sun_Not_All_Areas_Are_Equal_Transfer_Learning_for_Semantic_Segmentation_CVPR_2019_paper.pdf)

### Abstract

The success of deep neural networks for semantic segmentation heavily relies on large-scale and well-labeled datasets, which are hard to collect in practice. Synthetic data offers an alternative to obtain ground-truth labels for free. However, models directly trained on synthetic data often struggle to generalize to real images. In this paper, we consider transfer learning for semantic segmentation that aims to mitigate the gap between abundant synthetic data (source domain) and limited real data (target domain). Unlike previous approaches that either learn mappings to target domain or finetune on target images, our proposed method jointly learn from real images and selectively from realistic pixels in synthetic images to adapt to the target domain. Our key idea is to have weighting networks to score how similar the synthetic pixels are to real ones, and learn such weighting at pixel, region and image-levels. We jointly learn these hierarchical weighting networks and segmentation network in an end-to-end manner. Extensive experiments demonstrate that our proposed approach significantly outperforms other existing baselines, and is applicable to scenarios with extremely limited real images.



---

## Today Reading 

Fri, Nov 1, 2019

[Min-Max Statistical Alignment for Transfer Learning]()

### Abstract

A profound idea in learning invariant features for transfer learning is to align statistical properties of the domains. In practice, this is achieved by minimizing the disparity between the domains, usually measured in terms of their statistical properties. We question the capability ofthis school of thought and propose to minimize the maximum disparity between domains. Furthermore, we develop an end-to- end learning scheme that enables us to benefit from the proposed min-max strategy in training deep models. We show that the min-max solution can out perform the existing statistical alignment solutions, and can compete with state-of- the-art solutions on two challenging learning tasks, namely, Unsupervised Domain Adaptation (UDA) and Zero-Shot Learning (ZSL).

---



## Today Reading 

Sat, Nov 2, 2019

[Large Scale Fine-Grained Categorization and Domain-Specific Transfer Learning](https://ieeexplore.ieee.org/document/8578530/)

Cornell University, Google Research

### Abstract 

Transferring the knowledge learned from large scale datasets (e.g., ImageNet) via fine-tuning offers an effective solution for domain-specific fine-grained visual categorization (FGVC) tasks (e.g., recognizing bird species or car make & model). In such scenarios, data annotation often calls for specialized domain knowledge and thus is difficult to scale. In this work, we first tackle a problem in large scale FGVC. Our method won first place in iNaturalist 2017 large scale species classification challenge. Central to the success of our approach is a training scheme that uses higher image resolution and deals with the long-tailed distribution of training data. Next, we study transfer learning via fine-tuning from large scale datasets to small scale, domain- specific FGVC datasets. We propose a measure to estimate domain similarity via Earth Mover’s Distance and demon- strate that transfer learning benefits from pre-training on a source domain that is similar to the target domain by this measure. Our proposed transfer learning outperforms Im- ageNet pre-training and obtains state-of-the-art results on multiple commonly used FGVC datasets.