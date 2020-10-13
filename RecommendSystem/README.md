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

## 3. [Field-aware Factorization Machines_2015](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/Field-aware%20Factorization%20Machines_2015.pdf)

* **简介**： 这是2015年基于FM改进的一篇文章， 提出的模型在多项CTR大赛中夺得冠军， 并被Criteo、美团等公司深度应用
* **内容**：这个是在FM的基础上引入了特征域感知的概念， 上面的FM模型在学习隐向量的过程中， 综合考虑了所有特征域里面的隐向量， 也就是每个特征值只学习到了一个隐向量， 这样在进行两两特征交互的时候， 用的是他们的内积。 而FFM在这个基础上进行了改进， 认为不同的特征域里面的隐向量不应该相同， 所以**FFM为每个特征值学习了f个隐向量， 这里的f就是特征域的个数。 针对不同特征域里面的特征与某个特征值交叉会使用不同的隐向量进行内积作为交叉的权重**。 这里论文里面考虑的就是交互的时候， 由于交互特征属于不同的域， 统一用相同的隐向量进行计算可能不太合理， 比如(EPSN, Nike)和(EPSN, Male), 对于出版社EPSN来说， 与广告商Nike和性别的交互， 如果是FM， EPSN会是一个隐向量， 而FFM的话， 会分别针对广告商属性和性别属性学习两个隐向量， 这样交互的时候， 前面那个用广告属性的隐向量， 后者用Male的隐向量， 这样可能会合理一些。毕竟广告商和性别相差比较大， 统一学习的话效果不太好。  这篇论文的创新就是FFM， 先介绍了FM的不足， 引出FFM模型， 然后介绍了FFM模型的原理， 训练方式， 最后实验过程探索了一些超参数， 训练方式的影响， 以及速度方面， 和其他模型的比较， 不同数据集的实验等。
* **借鉴**： 这篇论文可以感觉人家的实验设计挺全的， 一读就是做了很多工作， 所以自己写论文的时候也要考虑全面性
* **原理解释**： [AI上推荐 之 FM和FFM](https://blog.csdn.net/wuzhongqiang/article/details/108719417)


## 4. [facebook-GBDT-LR_2014](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/facebook-GBDT-LR_2014.pdf)

* **简介**： 这是2014年来自Facebook的一篇文章
* **内容**： 针对FM没法进行更高阶特征交互的问题， 提出了GBDT+LR模型可以用来更高阶特征之间的交互， 并且把特征工程推向了自动化处理， 之前的那些模型， 特征工程大部分全是靠人工处理， 而该篇论文的模型提出之后， 使得模型自动的交叉组合特征， 然后进行预测工作， 节省了很多人力和人工干预。 本篇论文依然是讲了GBDT+LR模型的架构和工作原理， 然后大部分时间都是在实验， 从实践的角度进行梳理这篇文章， 探索了具体实践过程中的一些细节。
* **借鉴**： 这篇文章后面的实践部分没有细读， 详情可以参考下面这篇文章。

* **链接**：[GBDT+LR](https://blog.csdn.net/Yasin0/article/details/100737222)
* **原理解释**： [AI上推荐 之 逻辑回归模型与GBDT+LR](https://blog.csdn.net/wuzhongqiang/article/details/108349729)


## 5. [DeepCross_2016](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/DeepCross_2016.pdf)
* **简介**： 这是2016年来自微软的一篇文章
* **内容**： 这篇文章提出了DeepCrossing的网络模型， 这个模型是第一次把深度学习应用于推荐系统的工程实现， 解决了从特征工程、稀疏向量稠密化、多层神经网络进行优化目标拟合等一系列深度学习在推荐系统的应用问题，为后面的模型打下了良好的基础， DeepCrossing模型应用场景是微软搜索引擎Bing中的搜索广告推荐， 用户在输入搜索词之后， 搜索引擎除了返回相关结果， 还返回与搜索词相关的广告，Deep Crossing的优化目标就是预测对于某一广告， 用户是否会点击， 依然是点击率预测的一个问题。这个模型的具体结构可以参考下面的链接。具体实验部分没仔细看。
* **借鉴**： 这个模型涉及到的技术比较基础，在传统神经网络的基础上加入了embedding， 残差连接等思想， 且结构比较简单， 对初学者复现和学习都比较友好。
* **链接**： [DeepCross文章导读](https://mp.weixin.qq.com/s/WXnvkoRFxwFpflStAuW7kQ)
* **原理解释**： [AI上推荐 之 AutoRec与Deep Crossing模型](https://blog.csdn.net/wuzhongqiang/article/details/108948440)

## 6. [NeuralCollaborativeFiltering_2017](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/RecommendSystem/NeuralCollaborativeFiltering_2016.pdf)
* **简介**： 这是2017年来自新加坡国立大学的一篇文章
* **内容**： 这篇文章在传统的协同过滤的基础上进行了改进， 把神经网络引入进了深度学习， 提出了深度协同过滤(NeuralCF)模型，这个模型是GMF和MLP的一个组合模型， GMF就是矩阵分解的泛化模型， 这个依然是保留了MF内积的线性运算。而MLP就是在传统MF的思路基础上， **把内积运算用多层的感知机进行了替换**， 以增强非线性表达和更深层次的交叉， 学习到更多的信息。这一个线性， 一个非线性最后又组合了起来得到最终的NeuralCF模型。 这篇文章介绍了GMF模型， MLP模型， 以及它俩的融合， NeuralCF模型的计算过程， 然后就是在两个真实数据集上进行了实验。  
* **借鉴**： 这个模型涉及到的技术也比较基础，思路不是很复杂， 所以也比较利于学习， 涉及的特征只有用户和物品的交互信息， 也就是用户向量和物品向量， 没有其他的特征在里面， 而处理过程，就是通过embedding得到各自的隐向量， 然后各自的隐向量进入不同的模型进行计算。   借鉴的地方就是人家的实验部分抛出了四个问题， 然后一一解决， 非常全面。 这篇文章感觉质量还是很不错的。读起来， 要比前面的轻松。
* **链接**： 这个等整理完了具体的再放


# 模型复现
大部分模型复现和详细的解释可以参考这个GitHub项目：[https://github.com/zhongqiangwu960812/AI-RecommenderSystem](https://github.com/zhongqiangwu960812/AI-RecommenderSystem)
