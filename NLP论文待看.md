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
- [ ] !6 Skip rnn: Learning to skip state updates in recurrent neural networks (关于神经网络的可能性)
- [ ] !5 Compressive Transformers for Long-Range Sequence Modelling (Compressive Transformer, which compresses past memories for long-range sequence learning) (解决长序列问题 No.1)
- ~~Generating Long Sequences with Sparse Transformers (似乎是一种特殊的 attention机制，将复杂度从n^2变成了比较低的，虽然比起线性还是差点。那我为什么不直接看线性？ 总之有兴趣的话可以看下。。) (解决长序列问题 No.2) (没必要看了因为Reformer是更好的选择)~~
- [ ] Transformer-XL 应该是我想要找的了 (解决长序列问题 No.4)
- [ ] On the relation- ship between self-attention and convolutional layers (CNN和TF的关系论)
- [ ] Adaptive Sampled Softmax with Kernel Based Sampling (Linear Transformer Bases)
- [ ] Set Transformer
- [ ] TransGAN: Two Transformers Can Make One Strong GAN (趋势)
- [ ] BERT
  - [ ] Linguistic knowledge and transferability of contextual representations (2019 ACL，解析BERT NO.1)
  - [ ] What do you learn from context? probing for sentence structure in contextualized word representations. (解析BERT NO.2)
  - [ ] Are sixteen heads really better than one? (解析BERT NO.3，关于不同的HEAD学到什么)
  - [ ] What bert is not: Lessons from a new suite of psycholinguistic diagnostics for language models. (解析BERT NO.4，心理语言学？)
  - [ ] BanglaBERT: Combating Embedding Barrier for Low-Resource Language Understanding (孟加拉语言bert vs 多语言bert；考虑用多语言bert来代替日语)
  - [ ] !4 Less is More: ClipBERT for Video-and-Language Learning via Sparse Sampling （稀疏数据bert，）
  - [ ] Bertscore: Evaluating text generation with bert. (解析BERT NO.5)
  - [ ] How contextual are contextualized word representations? comparing the geometry of BERT, ELMo, and GPT-2 embeddings.
- [ ] RNN 
  - [ ] Lossy-Context Surprisal: An Information-Theoretic Model of Memory Effects in Sentence Processing. (关于认知科学，有对标TF的野心)


### GAN vs VAE

- [ ] 必须被填补的空白领域


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
- [X] 关于句子embedding
  - [X] Skip Thought (确实很amazing，不知道和bert比会怎样)
  - [X] Distributed Representations of Sentences and Documents (paragraph vector) (必看，static sentence embedding) (将word embedding冻结，然后通过预测来获得句子embedding，还行，可以考虑下，如果比LSTM更好的话，总是值得使用的)
  - [X] Generating sentences from a continuous space (感觉效果还可以，它好像catch住了很多语意信息，我觉得这个相当有潜力，是我的兴趣所向)
- [X] Variational Recurrent Auto-Encoders (这个似乎很好实现，结合Generating sentences from a continuous space的图来看) (可是这是面向音乐生成方向的)
- [X] How multilingual is Multilingual BERT? (多语言BERT，看看能否替代日语bert) (非常有意思，但是为了验证『多语言模型更聪明』的假设，或许得回顾一下原来的论文)
- [X] !2 Interpreting Pretrained Contextualized Representations via Reductions to Static Embeddings (contextualized representation -> static embedding， 我本来是想看看有没有加快bert的方法的，但是contextual注定是要fine-tune的吧。static embedding可以用来做通用embeding。。对) (通过多语句平均池化可以获得static embedding，可是性能只是通过对比词语相似度来判断，关于static embedding还要进一步看其他论文)
- [X] !3 Comparing Transformers and RNNs on predicting human sentence processing data (RNN和TF的比较研究，有必要看，马上看） (一般般，没啥意思。主要知道了一个惊奇值Surprisal的概念，还有ENCOW数据集以及一些脑科学数据集，TF多层可以引入位置信息值得验证，让我想起排序项目)
- [X] OpenAI CLIP: ConnectingText and Images (Paper Explained) (看的视频，太强了，虽然我不是做图像处理。主要问题点是，普通的classfier很容易将同标签内所有输入的差异都忘掉，这个本质问题在自然语言处理里也是存在的……真是) (TODO： 仔细想想没搞懂怎么生成不同标签)
- [X] A Joint Model for Document Segmentation and Segment Labeling (Sector的后续文章，量子速读了主要是想知道他们怎么整joint loss，结果发现只是简单的相加)
- [X] 2020/6 Learning To Classify Images Without Labels (Paper Explained) (一个新的clustering算法SCAN，在没有label的情况下都能达到很好的训练效果。主要流程是，首先用Transform来对图片做处理，然后用CNN来获取处理前后图片的latent representation，并努力缩减两者间的欧几里得距离，以此训练神经网络a。然后通过a把所有数据压缩到latent representation，以此弄成新的数据集，然后每个图片跟最邻近的5个图片作为一组用来训练神经网络b，b输出的结果是softmax，努力让结果一致就完了) (相当于一个变种VAE)
- [X] [2016 Unsupervised learning of visual representations by solving jigsaw puzzles] 将图片切成小块，然后重新拼回来，自监督算法。主要是No50有用到。Q：难道不会只学到边缘贴合算法？
- [X] Context Encoders: Feature Learning by Inpainting Inpainting跟AutoEncoder的区别在于后者是整块图片而前者只是图片中的一部分，他们称之为Context Encoder。主要是No50有用到，这个就是bert的灵感来源，我猜。
- [X] 2016 Colorful Image Colorization 自监督，去色，上色。主要是No50有用到。问题是NLP怎么去掉颜色？
- [X] No52 2018 Deep clustering for unsupervised learning of visual features，deep cluster之前大部分都是在固定的representation上使用k-means。facebook ai出品。
- [X] No53 2020 Extractive Summarization as Text Matching，我的研究计划书的灵感来源，通过将句子的representation和整个document的相比较进行句子抽出。
- [X] 2019 Sentence-bert 历史：过去的practice有用第一个token来作为输出或者用「bert embedding」的手法来获取sentence embedding，但是甚至比Glove embedding还要差。性能：计算10,000个句子的embedding要5秒，然后计算相似度0.01秒。实现：其中两个手法跟前面的practice一致，一个是cls，一个是mean，一个是max，共三个策略。）还得补triplet network。
- [X] 2019/4 Neural Text Degeneration 1）自然语言理解质量高可是一旦生成就低质量是反直觉的 2）Decoding strategies alone have dramatical effect 3）提出了Necleus Sampling， （2021/1/4）做指针网络碰到了反复输出同个指针的问题，就到网上找seq2seq repeat，然后就找到这个，现在不知道有多少帮助，不过至少是影响力很大的一篇论文，然后我也确实在整decoding问题，然后指针网络和生成词语的区别其实就是动态非动态的区别，总该有帮助的，从最新的成果回溯总是好的，先看看吧。
- [X] 2020/3 Decoding Strategies 只是博客，Beam Search可以看看
- [X] 2018/4 World Models 因为每次都要调动simulator的话，训练会变得太昂贵（等等，这里用replay buff不就能解决了？），所以他们决定训练一个model去模仿simulator的逻辑。具体做法是VAE来压缩图片，这个只是优化用，用RNN来预测下一帧的动作才是重点。相当于对世界的逻辑建模
- [X] 2020/8 REALM 其实我不是很懂这个，白看了，对这个不熟。总的来说就是把整个资料库用来pretrain一个document retriver，然后来回答问题。又是一个大突破只能这样说。应用方面我想想，首先要有一个完善，不变的资料库，话说真的是不能变么？也许不一定，emm，我还是不评价了
- [X] No55 [2017 word embedding methods in topic segmentation] 找到这个关键词以来看的第一篇文章，原来在2017之前topic segmentation还那么落后的吗？总之看了论文的abstract，Overview on topic segmentation这一部分还可以，可以作为以后论文的参照。1. 没有用到神经网络的 2. 就连词语变换都是用的传统方法，连word2vec都没有用。
- [X] No56 2019 Sector 去年的论文，应该是最有参考价值的了。基本看了一遍，步骤大概是，1）用word2vec+distributional sentence representation来建模句子 2）用双向LSTM来建模Topic 3）classfication，用固定数量的外部标签来判断正确与否，softmax+onehot 4）用每个句子的分类准确度来判断分数。
- [X] [2015/6 Pointer networks] 说实话一直对这个模型的灵活性很佩服，可是现在（2021/1/4）因为用到所以重读了一遍发现: 1) 原本的精度就不高（train50，test50，精度72.6%） 2）他们测试的时候限制了输出数量，所以能跟LSTM作对比
- [X] 2015/11 order matters Q： 将输入数据的顺序打乱再训练，就能够提升精度么？A: 是的，主要是鼓励片段(短期)依赖，可以想象，使优化变得更加容易Sequence to Sequence Learning with Neural Networks
- [X] 2020 ACL A Joint Model for Document Segmentation and Segment Labeling 使用joint loss(segment + labeling)可以提高segment的精度。还有用到IOB tagging。是Sector的一个进阶尝试，因为他们在整所以labeling和我无关。
- [X] [2020 Text Segmentation by Cross Segment Attention] Text Segmentation by Cross Segment Attention 谷歌的文本分割论文，将之前的模型全部打翻了。但是我发现他没有考虑到保留上次的分割点，难道这个不会有影响吗？
- [X] [Neural Text Generation in Stories Using Entity Representations as Context] (https://vimeo.com/277672801) 有视频，可以
- [X] [Understanding deep learning requires rethinking generalization] （引用数量蛮多的，主要论点就是规范化可以提高效率但不是必要的）
- [X] [Google: Long Range Arena(2020)] 一个评判标准，本来像用着试试的后来发现它集成了太多东西，JAX啥的，tensorflow我不用，就算了吧。但是从结果上可以知道一点： 要速度用Performer，要性能用bigbird或者普通TF。
- [X] [What Do Position Embeddings Learn] 就对我有用的结论来说，bert对绝对位置的分辨很差劲，它更多的关注masked word附近的词。然后一般情况下用sinusoid是最好的。
- [X] AUTOMATED GENERATION OF MULTILINGUAL CLUSTERS FOR THE EVALUATION OF DISTRIBUTED REPRESENTATIONS (关于单词相似度检验的一些反思以及自动一种新的自动生成方案)
- 
