### Todo

- [ ] Recurrent neural network regularization （RNN Regularzation，dropout不能很好的working在RNN里，不知道pytorch的rnn有没有整合这个技术，如果没有我可以自己编码进去）
- [ ] Distilling the knowledge in a neural network（将多个模型集中到一个模型，不过这个是收尾时候的工作了）
- [ ] Convolutional, long short-term memory, fully connected deep neural networks（CLDNN，比起分开的CNN，LSTM，DNN要高出4～6%的精度；要说能不能考虑当然是能考虑，只是作者必然也已经考虑了就是）
- [ ] A neural conversational model （会话建模是什么？我只关心这个）
- [ ] Sentence compression by deletion with lstms （通过训练神经网络进行token删除，能得到什么？好奇。如果能自动句子剪枝岂不是挺好的？可以先过一下这个系统再转成embedding）
- [ ] Multi-task sequence to sequence learning （多任务总比单任务好，就像sector v2那样；我可以考虑一下后续引入什么多任务操作）
- [ ] Towards principled unsupervised learning（被引数比较少，大意是引入了一个新的loss function，可以提高非监督学习的精度；看一下没准能启发非监督学习）
- [ ] Matching networks for one shot learning （从少量数据学习，提出的学习方法非常有意思；优先学习，一是因为它自信满满，二是因为能提高迭代速度）
- [ ] Contextual lstm (clstm) models for large scale nlp tasks (不管怎样，提到了topic，必看不可)
- [ ] Google's neural machine translation system: Bridging the gap between human and machine translation (虽然是机器翻译，但是至少是S2S，而且是大规模成功的系统；更加重要的是用了coverage loss function，这个可以看一下引了什么前置研究)
- [ ] Neural discrete representation learning　（用VAE整离散化表示）
- [ ] Bayesian recurrent neural networks (贝叶斯RNN，似乎能减少大量参数量和提高训练精度；因为我是用BiLSTM所以后续优化可能会用到这个)
- [ ] A hierarchical latent variable encoder-decoder model for generating dialogues (群友推荐的，看看；虽然是问答，但是跟NLG相关)
- [ ] Representation learning with contrastive predictive coding (预测接下来会出现的序列，就会学习到一个……；其实我不是很懂，不过很多人引用就考虑看看吧，是VAE一系的)
- [ ] Deep Sets
- [ ] Toward fast and accurate neural discourse segmentation (LSTM+CRF+ELMO)
- [ ] EDA: Easy data augmentation techniques for boosting performance on text classification tasks. (谷歌research说要实验的，那我也得看看把)
- [ ] Does label smoothing mitigate label noise? (谷歌research说要实验的，那我也得看看把)
- [ ] Convolutional sequence to sequence learning. （在S2S上使用卷积，2017，可以看，主要是pos embedding）
- [ ] Interpreting Pretrained Contextualized Representations via Reductions to Static Embeddings (contextualized representation -> static embedding， 我本来是想看看有没有加快bert的方法的，但是contextual注定是要fine-tune的吧。static embedding可以用来做通用embeding。。对)
- [ ] Comparing Transformers and RNNs on predicting human sentence processing data (RNN和TF的比较研究，有必要看，马上看）
- [ ] Skip rnn: Learning to skip state updates in recurrent neural networks (关于神经网络的可能性)
- [ ] Compressive Transformers for Long-Range Sequence Modelling (Compressive Transformer, which compresses past memories for long-range sequence learning) (解决长序列问题 No.1)
- ~~Generating Long Sequences with Sparse Transformers (似乎是一种特殊的 attention机制，将复杂度从n^2变成了比较低的，虽然比起线性还是差点。那我为什么不直接看线性？ 总之有兴趣的话可以看下。。) (解决长序列问题 No.2) (没必要看了因为Reformer是更好的选择)~~
- [ ] Transformer-XL 应该是我想要找的了 (解决长序列问题 No.4)
- [ ] On the relation- ship between self-attention and convolutional layers (CNN和TF的关系论)
- [ ] Adaptive Sampled Softmax with Kernel Based Sampling (Linear Transformer Bases)
- [ ] Set Transformer
- [ ] 关于句子embedding
  - [ ] Skip Thought
  - [X] Distributed Representations of Sentences and Documents (paragraph vector) (必看，static sentence embedding) (将word embedding冻结，然后通过预测来获得句子embedding，还行，可以考虑下，如果比LSTM更好的话，总是值得使用的)
  - [X] Generating sentences from a continuous space (感觉效果还可以，它好像catch住了很多语意信息，我觉得这个相当有潜力，是我的兴趣所向)
- [ ] TransGAN: Two Transformers Can Make One Strong GAN (趋势)

### GAN vs VAE

- [ ] 必须被填补的空白领域
- [ ] Variational Recurrent Auto-Encoders (这个似乎很好实现，结合Generating sentences from a continuous space的图来看)


### Done

- [X] Text Segmentation by Cross Segment Attention 
- [X] Long range arena
- [X] What Do Position Embeddings Learn (为了实验vanila TF，快速过一遍)
- [X] A SIMPLE BUT TOUGH TO BEAT BASELINE FOR SENTENCE EMBEDDINGS (BERT一亿参数太慢了，看看要不要用word2vec来整) (唯一明白的就是自己看不懂统计学方法，你妈的有神经网络还要个鸡巴统计学啊，所以才会被bert打的要死啊，看看bert有没有用到word2vec再说。。后续直接用RNN)
- [X] Adaptive Computation Time for Recurrent Neural Networks (在每个timestep，再纵向运算1到n次，相当于可以多思考一会儿。大概概念就是这样，但是式子有些麻烦就没看)
- [X] Universal transformers (将RNN和TF的优点结合，必看) （根本不是我想的那样，就是ACT在TF上的应用，草）
- [X] What you can cram into a single $&!#* vector: Probing sentence embeddings for linguistic properties (相当不错一个解剖研究，facebook整的，主要是看看那几个probing task，不知道会有什么)
- [X] Probing Neural Dialog Models for Conversational Understanding (21.2.16) （emm，没有什么突出成果。思考：首先我认为句子跟embedding跟QA是有很大联系的，所以第一算是了解了一些目前存在的QA Dataset，GLUE里边可以找到常识推理的数据集。然后思考可以往日语sentence probing方向发展一下）
- [X] GLUE: A Multi-Task Benchmark and Analysis Platform for Natural Language Understanding (怒看，直接把facebook那个探测给翻了) (21.2.16) 只有三页，主要是有线上bench mark，要学会用起来
- [X] 解剖Transformer
  - [X] A Unified Understanding of Transformer's Attention via the Lens of Kernel (核函数，SVN之类的是我的盲点阿) (周六花了一天肝完，必须说是受益匪浅，核函数什么的补全了，然后decoder的位置embedding也明白多了，但是这只是一个节点，接下来看RNN TF)
  - [X] Transformers are RNNs: Fast Autoregressive Transformers with Linear Attention (解决长序列问题 No.3) (顺便从RNN角度解剖TF)
