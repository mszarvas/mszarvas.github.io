[CSP: Center and Scale Prediction: A Box-free Approach for Pedestrian and Face Detection](https://arxiv.org/pdf/1904.02948.pdf)
    * Keras code: https://github.com/liuwei16/CSP/blob/master/README.md
    * Sota in 2019 when not using other PEDE DB
    * Predicts center and scale
    * Power likely comes from up-scaling (via deconv) the lower resolution feature maps
    * Inits with City persons

[SADet: Learning An Efficient and Accurate Pedestrian Detector](https://arxiv.org/pdf/2007.13119.pdf)
    * Similar accuracy to the previous
    * Uses anchor boxes
    * Uses some tricks, such as "Cosine NMS" to achieve this top result.  Cosine NMS, and maybe other tricks
      could be combined with other methods
    * Light (vs. other academic methods, still 50 ms per frame on whatever dGPU they use)
    * Inits with City persons

[ALFNet: Learning Efficient Single-stage Pedestrian Detectors by Asymptotic Localization Fitting](https://openaccess.thecvf.com/content_ECCV_2018/papers/Wei_Liu_Learning_Efficient_Single-stage_ECCV_2018_paper.pdf)
    * Code: https://github.com/VideoObjectSearch/ALFNet
    *  Served as inspiration for CSP above

[Pedestron: Pedestrian Detection: The Elephant In The Room](https://arxiv.org/pdf/2003.08799v6.pdf)
   * 1.7% LAMR on Caltech, which is about half of the second best
   * Their trick is using multiple datasets in a sequence for pre-training and then fine-tuning from there
      * Note: again, things come to pre-training and fine tuning; somehow, all best results come via fine-tuning
   * Code: https://github.com/hasanirtiza/Pedestron
   * Guy: https://www.linkedin.com/in/irtiza-hasan-bb4a84b6/
      * Finished PhD in 2018
      * Primary interest: self-driving cars: http://irtizahasan.com/
   * Also author of the CSP paper