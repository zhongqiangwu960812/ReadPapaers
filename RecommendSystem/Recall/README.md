# 论文拾贝

## 1. [Item-to-Item Collaborative Filtering_2003](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/Item-to-Item%20Collaborative%20Filtering_2003.pdf)

* **简介**： 这是2003年来自亚马逊的一篇文章
* **内容**： 提出了Item-to-Item协同过滤算法， 也就是物品与物品之间的协同过滤， 通过计算物品之间的相似度对用户来进行推荐， 相比较于用户之间的协同过滤， 适合在线推荐商品， 且在线计算复杂度会低很多。 本篇论文主要是描述了一下传统的协同过滤方法的原理， 像用户的协同过滤， 聚类的模型， 搜索的模型等， 然后通过分析他们的一些不足引出了Item-to-Item算法， 并进行了原理的解释，最后和已有的算法进行了对比。
* **借鉴**： 这篇文章提出的协同过滤推荐算法正式被用于在线推荐， 是推荐系统领域比较重要的一篇论文
* **链接**： [AI上推荐 之 协同过滤](https://blog.csdn.net/wuzhongqiang/article/details/107891787)

## 2. [Factorization-Machines_2010](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/Factorization-Machines_2010.pdf)

* **简介**： 这是2010年的一篇文章
* **内容**： 为了解决二阶多项式交叉算法无法在很稀疏的数据集上表现很好的问题， 提出了因子分解机模型FM， 该模型是把二阶多项式交叉特征前面的单独系数通过隐向量内积的形式表现了出来， 综合考虑了已有的所有数据。 首先是为每个特征学习一个隐向量， 然后把隐向量的内积作为两两交叉特征前面的权重， 相比较于Poly2来说， 这种方式在稀疏数据集上表现比较好。 本论文首先是阐述了FM的原理， FM的公式推导和训练方式， 然后对比了FM和SVM（采用核的思想对特征进行交叉）。这些方式与逻辑回归的区别就是特征与特征之间增加了交互信息。
* **借鉴**： 这篇文章的FM模型也是非常重要的一个模型了， 在传统的推荐算法中也是非常重要， 这种思想可以延续到深度学习领域的隐向量embedding。
* **链接**：[AI上推荐 之 逻辑回归模型与GBDT+LR](https://blog.csdn.net/wuzhongqiang/article/details/108349729)

##  3. [NeuralCollaborativeFiltering_2017](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/NeuralCollaborativeFiltering_2016.pdf)
* **简介**： 这是2017年来自新加坡国立大学的一篇文章
* **内容**： 这篇文章在传统的协同过滤的基础上进行了改进， 把神经网络引入进了深度学习， 提出了深度协同过滤(NeuralCF)模型，这个模型是GMF和MLP的一个组合模型， GMF就是矩阵分解的泛化模型， 这个依然是保留了MF内积的线性运算。而MLP就是在传统MF的思路基础上， **把内积运算用多层的感知机进行了替换**， 以增强非线性表达和更深层次的交叉， 学习到更多的信息。这一个线性， 一个非线性最后又组合了起来得到最终的NeuralCF模型。 这篇文章介绍了GMF模型， MLP模型， 以及它俩的融合， NeuralCF模型的计算过程， 然后就是在两个真实数据集上进行了实验。  
* **借鉴**： 这个模型涉及到的技术也比较基础，思路不是很复杂， 所以也比较利于学习， 涉及的特征只有用户和物品的交互信息， 也就是用户向量和物品向量， 没有其他的特征在里面， 而处理过程，就是通过embedding得到各自的隐向量， 然后各自的隐向量进入不同的模型进行计算。   借鉴的地方就是人家的实验部分抛出了四个问题， 然后一一解决， 非常全面， 还有就是pre-training的思路。 这篇文章感觉质量还是很不错的。读起来， 要比前面的轻松。
* **链接**： [AI上推荐 之 NeuralCF与PNN模型(改变特征交叉方式）](https://blog.csdn.net/wuzhongqiang/article/details/108985457)

## 4. YouTubeDNN

* 简介：2016年YouTube工程师写的工业界的一篇经典好文
* 内容: 从一个宏观的层面讲述了推荐系统架构， 介绍了召回模型和精排模型， 并且基于业务场景介绍了很多工程性的经验
* 借鉴：这篇paper里面，主要是一些经验点， 非常重要， 这个具体总结到了博客里面
* 链接: [AI上推荐 之 YouTubeDNN模型(工业界推荐系统的灯火阑珊)]([AI上推荐 之 YouTubeDNN模型(工业界推荐系统的灯火阑珊)_Miracle8070-CSDN博客](https://blog.csdn.net/wuzhongqiang/article/details/122671511?spm=1001.2014.3001.5501))

# 模型复现

大部分模型复现和详细的解释可以参考这个GitHub项目：[https://github.com/zhongqiangwu960812/AI-RecommenderSystem](https://github.com/zhongqiangwu960812/AI-RecommenderSystem)