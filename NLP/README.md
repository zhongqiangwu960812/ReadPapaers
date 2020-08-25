# 论文拾贝

## [1.	Distributed Representations of Words and Phrases and their Compositionality](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/NLP/distributed-representations-of-words-and-phrases-and-their-compositionality.pdf)
* **简介**： 2013年10月谷歌研究室的一篇文章
* **内容**： 提出了单词的分布式表示方法，这篇文章主要是提出方法学习词嵌入，
真正的实现wordtovec。 提出了skik-gram模型，负采样的方式等学
习词嵌入。
* **借鉴**： 这篇文章读起来挺晦涩难懂的，但是负采样的学习词嵌入的方式，
skipgram模型等值的借鉴， 在Pytorch课程中也实现了这个模型，
主要是弄懂这里的思想即可。这篇文章没有深入的读。
## [2.	Attention is all you need](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/NLP/attention%20is%20all%20you%20need.pdf)
* **简介**： 2017年谷歌团队发表的一篇文章。
* **内容**： 这篇文章最大的亮点就是提出了一种Transformer的结构，这种结构
呢，是完全依赖注意力机制来刻画输入和输出之间的全局依赖关系，
而不使用递归运算的RNN网络了。这样的好处就是第一可以有效的
防止RNN存在的梯度消失的问题，第二是允许所有的字全部同时训
练（RNN的训练是迭代的，一个接一个的来，当前这个字过完，才可
以进下一个字），即训练并行，大大加快了计算效率。Transformer使
用了位置嵌入来理解语言的顺序，使用了多头注意力机制和全连接
层等进行计算，还有跳远机制，LayerNorm机制，Encoder-Decoder
架构等，我感觉这里面比较重要且难以理解的就是Multi-Head 
Attention机制
* **借鉴**： 这篇文章最大的借鉴就是Attention的思路，现在也是用的超级多，
什么空间Attention，时间Attention等。 这篇文章在自然语言处理领
域也可以算的上经典之作，有了它，才打破了NLP里RNN的神话，
后面的BERT，ALBERT等都是这个基础上建立的模型。
* **链接**： [https://blog.csdn.net/wuzhongqiang/article/details/104414239](https://blog.csdn.net/wuzhongqiang/article/details/104414239)
