[Discussion of Kaiming initialization](https://medium.com/a-paper-a-day-will-have-you-screaming-hurray/day-8-delving-deep-into-rectifiers-surpassing-human-level-performance-on-imagenet-classification-f449a886e604)
[Compares Kaiming and Xavier Glorot initialization](https://pouannes.github.io/blog/initialization/)
[Mishin: all you need is a good init](https://arxiv.org/pdf/1511.06422.pdf)

[Hikvision: All You Need is Beyond a Good Init: Exploring Better Solution for Training Extremely Deep Convolutional Neural Networks
  with Orthonormality and Modulation] (https://openaccess.thecvf.com/content_cvpr_2017/papers/Xie_All_You_Need_CVPR_2017_paper.pdf):
  Applies orthogonal regularization during training. "Can train extremely deep DNN-s without residual connections." 

[Orthogonal regularization github code + paper](https://github.com/kevinzakka/pytorch-goodies#orthogonal-regularization)

[Can We Gain More from Orthogonality Regularizations in Training Deep CNNs?](https://papers.nips.cc/paper/7680-can-we-gain-more-from-orthogonality-regularizations-in-training-deep-networks.pdf)
* [Github for the same](https://github.com/VITA-Group/Orthogonality-in-CNNs)
* [PyTorch Implementation](https://github.com/VITA-Group/Orthogonality-in-CNNs/blob/master/Imagenet/preresnet/train_n.py)
* Reports
    * Improved training stability
    * Improved results in CIFAR10, CIFAR100
