### Todo

- [ ] Generating sentences from a continuous space （因为和我之前设想的很像。只是如果可行也和我无关，因为我不整generation）
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
- [ ] Universal transformers (将RNN和TF的优点结合，必看)
- [ ] Convolutional sequence to sequence learning. （在S2S上使用卷积，2017，可以看，主要是pos embedding）
- [ ] Interpreting Pretrained Contextualized Representations via Reductions to Static Embeddings (contextualized representation -> static embedding， 我本来是想看看有没有加快bert的方法的，但是contextual注定是要fine-tune的吧。static embedding可以用来做通用embeding。。对)


### Done

- [X] Text Segmentation by Cross Segment Attention
- [X] Long range arena
- [X] What Do Position Embeddings Learn (为了实验vanila TF，快速过一遍)
- [X] A SIMPLE BUT TOUGH TO BEAT BASELINE FOR SENTENCE EMBEDDINGS (BERT一亿参数太慢了，看看要不要用word2vec来整) (唯一明白的就是自己看不懂统计学方法，你妈的有神经网络还要个鸡巴统计学啊，所以才会被bert打的要死啊，看看bert有没有用到word2vec再说。。后续直接用RNN)
- [X] Adaptive Computation Time for Recurrent Neural Networks (在每个timestep，再纵向运算1到n次，相当于可以多思考一会儿。大概概念就是这样，但是式子有些麻烦就没看)
