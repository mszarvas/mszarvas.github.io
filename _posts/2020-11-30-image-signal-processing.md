-[DSLR-Quality Photos on Mobile Devices with Deep Convolutional Networks](https://arxiv.org/pdf/1704.02470.pdf)
    - Andrey Ignatov, Nikolay Kobyshev, Kenneth Vanhoey, Radu Timofte, Luc Van Gool
    - Good literature overview
    - Creates database of point and shoot and DSLR camera images
    - Explains how to align: SIFT + Homography via RANSAC
    - Explains error function
    - Explain issues of MSE error, related to lack of proper alignment -- no matter what, there exists alignment noise and perfect alignment via homogaraphy is not possible

-[Replacing Mobile Camera ISP with a Single Deep Learning Model](https://arxiv.org/pdf/2002.05509.pdf), 2020
    - Andrey Ignatov, Luc Van Gool, Radu Timofte
    - RAW to RGB
    - Similar to previous paper; not sure if it was RAW or not

-[Low Cost Edge Sensing for High Quality Demosaicking]()
    - Yan Niu , Jihong Ouyang, Wanli Zuo, and Fuxin Wang
    - IEEE TRANSACTIONS ON IMAGE PROCESSING, VOL. 28, NO. 5, MAY 2019
    - Benchmarks against 27 others, by running public code on identical data
    - 10-s of times faster at similar quality
    - Or better quality at similar runtime

-[Soft Prototyping Camera Designs for Car Detection Based on a Convolutional Neural Network]()
    - Zhenyi Liu, Trisha Lian, Joyce Farrell, and Brian Wandell
    - Simulates physically accuurate scenes
    - Simulates camera / lens?
    - Reference to simulator
    - Reference to 3D data
    - Validated using spectroradiometer
    - Higher resolution is more important at every light level
    - sRGB pipeline and simpler pipeline gave similar detection accuracy
    - Gamma not critical
    - Measures of IQ are not a good predictor of object detection accuracy
    - Bracketed HDR is better than center weighted exposure (but hard to measure on average; shows anecdotal evidence)

- [CURL: Neural Curve Layers for Global Image Enhancement](), 2020
    - Sean Moran∗,1, Steven McDonagh2, Gregory Slabaugh
    - RGB-to-RGB (enhancement) or
    - RAW-to-RGB (while ISP)
    - Uses aligned data from other projects

- [Reconfiguring the Imaging Pipeline for Computer Vision]()
    - Remove most ISP blocks to reduce energy
    - "Demosaic and gamma only are important"

- [Handheld Multi-Frame Super-Resolution]()
    - BARTLOMIEJ WRONSKI, IGNACIO GARCIA-DORADO, MANFRED ERNST, DAMIEN KELLY, MICHAEL KRAININ, CHIA-KAI LIANG, MARC LEVOY, and PEYMAN MILANFAR, Google Research
    - Multi-frame super-resolution
    - Directly from raw
    - No demosaic (at least not up-front)
    - Utilizes that shaking hand is scanning the image and fills the missing pixels
    - Explains sub-pixel registration of frames

- [Trinity of Pixel Enhancement: a Joint Solution for Demosaicking, Denoising and Super-Resolution]()
    - Reference images come from a Sony digital camera that can shake the sensor by 1 pixel, in order to capture the missing colors on the Bayer array

- [Comparison of color demosaicing methods]()
    - O. Lossona, L. Macairea, Y. Yang
    - 87 pages

- [Learning Deep Convolutional Networks for Demosaicing]()
    - 2018, Nai-Sheng Syu, Yu-Sheng Chen, Yung-Yu Chuang


- [Deep Demosaicing for Edge Implementation]()
    - Ramchalam Ramakrishnan, Shangling Jui, and Vahid Patrovi Nia

- [Image Demosaicing: A Systematic Survey]()
    - Xin Lia, Bahadir Gunturkb and Lei Zhan

- [ADAPTIVE JOINT DEMOSAICING AND SUBPIXEL-BASED DOWN-SAMPLING FOR BAYER IMAGE]()
    - Lu Fang, Oscar C. Au, Aggelos K. Katsaggelos

- [Restoration of Bayer-Sampled Image Sequences]()
    - Murat Gevrekci‡, Bahadir K. Gunturk‡, and Yucel Altunbasak§

- [Towards Real Scene Super-Resolution with Raw Images]()
    - Xiangyu Xu Yongrui Ma Wenxiu Sun, SenseTime Research

- [Comparative Study of Various Approaches For Joint Demosaicing And Subpixel Based Downsampling In Bayer Images]()
    - Lekshmi P R

- [Efficient, High-Quality Bayer Demosaic Filtering on GPUs]()
    - Morgan McGuire∗ Williams College

- [Color Reproduction From Noisy CFA Data of Single Sensor Digital Cameras]()
    - Lei Zhang, Member, IEEE, Xiaolin Wu, Senior Member, IEEE, and David Zhang, Senior Member, IEEE

- [A Fast Demosaicking Method Directly Producing YCbCr 4:2:0 Output]()
    - Colin Doutre, Student Member, IEEE, Panos Nasiopoulos, Member, IEEE, and Konstantinos N. Plataniotis, Senior Member, IEEE




- [Deep Photo Enhancer: Unpaired Learning for Image Enhancement from Photographs with GANs](https://openaccess.thecvf.com/content_cvpr_2018/papers_backup/Chen_Deep_Photo_Enhancer_CVPR_2018_paper.pdf)
    - https://github.com/nothinglo/Deep-Photo-Enhancer
    - Style transfer type, not matched pairs


-[Image quality assessment using the dead leaves target: experience with the latest approach and further investigations](https://www.semanticscholar.org/paper/Image-quality-assessment-using-the-dead-leaves-with-Artmann/1b5356e996bfb4a80b7bae5e72f9e1d4dcd81b2d)
    - Uwe Artmann, Image Engineering GmbH & Co KG
    - Details of objective IQ evaluation method
    - Align DSLR and point and shoot data



