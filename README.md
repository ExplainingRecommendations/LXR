# Learning to eXplain Recommendations (LXR)

LXR framework is a model-agnostic, post-hoc approach for explaining recommender systems. Being model-agnostic, LXR can work with any differentiable recommender. LXR does not require knowledge of the recommender's internal architecture or access to its parameters. Its sole prerequisite for the recommender model is its differentiability, and the ability to access the gradients with respect to the input. 
The LXR framework is based on an explainer model which is trained in order to produce explanation masks that score the significance of the user's personal data with respect to a recommended item. 

## A general overview 

![LXR_diagram](https://github.com/ExplainingRecommendations/LXR/assets/130644098/ec92edb8-4996-4e46-b1ce-f5795b8e53ef)


## Repository

This repository contains code for a Learning to eXplain Recommendations (LXR) framework that was evaluated on two publicly available benchmarks, MovieLens1M and a subset of Yahoo!Music dataset, using two different recommenders, Matrix Factorization (MF) and Variational Auto Encoder (VAE). Hyperparameters optimization was done using optuna.

## Folders

* **Data**: contains the raw files for both datasets.
* **Data_preprocessing**: contains code related to the preprocessing step for preparing data to run with our models.
* **MF**: contains code related to model evaluation on MF.
* **VAE**: contains code related to model evaluation on VAE.

## Requirements

* python 3.10
* Pytorch 1.13

## Usage

To use this code, follow these steps:
+ Create data to work with by running the Data_preprocessing notebooks.
+ Run either the MF or VAE notebooks that contain notebooks with these models.




