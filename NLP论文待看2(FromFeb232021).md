## TODO

- [ ] What do recurrent neural network gammars learn about syntax? (语法建模)
- [ ] On Unifying Deep Generative Models (统一生成模型) (No1的后续论文)
- [ ] Learning Transferable Visual Models From Natural Language Supervision (Open AI CLIP)
- [ ] Self-supervised learning: Generative or contrastive (Self-supervised Explore)

### Transformer

- [X] 2019 56 Compressive Transformer (谷歌的长距离TF) (通用性我感觉比较强，还有一个非常有意思的loss函数，可以处理长程依赖，受益匪浅) 
- [ ] 2021 `Trending` Swin Transformer: Hierarchical Vision Transformer using Shifted Windows (像CNN一样的TF，有替代CNN的潜力)

### BERT

- [X] What does BERT learn about the structure of language? (用之前看过的那个probing任务分析BERT)
- [X] BERT-enhanced Relational Sentence Ordering Network (收获不少)
- [ ] BERTRAM: Improved Word Embeddings Have Big Impact on Contextualized Model Performance (提高性能)
  - [ ] Attentive mimicking: Better word embeddings by attending to informative contexts. (AM，不知道能不能对TF有帮助，稀有单词的对应方式)
  - [X] Learning Semantic Representations for Novel Words (还不错，但是主要是用平均上下文的方式，而且首先要有上下文……而且日语的表面信息不像英语那样好拿) 
- [X] How does BERT’s attention change when you fine-tune? An analysis methodology and a case study in negation scope (看看不会有坏处的，解剖bert) (一点吊意思都没有怎么进ACL的)
- [X] What Does BERT with Vision Look At? (看看不会有坏处) (还行，视觉BERT还蛮有意思，可是怎么输出注意力区域我是不能理解的，毕竟不是做视觉和跨领域)
- [X] Should You Fine-Tune BERT for Automated Essay Scoring? (关于fine tune的问题) (没什么收获，他们试了feature extraction，结果比较差，没意义。不过推荐的几个论文倒是蛮有意思，看下边的BERTology)
  - [X] To Tune or Not to Tune? Adapting Pretrained Representations to Diverse Tasks (关于fine tune的问题)  (证据证明BERT同时建模句子对的效果更好) (交互信息评估仪的应用)
  - [ ] Do Attention Heads in BERT Track Syntactic Dependencies? 
  - [X] What Does BERT Look at? An Analysis of BERT’s Attention (解剖BERT) (斯坦福大学+脸书的论文，但是老实说没有什么收获，非要说的话 #1 SEP像是一个垃圾桶。 #2 CLS确实起到统合作用) （也许我后续要考虑带上两个SEP……）
- [ ] A Novel Hierarchical BERT Architecture for Sarcasm Detection (新架构？)
- [X] ALBERT-BiLSTM for Sequential Metaphor Detection (隐喻检测？) (Q：我也可以发ACL workshop吗？。三种subword的处理方式，最后选了只保留首部。保留BERT的output用作concat重要CRF vs Softmax)
- [ ] BERT-ology
  - [ ] 2019 321 Bert rediscovers the classical nlp pipeline. 
  - [ ] 2019 240 What does bert learn about the structure of language?
  - [ ] 2019 140 Revealing the Dark Secrets of BERT
  - [ ] 2020 153 A Primer in BERTology: What we know about how BERT works?
- [X] Simple BERT Models for Relation Extraction and Semantic Role Labeling (因为使用了多个SEP，需要赶紧看) (不是想象中的用法。不过还算是有收获，让BERT去学习元语言，居然也能正常运作)
- [X] Leveraging BERT for Extractive Text Summarization on Lectures (BERT做抽出要约。看能不能想到改善的方法？主要思考新方向) 
- [X] Understanding Advertisements with BERT (单纯用字幕就能理解图片……确实make sense)
- [X] Fine-tune BERT for Extractive Summarization （还行，不过好像对BERT的）
- [X] CogLTX: Applying BERT to Long Texts (清华大学，延长BERT处理长度) (引入了一个记忆机制，其实可以理解成一个attention，) (可以理解成衰减self attention)
- [X] Applying BERT to Document Retrieval with Birch (和想象的不一样，IR似乎是搜索引擎相关的东西，而不是制表)
- [X] Improving Context Modeling in Neural Topic Segmentation (这你妈不就是我的想法吗……有点蛋疼。假设在性能上没法超过，我的研究还有什么新规性呢？1）日语 2）段落分割不等于主题分割 3）架构上不一样。还有就是到底要不要引用这个论文呢？如果性能没办法超过就不要引了，如果wikisection上的性能超过那就引吧，还能补充一句说BERT就是王，其他绕道走)（得到的新思路是可以BERT + static embedding，也许性能会更好）

### 评估与分析
- [X] Scalable Mutual Information Estimation using Dependence Graphs (互信息评估仪，可以评估不同方案embedding和相应label的相关程度。值得看，也许能作为评估手段) (还行，主要是信息论在DNN上的运用。配合下面一个看，算是剖析神经网络。最重要的收获： 先扩大再缩小，泛化=压缩性能更好，而且不需要那么多的参数)
  - [X] [DL輪読会]Opening the Black Box of Deep Neural Networks via Information (很大收获，隐藏层的意义： 增加隐藏层，泛化=压缩的速度加快)
- [ ] `Trending` TextFlint: Unified Multilingual Robustness Evaluation Toolkit for Natural Language Processing (一个更好的评估方法，必看)
- [ ] Attention is not not Explanation (可以理解成一个分析方法的汇总) (Waiting...)

### VAE & GAN

#### CV
- [ ] 0 TransGAN (用来代替#99，毕竟我完全不想用CNN)
  - [ ] 2016 2315 Real-Time Single Image and Video Super-Resolution Using an Efficient Sub-Pixel Convolutional Neural Network (#100的前置)
  - [ ] 2016 5178 Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network （#101相关）
- [ ] 2018 20 Generative Adversarial Interpolative Autoencoding (GAIA) (线性插值，VAE和GAN的融合) 
- [ ] 2017 7578 CycleGAN
- [ ] 2018 1717 A Style-Based Generator Architecture for Generative Adversarial Networks (Style gan，正在做) (需要前置： Arbitrary Style Transfer)
- [ ] 2017 1084 Arbitrary Style Transfer in Real-time with Adaptive Instance Normalization (STleGan 前置)
- [ ] #99 2016 8604 Unsupervised representation learning with deep convolutional generative adversarial networks (图片空间向量操作)
- [X] 2019 44 ON THE RELATIONSHIP BETWEEN AND CONVOLUTIONAL LAYERS (现在CNN用爽了，不用自找麻烦了)
- [ ] 2021 `Trending` Swapping Autoencoder for Deep Image Manipulation (当前AE最好的应用了应该)
- [X] #3 2016 cite2572 InfoGan
  - [X] #3.1 Understanding Mutual Information and its Use in Info
- [ ] 2016 90 Preserving Color in Neural Artistic Style Transfer (Adobe的研究，保留style之后再跟其他图片合成，效果看起来还满可以的，视觉就是痛快)
- [ ] 2017 293 Demystifying Neural Style Transfer (样式转换本质上是领域适应问题？总之看看吧)

#### NLP
- [X] 2018 557 Toward Controlled Generation of Text (VAE。这个效果好像是近期见过最好的。也许应该从这个的引用论文开始看，而不是看以前的老古董)
  - [ ] 2020 20 A Probabilistic Formulation of Unsupervised Text Style Transfer (Doing...)
- [ ] 2018 89 Disentangled representation learning for text style transfer. (text style transfer) 
- [X] 2018 254 Style transfer in text: Exploration and evaluation. (text style transfer) (北大+南加州大学的论文，这种质量真是见鬼了，主要思路是用GAN来对抗生成想要的style，可是看起来效果很差。唯一的收获是又找到几篇论文)
- [ ] 2018 154 Syntax-directed variational autoencoder for structured data. (impose context-free grammars (CFGs as hard constraints in the VAE decoder)
- [ ] 2018 123 A deep generative framework for paraphrase generation.
- [ ] 2018 11 Syntactic manipulation for generating more diverse and interesting texts.
- [ ] 2017 374 Grammar variational autoencoder.
- [X] #1 Generating Sentences from Disentangled Syntactic and Semantic Spaces (居然是字节跳动的论文，主要是对潜在空间的z计算了一些辅助loss，以引入一些额外知识，老实说太复杂了我感觉应用前景不大)
- [X] #2 2017 Toward controlled generation of text.  (text style transfer) (Adversarial Loss)
- [ ] 2017 133 adversarial multi-criteria learning for chinese word segmentation (用GAN来分词，还是中文，总之看一下吧) (Doing...)


### CV NLP 交叉领域
- [ ] Beyond Visual Semantics: Exploring the Role of Scene Text in Image Understanding
- [X] 2021 16 MLP-Mixer: An all-MLP Architecture for Vision (这个看了油管的解读，首先回到原点挺好的，留下的技术只有GELU和skip connection和batch norm；重点是分batch，然后横竖使用MLP，很简单；比起vision transformer的好处在于，TF需要平方计算时间和内存容量；虽然小量数据集的性能还是堪忧，但是大量数据集完全可以和其他模型较劲；)

### 遗产
- [ ] A Formal Hierarchy of RNN Architectures (饱和RNN理论，证伪LSTM)
- [X] PIAGET’S STRUCTURALISM AND LINGUISTICS (Cool)


### 方向不明(重要，开拓新方向)
- [X] BERT-based Spatial Information Extraction (句子中的位置信息提取任务还蛮有意思。joint model; Resnet; Dropout; CLS+Mean;)
