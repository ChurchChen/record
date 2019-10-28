# 第9周笔记

## Talking  

Direction:  ***Weakly Supervised*** or ***Transfer Learning***

>  Mon, Oct 28th 2019   

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

> Mon, Oct 28th  2019 

### [Weakly Supervised Open-set Domain Adaptation by Dual-domain Collaboration](http://arxiv.org/abs/1904.13179)

### Original:

In conventional domain adaptation, a critical assumption is that there exists a fully labeled domain (source) that contains the same label space as another unlabeled or scarcely labeled domain (target). However, in the real world, there often exist application scenarios in which both domains are partially labeled and not all classes are shared between these two domains. Thus, it is meaningful to let partially labeled domains learn from each other to classify all the unlabeled samples in each domain under an open-set setting. We consider this problem as weakly super- vised open-set domain adaptation. To address this practical setting, we propose the Collaborative Distribution Alignment (CDA) method, which performs knowledge transfer bilaterally and works collaboratively to classify unlabeled data and identify outlier samples. Extensive experiments on the Office benchmark and an application on person re- identification show that our method achieves state-of-the- art performance.

### Extract

conventional domain adaption assumption source domain and target domain contains the same label space. However, in the real application scenarios is difficult to satisfy this condition. 

