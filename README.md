# ControlNet-ECE570 Reimplementation of ControlNet for ECE570 term project


ControlNet Implementation on Mnist
========
## Project video (5min)
Link here-

## Sample Output for ControlNet with DDPM on MNIST
Canny Edge Control 

<img src="[https://github.com/user-attachments/assets/a52c53b3-b62e-4535-affa-1ee0d0321223](https://github.com/Shaunak-Mukherjee/ControlNet-ECE570/blob/main/Output%20Canny%20Hint.png)">

___

This repository implements ControlNet in PyTorch for diffusion models using Google Colab.
* Training and Inference of Unconditional DDPM on MNIST dataset
* Training and Inference of ControlNet with DDPM on MNIST using canny edges


## Setup
In Colab create a new conda environment with python 3.10 then run below commands
%pip install condacolab
import condacolab
condacolab.install()
Next, install packages from requirements.txt.
___  

## Data Preparation
### Mnist dataset found here https://www.kaggle.com/datasets/hojjatk/mnist-dataset
Ensure directory structure is following
```
ControlNet-ECE570/data/mnist/train/images/*/*.png
ControlNet-ECE570/data/mnist/test/images/*/*.png
```
---
## Configuration
 Allows you to play with different components of ddpm training
 ```config/mnist.yaml``` - Config for MNIST dataset

___  
## Training
The repo's MNist Colab file provides training and inference for Mnist(Unconditional DDPM) and ControlNet with both these variations using canny edges.

Once the config and dataset is setup:
For training and inference of Unconditional DDPM and for training and inference of ControlNet with Unconditional DDPM please follow, Colab file codeblocks.

## Training Unconditional DDPM
For training and inference of ddpmon mnist, ensure the right path is mentioned in `mnist.yaml` and simply follow the Colab code blocks.


## Training ControlNet for Unconditional DDPM
For training and inference of ddpmon mnist,ensure the right path is mentioned in `mnist.yaml` and simply follow the Colab code blocks


## Output
During training and inference of unconditional ddpm or ldm following output will be saved:
* During training we will save the latest checkpoint in ```task_name``` directory
* During sampling, unconditional sampled image grid for all timesteps in ```task_name/samples/*.png``` . The final decoded generated image will be `x0_0.png`. Images from `x0_999.png` to `x0_1.png` will be latent image predictions of denoising process from T=999 to T=1. Generated Image is at T=0

During training and inference of controlnet with ddpm/ldm following output will be saved:
* During training we will save the latest checkpoint in ```task_name``` directory
* During sampling, randomly selected hints and generated samples will be saved in ```task_name/hint.png``` and  ```task_name/controlnet_samples/*.png```. The final decoded generated image will be `x0_0.png`. Images from `x0_999.png` to `x0_1.png` will be latent image predictions of denoising process from T=999 to T=1. Generated Image is at T=0



## Citations
```
@misc{zhang2023addingconditionalcontroltexttoimage,
      title={Adding Conditional Control to Text-to-Image Diffusion Models}, 
      author={Lvmin Zhang and Anyi Rao and Maneesh Agrawala},
      year={2023},
      eprint={2302.05543},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2302.05543}, 
}
```

