### Clustering

* No50 [2020/6 Learning To Classify Images Without Labels (Paper Explained)](https://www.youtube.com/watch?v=hQEnzdLkPj4&ab_channel=YannicKilcher) 一个新的clustering算法SCAN，在没有label的情况下都能达到很好的训练效果。主要流程是，首先用Transform来对图片做处理，然后用CNN来获取处理前后图片的latent representation，并努力缩减两者间的欧几里得距离，以此训练神经网络a。然后通过a把所有数据压缩到latent representation，以此弄成新的数据集，然后每个图片跟最邻近的5个图片作为一组用来训练神经网络b，b输出的结果是softmax，努力让结果一致就完了
* No51 [2016 Unsupervised learning of visual representations by solving jigsaw puzzles] 将图片切成小块，然后重新拼回来，自监督算法。主要是No50有用到。Q：难道不会只学到边缘贴合算法？
* [2016 Context Encoders: Feature Learning by Inpainting](https://arxiv.org/abs/1604.07379) Inpainting跟AutoEncoder的区别在于后者是整块图片而前者只是图片中的一部分，他们称之为Context Encoder。主要是No50有用到，这个就是bert的灵感来源，我猜。
* [2016 Colorful Image Colorization](https://arxiv.org/abs/1603.08511) 自监督，去色，上色。主要是No50有用到。问题是NLP怎么去掉颜色？
* No52 [2018 Deep clustering for unsupervised learning of visual features](https://arxiv.org/abs/1807.05520)，deep cluster之前大部分都是在固定的representation上使用k-means。facebook ai出品。


### Summarization
* No53 [2020 Extractive Summarization as Text Matching](https://arxiv.org/abs/2004.08795)，我的研究计划书的灵感来源，通过将句子的representation和整个document的相比较进行句子抽出。
* No54 [2019 Sentence-bert](https://arxiv.org/abs/1908.10084) 历史：过去的practice有用第一个token来作为输出或者用「bert embedding」的手法来获取sentence embedding，但是甚至比Glove embedding还要差。性能：计算10,000个句子的embedding要5秒，然后计算相似度0.01秒。实现：其中两个手法跟前面的practice一致，一个是cls，一个是mean，一个是max，共三个策略。）还得补triplet network。

### Translation

* [2019/4 Neural Text Degeneration](https://arxiv.org/abs/1904.09751) 1）自然语言理解质量高可是一旦生成就低质量是反直觉的 2）Decoding strategies alone have dramatical effect 3）提出了Necleus Sampling， （2021/1/4）做指针网络碰到了反复输出同个指针的问题，就到网上找seq2seq repeat，然后就找到这个，现在不知道有多少帮助，不过至少是影响力很大的一篇论文，然后我也确实在整decoding问题，然后指针网络和生成词语的区别其实就是动态非动态的区别，总该有帮助的，从最新的成果回溯总是好的，先看看吧。
* [2020/3 Decoding Strategies](https://huggingface.co/blog/how-to-generate) 只是博客，Beam Search可以看看 

### RL

* [2018/4 World Models](https://www.youtube.com/watch?v=dPsXxLyqpfs&ab_channel=YannicKilcher) 因为每次都要调动simulator的话，训练会变得太昂贵（等等，这里用replay buff不就能解决了？），所以他们决定训练一个model去模仿simulator的逻辑。具体做法是VAE来压缩图片，这个只是优化用，用RNN来预测下一帧的动作才是重点。相当于对世界的逻辑建模

### QA

* [2020/8 REALM](https://www.youtube.com/watch?v=lj-LGrnh1oU&ab_channel=YannicKilcher) 其实我不是很懂这个，白看了，对这个不熟。总的来说就是把整个资料库用来pretrain一个document retriver，然后来回答问题。又是一个大突破只能这样说。应用方面我想想，首先要有一个完善，不变的资料库，话说真的是不能变么？也许不一定，emm，我还是不评价了

### Topic Segmentation

* No55 [2017 word embedding methods in topic segmentation] 找到这个关键词以来看的第一篇文章，原来在2017之前topic segmentation还那么落后的吗？总之看了论文的abstract，Overview on topic segmentation这一部分还可以，可以作为以后论文的参照。1. 没有用到神经网络的 2. 就连词语变换都是用的传统方法，连word2vec都没有用。
* No56 [2019 Sector](https://www.mitpressjournals.org/doi/abs/10.1162/tacl_a_00261) 去年的论文，应该是最有参考价值的了。基本看了一遍，步骤大概是，1）用word2vec+distributional sentence representation来建模句子 2）用双向LSTM来建模Topic 3）classfication，用固定数量的外部标签来判断正确与否，softmax+onehot 4）用每个句子的分类准确度来判断分数。
* [2015/6 Pointer networks] 说实话一直对这个模型的灵活性很佩服，可是现在（2021/1/4）因为用到所以重读了一遍发现: 1) 原本的精度就不高（train50，test50，精度72.6%） 2）他们测试的时候限制了输出数量，所以能跟LSTM作对比
