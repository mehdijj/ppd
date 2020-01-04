# PPD: Permutation Phase Defense Against Adversarial Examples in Deep Learning
This repository provides implementation of the following paper: https://arxiv.org/abs/1812.10049



## How to run:
1. To train a model on the phase of permuted images, you need to run the ``main_mnist.py`` for MNIST dataset and ``main_cifar10.py`` for CIFAR10. For example, running

``python main_mnist.py --nb_epochs=100 --permutation_seed_list=100,101,102``

from the command line trains 3 models with permutation seeds 100,101,102 on MNIST dataset and saves them in ``Adversarial Attack >> saved_models >> mnistdense.`` Training for 10 different permutation seeds can approximately reproduce the results in the paper.


2. To test a saved model against adversarial attacks, you need to follow the instruction in ``Adversarial Attacks >> MNIST >> blackbox.py`` for blackbox attack and ``Adversarial Attacks >> MNIST >> new_dense_ensemble_load.ipynb`` for some of other attacks.
