---
title: R_introduction_180328_Zhaofei
author: zhaofei@sibs.ac.cn
---

## 说明：
1. 文档为**Markdown**[^1] 格式 ，可以使用相关编辑器查看和编辑，代码部分可以在R直接运行
2. 文档稍加调整可以直接用`RStudio`中的`R Presentation` 生成HTML版slides

---

## 数据科学重要性

- 摩尔定律[^2]
- 如何处理海量数据
- 如何进行归纳和预测
- 数据科学（Data science）：数据收集、处理、分析和呈现等
- 2012年哈佛商业评论将**Data Scientist**定义为21世纪最性感的职业[^3]。

![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/20167853.jpg)

## 数据科学和我们的关系

- 生命科学领域高通量测序价格下降和数据量快速增加

  ![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/60387706.jpg)

- 高效准确地从文献中找到自己需要的信息和数据

  ![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/47160729.jpg)

- 针对自己课题对已有信息和数据进行整合

- 正确处理并展示自己的实验数据

---

## 生物统计学重要性

- 数据科学家是21世纪最性感的职业
- 21世纪又是生命科学的世纪 : )
- 生物统计学是生物研究研究及重要却被经常忽视的内容

> There is no disputing the importance of statistical analysis in biological research, but too often it is considered only after an experiment is completed, when it may be too late.

**通过本学期生物统计课程**

- 学习（回忆）基本的统计学概念和知识
- 了解（入门）一种统计学常用编程语言
- 掌握文献中常用统计方法和展示方法
- 实验数据处理分析时能够独当一面
- 从湿实验走向干实验，或者转行……

---

## 怎样入门数据科学

> 课堂内容不仅仅可以用来处理生物学数据；学习并不轻松，能够入门已经不易。

### 数学和统计知识

- 课程会介绍最基本的统计学概念，多种常见的统计学模型和假设检验
- 努力回忆残存高中和大学数学与统计知识，理解常见的统计学概念

### 了解自己研究领域

- 没有背景的数据分析是没有意义的，生物学尤其如此

### 合理地获取数据

- 通过哪些途径和手段可以获取已有的公共数据
- 减少重复工作和盲目的工作，合理设计实验
- 确保自己的实验数据有意义

### 正确地处理数据

- 实验数据如何进行预处理
- 选择什么样的统计模型和方法

### 恰当地展示数据

- 如何把数据更好地展示给别人
- 画什么图，如何画图，用哪些结果

---

## 数据科学常用语言

> 罗列数据科学广泛应用的若干种语言（开发环境或者软件），说明R的优势。

###  Excel

- 最常用，最容易上手，非免费的
- 按列求和、查找替换、求方差标准差
- 常用函数 VLOOKUP/SUMIF/COUNTIF
- VBA 和宏

### MATLAB

- 建模，信号处理
- 图形化界面
- 非免费且贵

### Python

- 强大且用途极其广泛的编程语言
- 各种库可以满足不同需求：Tensorflow，NumPy，Pandas
- 容易入门，免费开源

### SQL

- 数据库操作：增删改查
- 大数据相关行业常用

### R 

- 统计学家为了统计学家进行统计学工作而开发的一种语言
- 免费开源，大量R包可以直接使用
-  生物信息分析一定会用到

---

## **为什么要学习R**

### R的诞生

1992年，Ross Ihaka和Robert Gentleman 在S语言（贝尔实验室开发的一种统计用编程语言）的基础上开始构思一种新的用于统计学分析的开源语言，直到1995年第一个版本正式发布（和各位年龄相仿）[^4]。

 据说是因为他们名字的第一个字母都是R，所以这门语言就被叫做R。这两个人都是统计学教授出身，再加上R语言的生父S语言，所以**R语言在统计学方面有着纯正的血统**。

![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/1329438.jpg)

### R的发展

- 作为开源软件的R能够迅速发展，很大程度上取决于其活跃的社区
- 学习R，很大程度上也是学习各种R包的使用
- 截止目前（2018年3月24日），CRAN(Comprehensive R Archive Network)[^5]上已经有12361个可以获取的R扩展包
- 各地的CRAN镜像是R网站的备份文件，内容完全一样，可以选择合适的镜像访问

### R的特长

**官网介绍** 

> R provides a wide variety of statistical (linear and nonlinear modelling, classical statistical tests, time-series analysis, classification, clustering, …) and graphical techniques, and is highly extensible. 

> One of R’s strengths is the ease with which well-designed publication-quality plots can be produced, including mathematical symbols and formulae where needed. 

- 多数统计相关的工作R都可以非常简洁的用几行命令完成

- R 高度的可扩展性体现在1万多个已有R包，绝大部分工作可以用现有的R包来辅助完成

- R 具有强大的绘图功能，可以画各种各样高逼格且直接用于发表的图

- Bioconductor[^6]中一千多个R包可以用来专门解决生物（信息）相关问题

  ![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/58146266.jpg)

---

## **R应用示例**


> 在这一部分，仅仅是给展示几个用R可以轻松完成的相对有趣的工作
> 安装对应包后应该可以直接运行


### 示例1 ggplot2 画图

```R
#install.packages("ggplot2")
library("ggplot2")
theta <- seq(0,24*pi, len=2000)
radius <- exp(cos(theta)) - 2*cos(4*theta) + sin(theta/12)^5
dd <- data.frame(x=radius*sin(theta), y=radius*cos(theta))
p <- ggplot(dd, aes(x, y))+geom_path()+xlab("")+ylab("") + theme_classic()
p
```

![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/55223622.jpg)

### 示例2 词频分析及词云

```R
#install.packages("wordcloud2")
library(wordcloud2)
wordcloud2(demoFreqC, size = 0.7, shape = 'diamond')
```

![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/32097450.jpg)

### 示例3 实时查看我国各地空气质量[^7]

```R
#install.packages("rvest")
#install.packages("leafletCN")
#install.packages("rgeos")
###
Sys.setlocale("LC_CTYPE", "eng")
library(rvest)
library(leafletCN)
library(rgeos)
doc = read_html("http://www.pm25s.com/cn/rank/")
cities = doc %>% html_nodes(".cityrank a") %>%
  html_text()
cities = iconv(cities, "UTF-8", "UTF-8")
AQI = doc %>% html_nodes("span[class^='lv']") %>%
  html_text() %>% .[c(F,F,T)] %>% as.numeric
dat = data.frame(city = cities, AQI = AQI)
geojsonMap(dat, "city",
           popup =  paste0(dat$city,":",dat$AQI),
           palette = "Reds", legendTitle = "AQI")
```

![](http://oxzxnm82k.bkt.clouddn.com/18-3-24/83788685.jpg)



---
## 尝试入门R语言

### 学习路线 

#### 通过考试

理论课后认真理解老师上课的内容，讨论课后消化作业题中用到的R语言知识点

- 了解一下R语言是什么，能干什么用
- 学习如何在R的官网下载R，如何在自己的电脑安装R并成功运行
- 学习如何安装Rstudio，并且了解其基本的用法（这步可省略）
- 学习如何查看R帮助文档（这步很重要）
- 学习如何将作业中的数据（作业中通常是txt或者csv格式）正确地导入R
- 了解R语言中的常见变量
- 学习R语言一些最基本的命令：如安装包、调用包、读入写入文件、构造矩阵和基础绘图
- 学习在R中如何使用（课上提到的）统计学相关函数，了解参数含义
- 能够独立完成最后几次作业和去年考题

#### 生物信息

- 了解R语言在生物信息学领域的应用。
- 理解R语言中的各种变量
- 学习如何创建数据集、清洗数据和使用常见的统计分析方法
- 能够对数据进行高级操作
- 学习R语言的中高级绘图方法，能够使用ggplot2
- 学习R中高级统计分析方法，如聚类、主成分分析和线性回归等
- 学习并熟练使用自己研究领域相关的R包（通过bioconductor）

### 入门的标准

拿到一份数据，第一反应是用R去处理；拿到一个任务，敢于用R去解决。

### 参考资料

**在线资料**

[R语言官网](https://www.r-project.org/)

[R语言官方文档](https://cran.r-project.org/manuals.html)

[RStudio官网](https://www.rstudio.com/)

[Bioconductor官网]( https://www.bioconductor.org/)

[R语言资料库](https://awesome-r.com/)

[R函数和包的在线帮助文档](https://www.rdocumentation.org/)

**中文书籍**

《R语言编程艺术》

《R语言实战(第2版)》

《统计建模与R软件》

《ggplot2:数据分析与图形艺术》

---

[^1]: R markdown 官网网站 http://rmarkdown.rstudio.com
[^2]: 摩尔定律 https://en.wikipedia.org/wiki/Moore%27s_law
[^3]: 相关文章 https://hbr.org/2012/10/data-scientist-the-sexiest-job-of-the-21st-century
[^4]: R language https://wiki2.org/en/R_(programming_language)
[^5]: CRAN官网 https://cran.r-project.org/
[^6]: Bioconductor官网 https://www.bioconductor.org/
[^7]: 示例3来源：http://langdawei.com/2017/01/07/aqi.html