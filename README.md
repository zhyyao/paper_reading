# Paper Reading of the speech and text pretraining
## Simple intro
This repositories is a collaction of the __recent paper__. I am a beginner research of speech and text pretraining and robust speech recognition. I will put the worthy reading paper here and do a conclusion of different paper.
后面嫌麻烦就用中文了

## Paper list
### Speech pretraining
* [HuBERT: Self-Supervised Speech Representation Learning by Masked Prediction of Hidden Units](https://arxiv.org/abs/2106.07447)
> __Google__
> 
> 这篇应该无人不知无人不晓吧，使用聚类方法生成pseudo label来进行预训练，同时也借鉴wav2vec系列论文使用mask方法来进行预训练，论文中解释：mask 方法可以让网络学习语音的表征，predict pseudo label可以让模型学习一个时域上上下文的关系，并且两个目标是一致的，这种一致性也是模型能够成功的原因之一。


## pretraining
* [data2vec: A General Framework for Self-supervised Learning in Speech, Vision and Language](https://arxiv.org/abs/2202.03555)
> __Meta AI__
> 
> 这篇是是一篇有启发性的文章，但是其模型训练难度非常大需要细调，介绍了一种general的训练方式，使用unmask的输入做为teacher去指导mask的输入，并且将mask输入模型的top N层拿出来做average作为student的标签，有点像不会做完型填空的我，在看着答案想我为啥这里选A，哈哈哈。另外teacher 在训练时也是有梯度的，其梯度和student的梯度进行了一个加权和。不过这篇论文只在三个领域内各自训练，跨领域估计很难收敛吧
