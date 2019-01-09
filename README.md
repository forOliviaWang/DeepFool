# Fooling Computer Vision in Autonomous Vehicles

This project have been developed for a Computer Science course on Cybersecurity from the engineering school CentraleSupélec. 
This projet is based on the Github Project [DeepFool](https://github.com/LTS4/DeepFool).

# Installation
This project require some dependencies.
Ensure that you have python3 and pip, then run:
```bash
pip3 install -r requirements.txt

```
Note : This command will install Torch, ~500MB  

You will also need tkinter
```bash
sudo apt-get install python-tk python3-tk
```

# Function descripion

## deepfool.py

This function implements the algorithm proposed in [[1]](http://arxiv.org/pdf/1511.04599) using PyTorch to find adversarial perturbations.

__Note__: The final softmax (loss) layer should be removed in order to prevent numerical instabilities.

The parameters of the function are:

- `image`: Image of size `HxWx3d`
- `net`: neural network (input: images, output: values of activation **BEFORE** softmax).
- `num_classes`: limits the number of classes to test against, by default = 10.
- `max_iter`: max number of iterations, by default = 50.

## test_deepfool.py

A simple demo which computes the adversarial perturbation for a test image from ImageNet dataset.

## Reference
[1] S. Moosavi-Dezfooli, A. Fawzi, P. Frossard:
*DeepFool: a simple and accurate method to fool deep neural networks*.  In Computer Vision and Pattern Recognition (CVPR ’16), IEEE, 2016.
