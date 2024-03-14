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
Tasks related to layout generation（布局生成的相关任务）：

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
- Rico: A Mobile App Dataset for Building Data-Driven Design Applications (**ACM UIST** 2017) [[Paper]](http://ranjithakumar.net/resources/rico.pdf) [[dataset]](http://www.interactionmining.org/rico.html#quick-downloads)
- PubLayNet: largest dataset ever for document layout analysis (**ICDAR** 2019) [[Paper]](https://arxiv.org/pdf/1908.07836v1.pdf) [[dataset]](https://github.com/ibm-aur-nlp/PubLayNet)
