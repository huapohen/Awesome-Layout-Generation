# Awesome-Layout-Generation
<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/layout2023.png">
</p>

## What is Layout ？

**Layout** refers to the three elements [**position, size, and type**] of the relevant elements in the layout (or in the image). It is often used in graphic design, poster design, UI layout design, printing layout design, magazine design, etc. Relevant elements can be foregrounds such as [**text, objects**], without background. Text can be divided into [_a large word in a frame, a line of words in a frame, or multiple lines of words in a frame, or any words combined into a frame_] according to different granularities. ], objects with different granularities can be divided into [_frames of main elements, frames of auxiliary elements, and frames composed of arbitrary objects_].


**布局(Layout)**，即版面中（也可以是图像中）有关元素的框的【**位置、大小、类型**】三要素，常用于平面设计、海报设计、UI排版设计、印刷排版设计、杂志设计、等等。有关元素可以是【**文字、物体**】这类前景，没有背景，文字根据粒度不同可以分为【_一个很大的字一个框、一行字一个框、或多行字一个框、任意字组合成一个框_】，物体粒度不同可以分为【_主体元素的框、辅助元素的框、任意物体组合后的框_】。

<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/rico.png">
</p>

<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/publaynet.png">
</p>

<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/poster_box_layout.png">
</p>

## What is Layout Generation ？

**Layout generation** uses deep learning to generate layouts. The most typical example is using models (GAN, VAE) and diffusion models (Diffusion Model, or DM/Diffusion) from the generation of adversarial networks to directly generate layouts ( layout generation), some are also generated using Transformer. Figures below illustrate the visualization process diagram of using the diffusion model (Diffusion) to "unconditionally" generate layouts.

**布局生成**，即利用深度学习的手段，进行布局layout的生成，最典型的例子为用生成对抗网络时代的模型（GAN、VAE）和扩散模型（Diffusion Model，或 DM / Diffusion）来直接生成布局（layout generation），也有利用Transformer来生成的。如下图示意了用扩散模型（Diffusion）来进行“无条件”生成布局的可视化过程图。

<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/forward process.png">
</p>

<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/reverse process.png">
</p>

## Tasks related to layout generation（布局生成的相关任务）
无条件生成(unconditional generation):  
  - Diffusion Model  
      
基于条件的生成(Condition-based generation):
  1. 基于类型+个数的布局生成：即有几个框，框的类型是什么。Layout generation of boxes based on type + number
  2. 基于初始化框，进行布局补全。Based on the initialized box, perform layout completion 
  3. 布局调整/重排。layout refinement or rearrangement
  4. 基于类型、个数、大小的布局生成。Layout generation based on type, number, and size 
<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/conditional.png">
</p>   
  5. content-aware text-box generation  <br>
  6. multimodal inputs + prompter <br>
  7. generate image or wireframe directly  <br>
  8. inpainting or outpainting: according to poster layout box, generate elements or background <br>
<p align="center">
  <img width="460" src="https://github.com/huapohen/Awesome-Layout-Generation/blob/main/assets/poster_box_layout.png">
</p>  
  9. others   


## datasets
- **Rico**: A Mobile App Dataset for Building Data-Driven Design Applications (**ACM UIST** 2017) [[Paper]](http://ranjithakumar.net/resources/rico.pdf) [[dataset]](http://www.interactionmining.org/rico.html#quick-downloads)
- **PubLayNet**: largest dataset ever for document layout analysis (**ICDAR** 2019) [[Paper]](https://arxiv.org/pdf/1908.07836v1.pdf) [[dataset]](https://github.com/ibm-aur-nlp/PubLayNet)
- Magazine: Content-aware Generative Modeling of Graphic Design Layouts (**SIGRAPH** 2019) [[Paper]](https://xtqiao.com/projects/content_aware_layout/paper.pdf) [[dataset]](https://xtqiao.com/projects/content_aware_layout/)
- WebUI: WebUI: A Dataset for Enhancing Visual UI Understanding with Web Semantics (**CHI** 2023) [[Paper]](https://arxiv.org/pdf/2301.13280v1.pdf) [[dataset]](https://uimodeling.github.io/)
- DocLayNet: A Large Human-Annotated Dataset for Document-Layout Analysis (**KDD** 2022) [[Paper]](https://arxiv.org/pdf/2206.01062v1.pdf) [[dataset]](https://github.com/DS4SD/DocLayNet)
- M6Doc: A Large-Scale Multi-Format, Multi-Type, Multi-Layout, Multi-Language, Multi-Annotation Category Dataset for Modern Document Layout Analysis (**CVPR** 2023) [[Paper]](https://arxiv.org/pdf/2305.08719.pdf) [[dataset]](https://github.com/HCIILAB/M6Doc)
- CLG v1: Composition-aware Graphic Layout GAN for Visual-textual Presentation Designs (**IJCAI** 2022) [[Paper]](https://arxiv.org/pdf/2205.00303v3.pdf) [[dataset]](https://tianchi.aliyun.com/dataset/142692)
- CLG v2: Relation-Aware Diffusion Model for Controllable Poster Layout Generation (**CIKM** 2023) [[Paper]](https://arxiv.org/pdf/2306.09086.pdf) [[dataset]](https://github.com/liuan0803/RADM?tab=readme-ov-file)
- PosterLayout: A New Benchmark and Approach for Content-aware Visual-Textual Presentation Layout (**CVPR** 2023) [[Paper]](https://arxiv.org/pdf/2303.15937v1.pdf) [[dataset]](https://github.com/PKU-ICST-MIPL/PosterLayout-CVPR2023)
- Huggingface reference link: https://github.com/pytorch-layout-generation


## papers (containing unconditional generation)
## 2024
- LayoutNUWA: Revealing the Hidden Layout Expertise of Large Language Models (**ICLR** 2024) [[paper]](https://openreview.net/pdf?id=qCUWVT0Ayy)
- Towards Aligned Layout Generation via Diffusion Model with Aesthetic Constraints (**ICLR** 2024) [[paper]](https://arxiv.org/pdf/2402.04754v1.pdf)
- Spot the Error:  Non-autoregressive Graphic Layout Generation with Wireframe Locator (**ICLR** 2024) [[paper]](https://arxiv.org/pdf/2401.16375v1.pdf)
- Dolfin: Diffusion Layout Transformers without Autoencoder (**withdraw**) [[paper]](https://arxiv.org/pdf/2310.16305v1.pdf)

## 2023
- LayoutDM: Discrete Diffusion Model for Controllable Layout Generation (**CVPR** 2023) [[paper]](https://arxiv.org/pdf/2303.08137v1.pdf) [[**code**]](https://github.com/CyberAgentAILab/layout-dm)
- LayoutDiffusion: Improving Graphic Layout Generation by Discrete Diffusion Probabilistic Models (**ICCV** 2023) [[paper]](https://arxiv.org/pdf/2303.11589v2.pdf)
- Diffusion-based Document Layout Generation (**ICDAR** 2023) [[paper]](https://arxiv.org/pdf/2303.10787v1.pdf) [[**code**]](https://github.com/microsoft/LayoutGeneration/tree/main/LayoutDiffusion)
- LayoutPrompter: Awaken the Design Ability of  Large Language Models (**NeurIPS** 2023) [[paper]](https://arxiv.org/pdf/2311.06495v1.pdf) [[**code**]](https://github.com/microsoft/LayoutGeneration/tree/main/LayoutPrompter)
- A Parse-Then-Place Approach for Generating Graphic Layouts  from Textual Descriptions (**ICCV** 2023) [[paper]](https://arxiv.org/pdf/2308.12700v1.pdf)
- Unifying Layout Generation with a Decoupled Diffusion Model (**CVPR** 2023) [[paper]](https://arxiv.org/pdf/2303.05049v1.pdf)
- LayoutDM: Transformer-based Diffusion Model for Layout Generation (**CVPR** 2023) [[paper]](https://arxiv.org/pdf/2305.02567v1.pdf)
- DLT: Conditioned layout generation with  Joint Discrete-Continuous Diffusion Layout Transformer (**ICCV** 2023) [[paper]](https://arxiv.org/pdf/2303.03755v1.pdf) [[**code**]](https://github.com/wix-incubator/DLT)
- PLay: Parametrically Conditioned Layout Generation using Latent Diffusion (**ICML** 2023) [[paper]](https://arxiv.org/pdf/2301.11529v2.pdf)

before 2023, I don't collect papers.
## 2022
- Composition-aware Graphic Layout GAN for  Visual-textual Presentation Designs (**IJCAI** 2022) [[paper]](https://arxiv.org/pdf/2205.00303v3.pdf)
- Layout Generation as Intermediate Action Sequence Prediction (**AAAI** 2023) [[paper 2205]](https://arxiv.org/pdf/2205.00303v3.pdf)
- LayoutFormer++: Conditional Graphic Layout Generation via Constraint Serialization and Decoding Space Restriction (**CVPR** 2023) [[paper 2208]](https://github.com/microsoft/KC/tree/main/papers/LayoutAction)

## 2021
- BLT: Bidirectional Layout Transformer for Controllable Layout Generation (**ECCV** 2022) [[paper 2112]](https://arxiv.org/pdf/2112.05112v2.pdf) [[**code**]](https://github.com/google-research/google-research/tree/master/layout-blt)
- Constrained Graphic Layout Generation via Latent Optimization (**ACM MM** 2021) [[paper]](https://arxiv.org/pdf/2108.00871v1.pdf) [[**code**]](https://github.com/ktrk115/const_layout)
- LayoutTransformer: Scene Layout Generation with Conceptual and Spatial Diversity (**CVPR** 2021) [[paper]](https://openaccess.thecvf.com/content/CVPR2021/papers/Yang_LayoutTransformer_Scene_Layout_Generation_With_Conceptual_and_Spatial_Diversity_CVPR_2021_paper.pdf) [[**code**]](https://github.com/davidhalladay/LayoutTransformer)

## 2020
- READ: Recursive Autoencoders for Document Layout Generation (**CVPRW** 2020) [[paper]](https://arxiv.org/pdf/1909.00302v4.pdf)

## 2019
- Neural Design Network: Graphic Layout  Generation with Constraints (**ECCV** 2020) [[paper 1912]](https://arxiv.org/pdf/1912.09421v2.pdf)
- Content-aware Generative Modeling of Graphic Design Layouts (**SIGRAPH** 2019) [[paper]](https://xtqiao.com/projects/content_aware_layout/paper.pdf) [[**code+dataset**]](https://xtqiao.com/projects/content_aware_layout/paper.pdf)
- LayoutGAN: Synthesizing Graphic Layouts with Vector-Wireframe Adversarial Networks (**ICLR** 2019) [[paper]](https://arxiv.org/pdf/1901.06767.pdf)
- LayoutVAE: Stochastic Scene Layout Generation From a Label Set (**ICCV** 2019) [[paper]](https://arxiv.org/abs/1907.10719)

## papers reference links:
https://github.com/JosephKJ/Awesome-Layout-Generators  
https://github.com/microsoft/LayoutGeneration  
https://github.com/Layout-Generation/layout-generation  
