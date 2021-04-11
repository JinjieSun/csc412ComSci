# **A Short Introduction to Generative Models**
Jinjie Sun 

## **Properties of Generative Models**
People are familiar with classifying a machine learning model  as supervised, unsupervied or reinforcement learning models based on the model's data type and model structure. Another way to distinguish the machine learning models is based on the model's output, and classify it as discriminative model or generative model.
### **Generative vs Discriminative Models**
For the discriminative model, the task is to identify the labels of a given image. For example, an image classification model is a discriminative model. In other words, the discriminative model is trying to learn the distribution of the label with given data, which is p(y|x).
Generative model, on the other hand, will output a new data sampled from the learned distribution. The learned distribution can be the joint distribution of data and label P(x, y) or simply the data itself p(x), if no labels are provided. 
### **Why we need Generative Models**
One significant advantage of the generative model is that it can create new data. If we train the model correctly, the new data will capture the structures of the original data. Therefore, if we want to do data forecasting or let the model doing a creative job, such as generate a piece of music with similar styles of a famous composer, then the generative model will do a great and surprisingly good job. 

## **Examples of Generative Model**
Variational Autoencoder and Generative Adversarial Networks are mainly used models in many areas with all kinds of generative models. In the following sections, we will briefly explain the structure of these two models, how they are trained, and their properties.
### **VAE**
#### **Model Structure**
Variational Autoencoder, also called VAE, has an encoder-decoder structure that comes from autoencoder. The autoencoder contains two parts, an encoder that maps the input data into a latent space and a decoder that generates output from latent space. In general, the latent space has a lower dimension than the input data. The transformations of the autoencoder model are linear that we can view the encoder and decoder as two matrices. The output of the autoencoder usually has the same dimension as input data.

![alt text][logo]

[logo]: ./autoencoder_structure.png "AutoEncoder Structure"

For VAE, we increase the model complexity by replacing encoder and decoder with deep neural networks, where the encoder learns the distribution of latent states given the input $p_{\theta}(z|x)$, and the decoder learns the distribution of output given the sampled latent vectors $q_{\theta}(x|\hat{z})$, where $\hat{z} \sim p_{\theta}(z|x)$. The choice of deep neural networks can be variate according to different tasks, such as adding LSTM cells for time series data or an MLP for general purposes.

#### **Training Process**
#### **Model Features**

### **GAN**
#### **Model Structure**
#### **Training Process**
#### **Model Features**

## **Applications of Generative MOdels**

### **VAE**
### **GAN**

## **Summary**

## References
1. Brownlee, J. (2019, July 19). A gentle introduction to generative adversarial networks (gans). Retrieved April 11, 2021, from https://machinelearningmastery.com/what-are-generative-adversarial-networks-gans/
2. Jeremy Jordan. (2018, July 16). Variational autoencoders. Retrieved April 11, 2021, from https://www.jeremyjordan.me/variational-autoencoders/
3. 