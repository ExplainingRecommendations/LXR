# Learning to eXplain Recommendations (LXR)

LXR is a model-agnostic, post-hoc framework to explain recommender systems. LXR can work with any differentiable recommender and learns to score the importance of users' personal data with respect to a recommended item. The framework's objective employs a novel self-supervised counterfactual loss function that aims to identify the user data that best explains the item's recommendation. Additionally, we propose several counterfactual evaluation metrics for assessing explanations in recommender systems. Using these metrics, our results demonstrate LXR's capability to provide counterfactual explanations for various recommendation algorithms across different datasets.

## A general overview 

![last_model](https://github.com/ExplainingRecommendations/LXR/assets/130644098/7b3e1511-f3d6-40c9-9563-d6583b0aaee8)

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




