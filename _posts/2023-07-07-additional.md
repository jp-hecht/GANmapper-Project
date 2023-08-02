---
layout: post
title: 'Additional Ressources'
subtitle: 'Some more tipps & tricks'
date: 2023-07-30 9:45:20 -0400
background: '/img/data_bw.jpg'
author: Jonathan Hecht
---

## How to advance our results with the second pre-processd dataset:
We have upload their GitHub Repo and our data sets to the filecloud of the our university. The following link should open a ZIP-file, which you could download:
* [Link](https://cloud.hcu-hamburg.de/nextcloud/s/w9yNWje5KqH5oyK)
* Password: *feel free to contact us (jonathan.hecht@hcu-hamburg.de)*

#### Install the repo
1. Unzip the folder to your favorite directory
2. Use `environment.yml` to create a conda environment for GANmapper

  ```sh
  conda env create -f environment.yml
  conda activate ganmapper_project
  ```
3. Change working directory to *ganmapper_project*
4. Testing with some sample data from LA. Results are in the *"./results/LA/test_latest/images"* folder. If the prediction is not immediatly working follow step 5..

```sh
python predict.py --dataroot datasets/test/LA/Source --checkpoints_dir checkpoints/Exp3 --name LA 
# or without a gpu
python predict.py --dataroot datasets/test/LA/Source --checkpoints_dir checkpoints/Exp3 --name LA --gpu_ids -1
```
5. Manually install some necessary packages (I have not tried to add these to the .yml). On my local machine I just had to install *tqdm*. On Google Colab I had to install some more packages. I have listed both packages below:

```sh
# locally 
pip install tqdm

# colab
!pip install torch
!pip install numpy
!pip install Pillow
!pip install torchvision
!pip install dominate
!pip install visdom

```
6. Hurray, your installation should be complited!

#### Run experiments with 'default' parameters

```sh
# cd to your ganmapper_project folder
conda activate ganmapper_project

# first experiment
python train.py --dataroot ./datasets/exp_high/ --name exp_high --model pix2pix --direction AtoB --crop_size 256 --load_size 260 --n_epochs 100 --n_epochs_decay 100 --netG resnet_9blocks

# second experiment
python train.py --dataroot ./datasets/exp_low/ --name exp_low --model pix2pix --direction AtoB --crop_size 256 --load_size 260 --n_epochs 100 --n_epochs_decay 100 --netG resnet_9blocks

# third experiment
python train.py --dataroot ./datasets/exp_medium/ --name exp_medium --model pix2pix --direction AtoB --crop_size 256 --load_size 260 --n_epochs 100 --n_epochs_decay 100 --netG resnet_9blocks

```
#### Known problems
* The visdom packages refuses to establish a connection. Just ignore this messages. It will run despite of this message.
 