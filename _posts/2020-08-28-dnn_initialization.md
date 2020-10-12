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

* [Data Dependent Initialization of Convolutional Neural Networks](https://arxiv.org/pdf/1511.06856.pdf)
    * Guy's focus is not just init but good transfer learning
    * Lots of test data
    * Might be doing similar things to what I did by normalizing each layer's output variance, using input data
    * Key learning might be that pre-training on image-net provides huge advantage vs. training from scratch
        * Need more thinking what to do with this information
        * Where is the knowledge coming from?
            * Coming from the hard work of the labelers of Imagenet?
            * Coming from the manually tuned learning rates of the Imagenet DNN?
            * When using Imagenet pre-training, what learning rates are these guys using for fine-tuning?
                * Using Imagenet's manually tuned learning rates?
        * Is it any better than adding the same amount of domain-specific labelled data? -- Moot question, we don't have such data.
        * For what data set size is Imagenet pre-training important and at what size does it become irrelevant?
        * What happens if we try to train Imagenet with random weights vs with this guy's, etc. optimized init?
        * Should re-read the old papers and track how did they do initializaiton and what tricks they did for ensuring convergence?
            * Looks like Googlenet originally used extra training heads, just like the older Cifar paper, for providing direct feedback to earlier layers
                * Such things tend to get forgotten
        
