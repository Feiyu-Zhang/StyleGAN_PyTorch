# A PyTorch Implementation of StyleGAN (Unofficial)

![Github](https://img.shields.io/badge/PyTorch-v1.0.1-green.svg?style=for-the-badge&logo=data:image/png)
![Github](https://img.shields.io/badge/python-3.6-green.svg?style=for-the-badge&logo=python)
![Github](https://img.shields.io/badge/status-WorkInProgress-blue.svg?style=for-the-badge&logo=fire)
![Github](https://img.shields.io/badge/license-CC_BY--NC-green.svg?style=for-the-badge&logo=fire)

This repository contains a PyTorch implementation of the following paper:
> **A Style-Based Generator Architecture for Generative Adversarial Networks**<br>
> Tero Karras (NVIDIA), Samuli Laine (NVIDIA), Timo Aila (NVIDIA)<br>
> http://stylegan.xyz/paper
>
> **Abstract:** *We propose an alternative generator architecture for generative adversarial networks, borrowing from style transfer literature. The new architecture leads to an automatically learned, unsupervised separation of high-level attributes (e.g., pose and identity when trained on human faces) and stochastic variation in the generated images (e.g., freckles, hair), and it enables intuitive, scale-specific control of the synthesis. The new generator improves the state-of-the-art in terms of traditional distribution quality metrics, leads to demonstrably better interpolation properties, and also better disentangles the latent factors of variation. To quantify interpolation quality and disentanglement, we propose two new, automated methods that are applicable to any generator architecture. Finally, we introduce a new, highly varied and high-quality dataset of human faces.*

![Teaser image](utils/stylegan-teaser.png)
Picture: These people are not real – they were produced by our generator that allows control over different aspects of the image.

## Motivation
To the best of my knowledge, there is still not a similar pytorch 1.0 implementation of styleGAN as NvLabs released(Tensorflow),
therefore, i wanna implement it on pytorch1.0.1 to extend its usage in pytorch community.

## Author

- [Samuel Ko](https://blog.csdn.net/g11d111)
- [Sunner Li](https://github.com/SunnerLi)

## Training

``` python
# ① pass your own dataset of training, batchsize and common settings in TrainOpts of `opts.py`.

# ② run train_stylegan.py
python3 train_stylegan.py

# ③ you can get intermediate pics generated by stylegenerator in `opts.det/images/`
```

## Unfinished

* ① `blur2d` mechanism still not available.

## Related
[1. StyleGAN - Official TensorFlow Implementation](https://github.com/NVlabs/stylegan)

[2. The re-implementation of style-based generator idea](https://github.com/SunnerLi/StyleGAN_demo)


## System Requirements
- Ubuntu18.04
- PyTorch 1.0.1
- Numpy 1.13.3
- torchvision 0.2.1
- GTX 1080Ti or above

## Q&A

## Acknowledgements
Our code can run `1024 x 1024` resolution image generation task in single 1080Ti, if you have stronger graphic card or GPU, then
you may train your model with large batchsize and self-define your multi-gpu version of this code.

My Email is **samuel.gao023@gmail.com**, if you have any question and wanna to PR, please let me know, thank you. 
