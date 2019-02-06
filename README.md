# ML-paper-summaries

2019 겨울부터 시작된 머신러닝 논문 스터디 내용을 정리하기 위한 파일입니다. 현재 [유시현](sihyun-yu.gihtub.io), [양수정](https://github.com/SoojungYang), [문석현](https://github.com/mseok), [김승수](https://github.com/SeungsuKim), [조재영](https://github.com/heartcored98) 총 5명이 진행하고 있습니다.

## Training Tips in DL

## Generative Model

## 1. Generative Adversarial Nets (2014, Ian J. Goodfellow) (유시현)

Discriminator와 Generator가 서로 게임을 한다고 생각하고 loss function을 정의하여 학습시키는 neural net 모델. 이 loss function은 결국 JS divergence를 optimize하는 것이 되며 초기 gradient가 거의 0이어서 학습이 되지 않는 것을 방지하기 위해서 discriminator의 loss에 log를 붙여 학습을 시켜주기도 함.

📄Paper Link : [Link](https://arxiv.org/pdf/1406.2661.pdf) 

🛠More Description : [Link](https://sihyun-yu.github.io/2018/12/17/GAN1/) (with recent study sketch)

💻Implementation : [Link](https://github.com/sihyun-yu/GANs-implementation) (Based on CS231n, Stanford) 

## 2. Wasserstein GAN (Martin Arjovsky, 2017) (유시현)

기존 loss function의 문제를 지적하고 EM distance라는 수학 개념에서 기안하여 loss function을 새로이 정의하여 학습함. 이렇게 정의되어 학습된 generative network는 기존의 Vanilla-GAN보다 학습이 더 stable하게 잘 되는 것을 확인할 수 있음.

📄Paper Link : [Link](https://arxiv.org/pdf/1701.07875.pdf)

🛠More Description : [Link](https://drive.google.com/drive/folders/1YIeiKe-I_S6skd3pat7PgIp2XRzMOTAD) (with slides)

## 3. Improved Training of Wasserstein GANs (Ishaan Gulrajani, 2017) (유시현)

WGAN을 train시킬 때 gradient를 단순히 clipping시켜서 학습시키는 것이 아니라 gradient penalty를 줘서 학습시키면 기존 WGAN보다 학습이 더 잘 된다는 논문. WGAN-GP(gradient penalty)라고 부름.

📄Paper Link : [Link](https://arxiv.org/pdf/1704.00028.pdf)

## 4. StackGAN: Text to Photo-realistic Image Synthesis with Stacked Generative Adversarial Networks (Han Zhang, 2016) (문석현)

Text to Image generation process에서 conditioning augmentation과 stacked structure를 통해 state-of-the-art 성능을 가지는 StackGAN이라는 모델에 대한 논문.

📄Paper Link : [Link](https://arxiv.org/pdf/1612.03242.pdf)

🛠More Description : [Link](https://drive.google.com/drive/folders/1YIeiKe-I_S6skd3pat7PgIp2XRzMOTAD) (with slides)

## NLP

## Reinforcement Learning

## Adversarial Attacks and Defenses

## 1. Adversarial Examples that Fool both Computer Vision and Time-Limited Humans (2018) (유시현)

딥러닝 공격하는 adversarial example을 인간에게도 짧은 시간동안만 보여주면 원본에 비해 구별을 잘 못한다는 내용이다. 즉 adversarial attack에 으로 만들어진 sample들을 짧은 시간 보여주었을 때 인간의 인지과정에서도 유의미한 차이를 나타낼 수 있다는 맥락의 논문.

📄Paper Link : [Link](https://arxiv.org/pdf/1802.08195.pdf)