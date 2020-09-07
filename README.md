# ReadPapaers（论文拾贝）简介
本仓库记录自己读过的一些经典papers， 主要包括推荐系统， NLP， 时空序列预测， 海表温预测等方向，  对于精读论文， 会写相关的论文笔记和代码，
而通读的论文会总结一些思想，把所有论文放在一块便于统一管理和查看。对于比较好的论文， 还会单独总结成博客， 所以这个仓库和博客是链接起来的。

<br>博客地址[https://blog.csdn.net/wuzhongqiang/category_9722295.html](https://blog.csdn.net/wuzhongqiang/category_9722295.html)

# 写在前面：
## 1. 我们为什么读论文？
1. 构建知识体系： 通过Related Work快速了解该方向的研究现状， 追踪经典论文
2. 紧跟前沿技术： 了解领域内新技术和效果， 快速借鉴到自身项目
3. 培养科研逻辑： 熟悉论文体系， 了解如何创造新事物， 培养良好科研习惯
4. 写论文： 多读才会写
5. 面试找工作： 涉及大量的面试问题， 丰富建立必备

## 2. 读哪些论文？ 
我们读的论文大致分为两类：
* 综述论文： 快速熟悉某领域的发展历程， 现状及子方向， 了解领域内基础概念和关键词
* 专题论文： 介绍具体算法， 可学习其设计思路， 实验技巧， 代码实现等具体技术

高质量论文角度：
* 高质量期刊会议： CVPR, ECCV, ICCV, AAAI, NIPS, ICLR, ICML等
* 高引论文： 同行间普遍认可， 参考借鉴的论文
* 知名团队： Yoshua Bengio, Yann LeCun, Geoffrey Hinton, Andrew Ng等
* 有代码论文： “Talk is cheap, Show me the code”
* 推荐网站：[https://paperswithcode.com](https://paperswithcode.com)


## 3. 如何找论文
如果不知道论文题目， 依据**关键字**搜索相关领域论文。
* 知网： 寻找优质综述， 快速入门
* 百度学术， 谷歌学术
* arXiv: [https;//arxiv.org]论文预印本
* 顶会： CVPR, ECCV, ICCV, AAAI, NIPS, ICLR, ICML等
是否优质， 看影响因子（Impact Factor IF）: 期刊前N年发表的论文被引数除以前N年发表的论文数， 通常N=2或者N=5， JCR(Journal Citation Reports, 期刊引证报告): 统计SCI期刊的论文引用数据， 给出各期刊的IF。SCI期刊分区：
  * JCR方式， 一、二、三、四区各占25%
  * 中科院方式， 一区为前5%， 二区为5%-20%， 三区为20%-50%， 四区为50%-100%
下面给出几个比较好的论文网站：
  * sci-hub:[http://tool.yovisun.com/scihub/](http://tool.yovisun.com/scihub/) , 一个能绕过科研论文收费的神奇网站 [https://sci-hub.tw](https://sci-hub.tw)、[https://sci-hub.si](https://sci-hub.si)、[https://sci-hub.se](https://sci-hub.se), DOI码， 是数字对象的唯一标识符， 相当于文献的数字身份证， 所以拿DOI去搜就可以。
  * DBLP: [https://dblp.uni-trier.de/db/](https://dblp.uni-trier.de/db/)
  * PaperWeekly: [http://www.paperweekly.site/](http://www.paperweekly.site/)
  * 如果是在读研究生， 一般学习会有买各种论文网站资源，这个简直美滋滋。

## 4. 一篇论文的大体结构布局：
1. **Abstract**： 论文简介， 阐述工作内容， 创新点， 效果
2. **Introduction**： 介绍研究背景， 研究意义， 发展历程， 提出问题
3. **Related Work**： 相关研究算法简介， 分析存在的缺点
4. **OurWork**： 论文的主要方法， 实现细节
5. **Experiments**： 实现步骤及结果分析
6. **Discussion**： 论文的结论及未来可研究方向
## 5. 如何读论文：
三部曲： 泛读、精读、总结
* 泛读： 快速浏览， 把握概要， 重点读**标题， 摘要， 结论， 所有小标题和图表** <br>泛读目标和效果自测： 还是那三个问题， 论文解决什么问题？ 采用什么方法？ 达到什么效果？
* 精读： 选出精华， 仔细阅读， 每一部分详细读<br> 精读目标和效果自测： 所读段落是否详细掌握， 核心思想是否能自己捋清楚， 是否可以不看论文通过博客记录文章的主要原理
* 总结： 总览全文， 归纳总结， 文中的创新点， 关键点， 启发点（这个就是我README.md的总结）


## 6. 论文代码的学习方法
1. **任务定义**： 搞清楚程序的目的， 为了实现什么任务
2. **数据来源**： 源码获取渠道、数据集类型、数据集来源
3. **运行环境**： 运行环境、实验工具、第三方库
4. **运行结果**： 能否运行成功， 结果是啥
5. **如何实现**： 代码整体架构， 每部分实现细节



# 文件夹说明
## [NLP](https://github.com/zhongqiangwu960812/ReadPapaers/tree/master/NLP)
这里面主要是存放NLP领域的一些papers， 包括NLP的基础知识， Attention等
## [SeaSurfaceTemperature](https://github.com/zhongqiangwu960812/ReadPapaers/tree/master/SeaSurfaceTemperature)
这里面主要是存放海表温预测相关的一些papers
## [RecommendSystem](https://github.com/zhongqiangwu960812/ReadPapaers/tree/master/RecommendSystem)
这里面存放推荐系统相关的一些papers
## [SpatiotemporalSeriesPrediction](https://github.com/zhongqiangwu960812/ReadPapaers/tree/master/SpatiotemporalSeriesPrediction)
这里面存放时空序列预测相关的一些papers
## [POIRecommend](https://github.com/zhongqiangwu960812/ReadPapaers/tree/master/POIRecommend)
这这里面存放POI推荐的一些papers




# 格式说明
每一个文件夹里面存放相应专题的论文， 并配有一个README.md说明文档， 该说明文档是对文件夹下色所有文章的一个简介， 以后用统一的一个整理格式（之前的文章不做要求了）
* 简介： 这里面说明文章是哪一年发表到哪里作者是谁
* 内容： 这里面主要回答三个问题， 这篇文章解决了什么样的问题？ 是怎样解决的？ 最后的结果是什么？
* 借鉴： 这里面是文章可以借鉴的一些内容， 比如写作技巧， 论证技巧， 思路方法等
* 链接： 对于精读的论文会从博客上详细整理一遍， 这里会发出链接
* 复现代码： 如果是非常重要的模型， 会尝试去复现， 这里是复现代码的链接

为什么要这么整理？  因为这么整理以后搜索论文的时候会非常方便， 首先下get到论文是关于什么专题的 然后直接就可以去找该文件夹下的README.md文档， 就可以获取文章的主要内容， 然后对于再基于感兴趣的内容去读相应的paper即可。 还有一点要说明的是**这里面的这些论文我都已经做了笔记， 可能不适合直接读， 所以建议是如果找到有合适主题的文章， 可以根据题目去搜索原论文**， 当然后面阅读记录的时候， 我会把标题的链接转到原论文上。


