# 论文拾贝

## [1.	A CFCC-LSTM Model for Sea Surface Temperature Prediction](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SeaSurfaceTemperature/A%20CFCC-LSTMF%20MODEL%20FOR%20SEA%20SURFACE%20TEMPERATURE%20PREDICTION.pdf)
* **简介**： 2018年2月份发表在IEEE地球科学和遥感通讯的一篇文章。
* **内容**：这篇文章把海洋预测问题看成了一个时间序列的预测问题，并且采用了卷积和FCLSTM结合的模型进行该问题的解决，先用卷积网络提取
空间特征，然后FCLSTM获取时间特征，这样该模型就可以同时捕获温度的时空特征并进行预测。
* **借鉴**： 空间特征使用卷积，时间特征使用LSTM，两个海洋温度的数据集可以借鉴一下，然后Introduction中对海洋温度预测任务的描述可以借
鉴， 评估指标的ACC也可以借鉴一下子，并不是只有什么均方误差之类的东西衡量模型。
## [2.	A spatiotemporal deep learning model for sea surface temperature field prediction using time-series satellite data](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SeaSurfaceTemperature/A%20spatiotemporal%20deep%20learning%20model%20for%20sea%20surface%20temperature%20field%20pediction.pdf)
* **简介**： 2019年发表环境模型与软件学报上的一篇文章。
* **内容**：这篇文章使用了ConvLSTM完成了海洋温度的预测，关于ConvLSTM的模型可以参考下面，ConvLSTM可以同时捕捉时间和空间的信息， 针
对海洋预测的问题正好。
* **借鉴**： 这一个可以借鉴一下人家的数据集，关于ConvLSTM和其他对比实验模型的一些参数设置，最后的评估标准，引入了皮尔逊系数来看看与过去的关联等， 实验结果的展示技巧和描述技巧，还用了高斯核函
数来对比完整性等，都可以借鉴。
## [3.	面向海表温大数据的时间序列预测技术研究（师哥的毕设论文）](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SeaSurfaceTemperature/1701846%20-%201230%E7%89%88.pdf)
* **简介**： 这是师哥的毕设论文， 2019年12月完稿。
* **内容**： 这是一个毕业设计的论文，所以做得就比较完善了，从研究背景，相关工作，理论基础到实验和结果等都有，师哥主要做得是单点中长期预测和区域中长期预测的问题，在单点中长期预测中，有一个挺好的
创新点就是用xgboost重新做了做了特征，实现了机器学习模型和深度学习模型的一个融合， 并且对于单点的预测，还考虑了周围点过去的一天未来一天的影响，这个点其实也挺好，在区域预测中，使
用了卷积和LSTM结合的方式进行预测，并且还加入了Attention的思想。
* **借鉴Z**： 师哥这个是我研究的一个基础，从背景相关工作到理论和代码，都是基础。
## [4.	Prediction of Sea Surface Temperature using Long Short-Term Memory](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SeaSurfaceTemperature/Prediction%20of%20Sea%20Surface%20Temperature%20using%20Long%20Short-Term%20Memory.pdf)
* **简介**： 2017年发表在IEEE地球科学和遥感通讯的一篇文章。
* **内容**：这篇文章使用了FC-LSTM实现的海洋温度的预测，感觉算是一篇比较老的文章了，所以只是泛读了一下。
* **借鉴**： 这个也有一些借鉴的地方，比如introduction的描述，最后实验的时候有个线上测试的思路，感觉挺不错的，就是提出的这个模型，如果来了新的数据集，可以在原来训练好的基础上接着进行训练而不
用从头开始，从而节省了很大的计算。
## [5.	PREDICTION OF SEA SURFACE TEMPERATURE IN THE SOUTH CHINA SEA BY ARTIFICIAL NEURAL NETWORKS](https://github.com/zhongqiangwu960812/ReadPapaers/blob/master/SeaSurfaceTemperature/PREDICTION%20OF%20SEA%20SURFACE%20TEMPERATURE%20IN%20THE%20SOUTH%20CHINA%20SEA%20BY%20NEURAL%20NETWORKS.pdf)
* **简介**： 2015的一篇文章。
* **内容**：这篇文章也是挺老的一篇文章了，用的多层感知机，并且好像不是预测的面的温度，而是数据点的温度。
* **借鉴**： 这个文章数据预处理的思路挺不错的，为了减少SST变化带来的预测误差，提出将海温时间序列数据分解为气候月平均值和月异常数据集，并建立两个神经网络模型。这两个模型的结合给出了最终的海温
预测结果。利用该方法对南海海温进行了预测。对于海温扰动比较大的地区，这种数据预处理的方式或许是一种可行的方式。老师上次不是说海温数据可能容易受到扰动影响吗？
