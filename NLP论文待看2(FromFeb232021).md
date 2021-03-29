## TODO

- [ ] What do recurrent neural network gammars learn about syntax? (语法建模)
- [ ] On Unifying Deep Generative Models (统一生成模型) (No1的后续论文)
- [ ] Learning Transferable Visual Models From Natural Language Supervision (Open AI CLIP)
- [ ] Self-supervised learning: Generative or contrastive (Self-supervised Explore)

### Transformer

- [X] 2019 56 Compressive Transformer (谷歌的长距离TF) (通用性我感觉比较强，还有一个非常有意思的loss函数，可以处理长程依赖，受益匪浅) 

### BERT

- [X] What does BERT learn about the structure of language? (用之前看过的那个probing任务分析BERT)
- [X] BERT-enhanced Relational Sentence Ordering Network (收获不少)
- [ ] BERTRAM: Improved Word Embeddings Have Big Impact on Contextualized Model Performance (提高性能)
  - [ ] Attentive mimicking: Better word embeddings by attending to informative contexts. (AM，不知道能不能对TF有帮助，稀有单词的对应方式)
- [ ] How does BERT’s attention change when you fine-tune? An analysis methodology and a case study in negation scope (看看不会有坏处的，解剖bert)
- [ ] What Does BERT with Vision Look At? (看看不会有坏处)
- [ ] Understanding Advertisements with BERT 
- [ ] Should You Fine-Tune BERT for Automated Essay Scoring? (关于fine tune的问题)
- [ ] A Novel Hierarchical BERT Architecture for Sarcasm Detection (新架构？)
- [ ] ALBERT-BiLSTM for Sequential Metaphor Detection (隐喻检测？)

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


#### NLP
- [ ] 2018 89 Disentangled representation learning for text style transfer. (text style transfer) 
- [ ] 2018 254 Style transfer in text: Exploration and evaluation. (text style transfer)
- [ ] 2018 154 Syntax-directed variational autoencoder for structured data. (impose context-free grammars (CFGs as hard constraints in the VAE decoder)
- [ ] 2018 123 A deep generative framework for paraphrase generation.
- [ ] 2018 11 Syntactic manipulation for generating more diverse and interesting texts.
- [ ] 2017 374 Grammar variational autoencoder.

## Done 

- [X] #1 Generating Sentences from Disentangled Syntactic and Semantic Spaces (居然是字节跳动的论文，主要是对潜在空间的z计算了一些辅助loss，以引入一些额外知识，老实说太复杂了我感觉应用前景不大)
- [X] #2 2017 Toward controlled generation of text.  (text style transfer) (Adversarial Loss)
- [X] #3 2016 cite2572 InfoGan
  - [X] #3.1 Understanding Mutual Information and its Use in InfoGAN
- [X] PIAGET’S STRUCTURALISM AND LINGUISTICS (Cool)
- [X] CogLTX: Applying BERT to Long Texts (清华大学，延长BERT处理长度) (引入了一个记忆机制，其实可以理解成一个attention，) (可以理解成衰减self attention)
