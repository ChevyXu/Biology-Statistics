

---
title: "使用DESeq2分析RNA-seq数据"
author: "Chunhui Xu"
date: "2021/4/19"
output: html_document
---
# Bio-Statistics

```{r setup, include=FALSE}
knitr::opts_chunk$set(echo = TRUE)
```
---

本文依据[Analyzing RNA-seq data with DESeq2](<http://bioconductor.org/packages/devel/bioc/vignettes/DESeq2/inst/doc/DESeq2.html>)进行解读后撰写，包含差异分析必备流程及必备知识

---

前言：RNA-seq的基本任务就是检测差异基因，基于我们拥有的多个样本表达矩阵数据，一个重要的问题就是基因表达的定量和在不同条件下表达变化的统计推断。

DEseq2包提供了基于负二项分布构建的线性模型对差异表达进行检测，使用数据的先验分布进行离散程度及倍数变化的估计。

> 如果你在发表文章时使用到DEseq2包，请引用：
>
> Love, M.I., Huber, W., Anders, S. (2014) Moderated estimation of fold change and dispersion for RNA-seq data with DESeq2. *Genome Biology*, **15**:550. [10.1186/s13059-014-0550-8](http://dx.doi.org/10.1186/s13059-014-0550-8)



# Bio-Statistics

> 这是徐春晖于2019学年 春季学期 当助教时 所使用的材料

http://xuchunhui.top/Bio-Statistics/

|   课程   |  使用PPT   |  下载资源    |
| ---- | ---- | ---- |
|  Class1    |    http://xuchunhui.top/Bio-Statistics/First_class.html  |      |
|  Class2    |    http://xuchunhui.top/Bio-Statistics/Second_class.html  |      |
|  Class3    |    http://xuchunhui.top/Bio-Statistics/Third_class.html  |      |
