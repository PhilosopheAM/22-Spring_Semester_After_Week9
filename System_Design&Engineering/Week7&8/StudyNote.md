# 第七周&第八周上课笔记
<!--StudyNote使用md写成，实际展示效果依据不同渲染器而定-->

## Preliminary Design 初步设计

我们在完成系统层面上的设计以后（走完SNR、SDR等流程以后）就已经定义了系统层面上的需求(** System-level requirements**). 下一步就要具体到子系统、子模块该怎么做。  
以造房子为例，Preliminary Design 就是已经确定一种造房子的方案以后继续确定(elaborate)各个房间、或者各个功能模块（如水管线路、电路排布等）在preliminary design环节中我们主要用到对系统层次需求的分解(decompose)和推断(derive)。可以利用先前提到过的如[FFBD工具](https://youtu.be/Ii1MI68MKDs)来完成这一步骤。
在进行PD流程(Preliminary Design)的时候，我们要意识到已经从甲方过渡到乙方了；我们先前讨论的偏向概念、功能，而在之后的步骤中要将注意力放在物理层。

### 子系统 (sub-system) 的开发路径选择
![](source\img\子系统的三种实现路径-商用购买、商用适配、自研.png)很显然，自研（**风险的发生性与风险发生造成的危害都很高**）是最难的，但也因为可控性强，最能够实际适应产品需要。  
原则上我们尽量购买市场上成熟的、现有的商品；但是一切都要从实际出发。最重要的还是不断地iterate.

### 初步设计的验收 Review
**PDR**(Preliminary Design Review)考虑技术风险（**风险的发生性与风险发生造成的危害**）和是否满足FBL.



