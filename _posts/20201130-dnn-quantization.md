
Raghuraman Krishnamoorthi, 2018,
[Quantizing deep convolutional networks for efficient inference: A whitepaper](https://arxiv.org/pdf/1806.08342.pdf)
    * Wide overview of quantization
    * Includes results
    * Some results not SOTA
    * Might be superceded by Wu 2020
    * Still, wide references

Hao Wu, Patrick Judd, Xiaojie Zhang, Mikhail Isaev, Paulius Micikevicius, 2020,
[INTEGER QUANTIZATION FOR DEEP LEARNING INFERENCE: PRINCIPLES AND EMPIRICAL EVALUATION](https://arxiv.org/pdf/2004.09602.pdf)
    * Symmetric, per channel for weights
    * Symmetric, per tensor for activations
    * MobileNet needs QAT
    * Some nets may need even more, such as distillation
    * Includes receipe and evaluation results


[Distilling the Knowledge in a Neural Network](https://arxiv.org/pdf/1503.02531.pdf)
    * Use targets for small net based on outputs of larger net, instead of the original hard 0/1 targets
    * The training set can be the same

Asit Mishra & Debbie Marr
[APPRENTICE: USING KNOWLEDGE DISTILLATION TECHNIQUES TO IMPROVE LOW-PRECISION NETWORK ACCURACY](https://arxiv.org/pdf/1802.05668.pdf)
    * Takes credit for being the original distiller for improving quantized results
    
Antonio Polino, Razvan Pascanu, Dan Alistarh,
[MODEL COMPRESSION VIA DISTILLATION AND QUANTIZATION](https://arxiv.org/pdf/1802.05668.pdf)
    * https://github.com/antspy/quantized_distillation
    * Two new compression methods, which jointly leverage weight quantization and distillation of larger networks, called “teachers,” into compressed “student” networks
    * Quantized shallow students can reach similar accuracy levels to state-of-the-artfull-precision teacher models, while providing up to order of magnitude compression, and inference speedup that is almost linear in the depth reduction
    
