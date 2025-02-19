# ECE570 term project

ControlNet Implementation on MNIST Dataset. This repository implements ControlNet in PyTorch for diffusion models using Google Colab. 
Training and Inference of DDPM on MNIST dataset and training and Inference of ControlNet with DDPM on MNIST using canny edges.


# Sample Output for ControlNet with DDPM on MNIST
Canny Edge Control https://github.com/Shaunak-Mukherjee/ControlNet-ECE570/blob/main/ControlNet_Cannyedge_genimage.png
![ControlNet_Cannyedge_genimage](https://github.com/user-attachments/assets/7883b187-cc46-4171-bbb5-702c49e76c8e)
A cool time evolution video- https://anonymous.4open.science/r/ControlNet-ECE570-D5C5/controlnet_time_evolution.mp4
This repository implements ControlNet in PyTorch for diffusion models using Google Colab. 
Training and Inference of DDPM on MNIST dataset and training and Inference of ControlNet with DDPM on MNIST using canny edges.

Key Project File Containing ALL code is - `Main_mnist.ipynb'
This file have step by step instruction that simply needs to be executed. 

# Setup
In Colab create a new conda environment with python 3.10 then run below commands
%pip install condacolab
import condacolab
condacolab.install()
Next, install packages from requirements.txt.
___  
# Data Preparation
# Mnist dataset found here 
[https://www.kaggle.com/datasets/hojjatk/mnist-dataset](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv)

Ensure directory structure is following
```
ControlNet-ECE570/data/mnist/train/images/*/*.png
ControlNet-ECE570/data/mnist/test/images/*/*.png
```
---
# Configuration
 Allows you to play with different components of ddpm training
 ```config/mnist.yaml``` - Config for MNIST dataset

___  
# Training
The repo's MNist Colab file provides training and inference for Mnist(Unconditional DDPM) and ControlNet with both these variations using canny edges.

Once the config and dataset is setup:
For training and inference of Unconditional DDPM and for training and inference of ControlNet with Unconditional DDPM please follow, Colab file codeblocks.

# Training Unconditional DDPM
For training and inference of ddpmon mnist, ensure the right path is mentioned in `mnist.yaml` and simply follow the Colab code blocks.

# Training ControlNet on Unconditional DDPM with Canny Hint Image
For training and inference of ddpmon mnist,ensure the right path is mentioned in `mnist.yaml` and simply follow the Colab code blocks

# Output
During training and inference of unconditional ddpm images will be saved under /ControlNet-ECE570/mnist/samples folder
The final decoded generated image will have file names as `x0_0.png,x0_2.png,... etc`.
During training we will save the latest checkpoint in ``` /ControlNet-ECE570/mnist/ ``` directory
During sampling, randomly selected hints and generated samples will be saved in ```/ControlNet-ECE570/mnist//hint.png``` and  ```/ControlNet-ECE570/mnist/controlnet_samples/*.png```. The final decoded generated image will be `x0_0.png,x0_2.png,... etc`.


