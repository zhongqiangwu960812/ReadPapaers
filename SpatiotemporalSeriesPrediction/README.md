# 论文拾贝：


## [1. Convolutional LSTM Network：A Machine Learning Approach for Prediction Nowcasting](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SpatiotemporalSeriesPrediction/Convolutional%20LSTM%20Network2015.pdf)
* **简介**： 2015年发表在Nips上的一篇文章
* **内容**： 提出了ConvLSTM网络结构用于时空序列预测问题，这种结构善于捕捉空间相关性，就是FCLSTM的全连接的运算变成了卷积运算，这样就可以用一种结构来捕捉时空特征。并且提出了一种Encoding-
Forecasting Structure结构：类似Encoding-Decoding Structure，把编码和预测分开，互不影响。
* **借鉴**： 这个网络结构的思路可以借鉴，因为时空序列的预测这块，空间和时
间特征同样重要，这是时空序列预测的里程碑之作，第一次实现了网
络同时捕捉空间和时间特征。
* **链接**： [https://blog.csdn.net/wuzhongqiang/article/details/104330425](https://blog.csdn.net/wuzhongqiang/article/details/104330425)
## [2. PredRNN: Recurrent Neural Networks for Predictive Learning using Spatiotemporal LSTMs](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SpatiotemporalSeriesPrediction/predrnn-nips17.pdf)
* **简介**： 2017年发表在Nips上的一篇文章
* **内容**： 提出了一种新的端到端的结构PredRNN， 允许属于不同LSTMS的单元跨层交互。设计了一种新的时空LSTM（ST-LSTM）单元，它在一个统一的记忆单元中记忆空间和时间特征，并在垂直层面和水平层面
上传递记忆。这种单元是PredRNN的关键部分。最后再视频预测和运动数字，雷达回波预测数据集上做的实验，证明了这种结构的效果很原来的好了很多。
* **借鉴**： 这个网络结构的思路可以借鉴，这篇文章是在ConvLSTM的基础上进行改进的一个版本，ConvLSTM上次说到存在的问题是记忆状态被限制在每个ConvLSTM层并且只能水平传递（时间域内进行更新），层
与层之间的记忆单元是相互孤立的，这样带来的一个问题就是底层会完全忽略顶层在之前的时间步骤中所记忆的内容。 所以本文对这个问题进行了改进，这个网络架构我觉得不错。
* **链接**： [https://blog.csdn.net/wuzhongqiang/article/details/104348099](https://blog.csdn.net/wuzhongqiang/article/details/104348099)
## [3. PredRNN++: Towards A Resolution of the Deep-in-Time Dilemma in Spatiotemporal Predictive Learning](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SpatiotemporalSeriesPrediction/Predrnn%2B%2B%20-2018.pdf)
* **简介**： 2018年发表在ICML上的一篇文章
* **内容**： 提出了一种新的单元Casual LSTM(时空记忆单元的级联操作)，这种单元可以层次不变的情况下，增加更多的非线性操作，使得特征会放大，这样更有利于捕捉短期动态变化和突发情况，但带来的问题仍然
是梯度消失。所以又提出了GHU（梯度高速公路单元），直接类似于一条高速公路在时间中穿梭，把历史和未来相连，这样前面时间步中的重要的特征可以不经历漫长的之字形或者记忆单元传播，而是直
接通过高速公路相传，这样在反向传播的时候更容易保留下梯度。解决了梯度消失的问题。所以上面提出的两种单元，能够自适应的捕捉长期和短期的特征， 也能够建立很深的网络进行学习。 
* **借鉴**： 这个网络结构的思路可以借鉴，这篇文章是在PredRNN的基础上进行改进的一个版本，上次说过，PredRNN结构效果挺好，但是也存在问题，就是梯度消失，尤其是那个之字形流动的那个，层数一多，时间
一长，就容易梯度消失，不擅长捕捉深层次网络的长期特征。所以本文对这个问题进行了改进。
* **链接**： [https://blog.csdn.net/wuzhongqiang/article/details/104451925](https://blog.csdn.net/wuzhongqiang/article/details/104451925)
## [4. EIDETIC 3D LSTM: A MODEL FOR VIDEO PREDICTION AND BEYOND](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SpatiotemporalSeriesPrediction/Eidetic_3d_lstm.pdf)
* **简介**： 2018年发表在ICML上的一篇文章
* **内容**： 提出了一种新的时空序列学习的网络结构E3D-LSTM，该结构加入了self-Attention机制，把当前单元的状态记忆特征与前面某段时间的状态进行了一种关联，并让网络自己学习前面某段时间状态对当前的
影响权重，这样，拓展了时间维度，可以更好捕捉长期的帧交互，使得长期表征学习成为可能。即使在长时间的干扰之后，也可以通过多个时间戳来回忆所存储的记忆。为了达到对学习短期依赖和长期表征的一个均衡控制，改变了LSTM的更新门操作，引入了一种
RECALL机制来改善记忆状态的递归转移函数，即当前的记忆状态更新取决于当前的输入和前一步的隐态，还取决于前一步记忆和过去某段时间的记忆的融合。提出了自我监督的辅助性学习，就是把帧
预测和行为识别的任务合成一块，因为行为识别的任务需要记住更多过去的细节，而帧预测正好是记住了过去的细节去预测未来，所以后者可以作为前者的一种辅助，并且采用了迭代衰减系数来保证两
个任务之间完成转移。
* **借鉴**： 这个网络结构的思路可以借鉴，是时空序列预测模型的第四篇，这篇文章提出的EIDETIC 3D LSTM网络是继ConvLSTM, PredRNN, PredRNN++网络的更加高级的一个网络，前边的三个网络的普遍特
征时只能捕捉前面单个时间步某个单元的状态的特征， 而E3D-LSTM拓展了时间维度，可以捕捉长期的帧交互，这个想法的来源就是Attention。
* **链接**： [https://blog.csdn.net/wuzhongqiang/article/details/104584892](https://blog.csdn.net/wuzhongqiang/article/details/104584892)
## [5. Memory In Memory：A Predictive Neural Network for Learning Higher-Order-Non-Stationary from Spatiotemporal Dynamics](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SpatiotemporalSeriesPrediction/MemoryInMemory.pdf)
* **简介**： 2019年发表在cvpr上的一篇文章
* **内容**： 这次的这个网络是为了解决时空序列中的非平稳的问题，非平稳是没有规律的，所以为了捕捉时空序列中的非平稳信息，提出了MIM网络，这种网络是在ST-LSTM的基础上对遗忘门进行了改进， 因为在
原来的模型工作过程中， 遗忘门百分之80处在饱和状态，这样的话模型只能记住平稳的信息，所以这里把遗忘门换成了两个级联的自更新的LSTM模块。MIM块利用相邻重复态之间的差分信号，通过
两个级联的、自更新的记忆模块来模拟时空动力学中的非平稳和近似平稳特性。 任何一个非平稳的过程都可以分解为确定项+时间变
量多项式+零均值随机项， 而差分的转换，使得非平稳近似转成平稳项。 MIM提出了一个state可以提取到高阶非平稳特征， 基于MIM又提出了一个新的RNN结构 然后就是RNN结构的堆叠。
* **借鉴**： 我觉得这里的这个结构也可以借鉴一下，因为海洋的环境类似于降雨量的那个，肯定是存在波动和非平稳性，所以模型应该尽量的捕捉到非平稳性的信息， 然后再加上Attention，就更加完美了。 这一篇
文章算是PredRNN上的一个改进。
* **链接** ： [https://blog.csdn.net/wuzhongqiang/article/details/108218338](https://blog.csdn.net/wuzhongqiang/article/details/108218338)	
