# CoDefend

This repository provides the PyTorch implementation of CoDefend.

## Requirments
 - Python3
 - Pytorch
 - Torchvision

## Data
 - Download train and test datasets manually or they will be automatically downloaded from torchvision datasets.
 - Experiments are run on MNIST, HAM10000 and CIFAR10 datasets.
 - To use your own dataset: Move your dataset under data/ directory.

## Running the experiments

There are many parameters involved, please feel free to play with option.py.

This is an example:
   
 - To run the experiment on CIFAR10 with 5 clients including 2 malicious clients manipulating smashed data with 100 epochs and 300 batch size:
   ```sh
   python main.py --num_users 5 --malicious_client_number 2 --malicious_index 2 --dataset 'CIFAR10' --epochs 100 --batch_size 300

  ## Options
  The default values of the parameters used in the experiment are specified in options.py. Details of key parameters are described below:

 - `--lr`: learning rate, default 0.001.
 - `--batch_size`: number of batch size, default 256.
 - `--malicious_client_number`: number of the malicious client, default 0.
- `--num_users`: number of clients, default 2.
 - `--epochs`: number of epochs, default 10.
