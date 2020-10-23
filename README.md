# ALFA - Meta-Learning with Adaptive Hyperparameters
#### Sungyong Baik, Myungsub Choi, Janghoon Choi, Heewon Kim, Kyoung Mu Lee

Source code for NeurIPS 2020 paper "Meta-Learning with Adaptive Hyperparameters" (previously titled "Adaptive Learning for Fast Adaptation")

This repository is the implementation of ALFA.
The code is based off the public code of MAML++, where their reimplementation of MAML is used as the baseline.

## Requirements

- Ubuntu 18.04
- Anaconda3
- Python==3.6
- PyTorch==1.5
- numpy==1.19.1

## Hardware Requirements

- GPU with memory more than 27GB for a single-GPU ResNet12 training.


To install requirements, first download Anaconda3 and then run the following:

```setup
bash install.sh
```

## Datasets
For miniIamgenet, the dataset can be downloaded from the link provided from MAML++ public code.
make a directory named 'datasets' and place the downloaded miniImagnet under the 'datasets' directory.


## Training

To train the model(s) in the paper, run this command in experiment_scripts folder:

For single GPU
```train
bash alfa+maml.sh 0
```
where 0 represent GPU_ID.

For multi-GPU,

```train
bash alfa+maml.sh 0 1 2 3
```
where 0 1 2 3 represent 4 GPU_IDs.


## Evaluation

After training is finished, the same command is run to evaluate:

For single GPU:
```eval
bash alfa+maml.sh 0
```
For multi-GPU:
```eval
bash alfa+maml.sh 0 1 2 3
```
where 0 1 2 3 represent 4 GPU_IDs.
