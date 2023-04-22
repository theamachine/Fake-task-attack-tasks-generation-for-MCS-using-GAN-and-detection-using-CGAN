# Fake task attack tasks generation for MCS using GAN and detection using CGAN
## Background:  
Fake task attack is critical for Mobile Crowdsensing system (MCS) that aim to clog the sensing servers in the MCS platform and drain more energy from participants’ smart devices. Typically, fake tasks are created by empirical model such as CrowdSenSim tool. Recently, cyber criminals deploy more intelligent mechanisms to create attacks. Generative Adversarial Network (GAN) is one of the most powerful techniques to generate synthetic samples. GAN considers the entire data in the training dataset to create similar samples. This project aims to use GAN to create fake tasks and verify fake task detection performance.  
## Introduction:  
The objective of this project is to generate intelligent fake tasks by GAN. Meanwhile, you need to evaluate detection accuracy for original fake tasks and GAN-generated fake tasks. Detection
mechanisms contains classic machine learning (ML) models (e.g., Random Forest (RF) and Adaboost) and a GAN-based cascade detection framework. Another objective is to compare traditional MLs and the cascade detection framework detection performance.
Traditional ML models (RF and Adaboost)-based detection methods are considered as bench marks. This project focuses on the GAN-based cascade framework which is demonstrated in Figure 1. The cascade framework is proposed that implements a two-level cascaded classifier architecture to predict the generated attack samples and original (empirically designed) attack samples and filter them before distributing them to MCS participants.
The first level is formed by the GAN discriminator whereas the second level is a binary classifier. According to Figure 1, the training dataset is utilized to train binary classifiers (e.g., RF, Adaboost) and GAN. The training dataset includes original fake tasks. GANs take input samples of noise, and output adversarial (i.e., synthetic) samples. GAN consists of a Generator neural network and a Discriminator neural network. The role of the generator is to create synthetic samples as similar as the real ones whereas a Discriminator designs to distinguish real samples from the synthetic ones. The motive for the competition is to reduce the gap between generated samples for Generator and increase detection accuracy for Discriminator.
![image](https://user-images.githubusercontent.com/48517382/233803195-5f6e7a67-d5f9-4c3a-b6ac-ce91493b417e.png)
This project has the following objectives:  
1.	Understand GAN model working procedure  
2.	Implement GAN model (e.g., Conditional GAN (CGAN ))  
3.	Generate fake tasks via CGAN  
4.	Verify RF and Adaboost fake task detection performance, including original fake tasks and GAN- based fake tasks  
5.	Verify the cascade framework detection performance for original fake tasks and GAN-based fake tasks
![image](https://user-images.githubusercontent.com/48517382/233803261-2969dc02-f4f1-4597-96c7-584e70290a38.png)
![image](https://user-images.githubusercontent.com/48517382/233803271-f9acc807-2631-4795-8a05-c9037bee1f71.png)
