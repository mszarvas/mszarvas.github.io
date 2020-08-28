
fast.ai [Self superrvised learning](https://www.fast.ai/2020/01/13/self_supervised/) states that transfer learning is a must and improves accuracy.

[Transfusion: Understanding Transfer Learning for Medical Imaging](https://arxiv.org/pdf/1902.07208.pdf) says that transfer learning from general CV models is the standard approch to medical imaging tasks but the pretrained models dont, in reality, improve performance at all. Not even for non-medical imaging tasks.

Imagenet type models have many parameters in the higher layers because of the large number of classes.

Both the fast.ai paper and the transfusion paper note that the primary benefit of pretraining is faster convergence.

Transfusion paper: it is sufficient to keep only the *scaling* of pre-trained weights in order to get the convergence speed benefit.
Any such comparison should include the advanced initialization methods among the baselines in order to be relevant:

[Saxe 2014: Random orthogonal initialization](https://www.saxelab.org/assets/papers/Saxe2014.pdf): discusses / compares to pre-training; focus is in linear networks

[Mishkin 2016: All you need is a good init](https://arxiv.org/pdf/1511.06422.pdf): Layer-sequential unit-variance init; focus is on non-linear networks

Mishkin's unit variance init and the transfusion paper's keeping the weight scalings is similar.

The [fast.ai](https://www.fast.ai/2020/01/13/self_supervised/) paper says that the transfusion paper says that using the first few layers of a pre-trained imagenet model will improve both the convergence speed and the accuracy of medical imaging models.  But the intro of the Transfusion paper is suggesting a different message.  Should verify.

Okay, fast.ai acknowledges that the improvement from imagenet is small.

Then they come with self-supervised training, where the training targets are some natural attribute of the unlabelled training data.

[Howard, Ruder: Universal language model fine-tuning for text classification](https://arxiv.org/pdf/1801.06146.pdf), [blog on the same paper](https://nlp.fast.ai/classification/2018/05/15/introducing-ulmfit.html): train a DNN language model for the purpose of converting words to features.  Then use the feature vectors for sentiment analysis = document classification.  100x reduction in data need for the text classification task.  Also, ~20% reduction in error rate vs. SOTA.

This fast.ai [ULMFiT blog](https://nlp.fast.ai/classification/2018/05/15/introducing-ulmfit.html) calls Google *word2vec* as single-layer transfer learning = embedding.

[What makes Imagenet good for transfer learning](https://arxiv.org/pdf/1608.08614.pdf): does not answer the question but shows that much smaller amount of pre-training data and smaller number of classes is sufficient. Many references to transfer learning papers and how do they do transfer learning.

Big overview blog post with references: [Transfer Learning - Machine Learning's Next Frontier](https://ruder.io/transfer-learning/)

[ULMFiT paper](https://nlp.fast.ai/classification/2018/05/15/introducing-ulmfit.html) talks about transfer-learning/refinement techniques needed to avoid the model forgetting the pre-training results (gradual unfreezing, discriminative learning rates, and one-cycle training). The `fastai2` `fine_tune` method implements these techniques.

[How transferable are features in deep neural networks?](https://arxiv.org/pdf/1411.1792.pdf): "Transferability is negatively affected by optimization difficulties related to splitting networks between co-adapted neurons, which was not expected." " initializing a network with transferred features from almost any number of layers can produce a boost to generalization that lingers even after fine-tuning to the target dataset".




