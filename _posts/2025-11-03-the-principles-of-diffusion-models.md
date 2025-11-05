---
title: "What actually is diffusion model?"
date: 2025-11-03 17:46:00 +0800
categories: ["The Principles of Diffusion Models: From Origins to Advances"]
tags: [diffusion-models, reading-notes, generative-models]
---

### 我不喜欢从原理讲起的书，但

我本来想直奔讲解推理加速的章节的，但看了一眼全是公式，我还是老实地从头看起吧。

虽然我一向不喜欢从xxx原理开始介绍的书籍

在开始阅读这一系列之前，你可以先看看3blue1brown的视频：[But how do AI images and videos actually work? &#124; Guest video by Welch Labs
](https://youtu.be/iv-5mZ_9CPY?si=n8vbkBPiJDRM_YHl)

关于diffusion model，同事曾推荐我以下的资料：

- [Diffusion Models &#124; Paper Explanation &#124; Math Explained](https://www.youtube.com/watch?v=HoKDTa5jHvg&t=444s)
- [Flow Matching &#124; Explanation + PyTorch Implementation](https://www.youtube.com/watch?v=7cMzfkWFWhI)

如果没有兴趣看完两个长视频，可以直接看第二个。

> Diffusion modeling begins by specifying a forward corruption process that gradually turns data into noise. 
> This forward process links the data distribution to a simple noise distribution by defining a continuous family of intermediate distributions. 
> The core objective of a diffusion model is to construct another process that runs in the opposite direction, transforming noise into data while recovering the same intermediate distributions defined by the forward corruption process.

> We describe three complementary ways to formalize this idea. 

> **The variational view**, inspired by variational autoencoders, sees diffusion as learning to remove noise step by step, solving small denoising objectives that together teach the model to turn noise back into data. 

> **The score-based view**, rooted in energy-based modeling, learns the gradient of the evolving data distribution, which indicates how to nudge samples toward more likely regions. 

> **The flow-based view**, related to normalizing flows, treats generation as following a smooth path that moves samples from noise to data under a learned velocity field.

我同样也不喜欢这样引用原文，但我没有自信比这说的更精准。


### 参考文献

[1] The Principles of Diffusion Models: From Origins to Advances. arXiv preprint arXiv:2510.21890, 2025. https://arxiv.org/pdf/2510.21890