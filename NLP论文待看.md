### TODO

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
