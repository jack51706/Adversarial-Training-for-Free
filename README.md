# Adversarial Training for Free

This is an unofficial PyTorch implementation of the paper "Adversarial Training for Free!".<br> 
https://128.84.21.199/pdf/1904.12843.pdf
It only contains the code for adversarial training on CIFAR-10. However one can easily modify it for other datasets. 
This is a really helpful technique which can significantly accelerate adversarial training.

## Overview

This repository contains two files. One for adversarial training and one for testing. Note that the model used here is not WideResNet 32-10 which is used in the paper 'Adversarial Training for Free'. I use WideResNet 28-10 which is used in the original PGD paper. Be aware that some of the hyperparameters are slightly different from the paper (weight decay and learning rate scheduling)

`checkpoint` [Google Drive](https://drive.google.com/file/d/1iZ52Ctcwty8bLMvLJJMlWcHL-__lJcbo/view?usp=sharing) 

## Accuracy (under PGD attack: epsilon = 8, step size = 2, iteration = 100)
| Model                      | Acc         |
| ---------------------------| ----------- |
| [ WideResNet 28-10 ]       | 46.93%      |

(I did not test every epoch's checkpoint. I simply chose from one of the last epochs to test. Results might be slightly better. I've also released the checkpoint. One can test it) 

## Dependencies
The repository is based on Python 3.5, with the main dependencies being PyTorch==1.0.0 Additional dependencies for running experiments are: numpy, tqdm, argparse, os, random, advertorch.

Advertorch can be installed from https://github.com/BorealisAI/advertorch<br>
Run the code with the command:<br>
```
$ CUDA_VISIBLE_DEVICES=0 python3 main.py 
```


