### Clustering

* [2020/6 Learning To Classify Images Without Labels (Paper Explained)](https://www.youtube.com/watch?v=hQEnzdLkPj4&ab_channel=YannicKilcher) 一个新的clustering算法SCAN，在没有label的情况下都能达到很好的训练效果。主要流程是，首先用Transform来对图片做处理，然后用CNN来获取处理前后图片的latent representation，并努力缩减两者间的欧几里得距离，以此训练神经网络a。然后通过a把所有数据压缩到latent representation，以此弄成新的数据集，然后每个图片跟最邻近的5个图片作为一组用来训练神经网络b，b输出的结果是softmax，努力让结果一致就完了

### Summarization


### Translation

### RL

* [2018/4 World Models](https://www.youtube.com/watch?v=dPsXxLyqpfs&ab_channel=YannicKilcher) 因为每次都要调动simulator的话，训练会变得太昂贵（等等，这里用replay buff不就能解决了？），所以他们决定训练一个model去模仿simulator的逻辑。具体做法是VAE来压缩图片，这个只是优化用，用RNN来预测下一帧的动作才是重点。相当于对世界的逻辑建模


