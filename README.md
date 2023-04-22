# LXR

Learning to eXplain Recommendations (LXR) framework is a model-agnostic, post-hoc approach for explaining recommender systems. Being model-agnostic, LXR can work with any differentiable recommender. LXR does not require knowledge of the recommender's internal architecture or access to its parameters. Its sole prerequisite for the recommender model is its differentiability, and the ability to access the gradients with respect to the input. 
The LXR framework is based on an explainer model which is trained in order to produce explanation masks that score the significance of the user's personal data with respect to a recommended item. 

## A general overview 

![LTR_model_2 (1)](https://user-images.githubusercontent.com/130644098/233772191-7252b1a1-da3e-482f-91d3-50318a511459.png)


## Repository

This repository contains code for a Learning to eXplain Recommendations (LXR) framework that was evaluated on two publicly available benchmarks, MovieLens1M and a subset of Yahoo!Music dataset, using two different recommenders, Matrix Factorization (MF) and Variational Auto Encoder (VAE). Hyperparameters optimization was done using optuna.

## Folders

* Data: contains the raw files for both datasets.
* Data_preprocessing: contains code related to the preprocessing step for preparing data to run with our models.
* MF: contains code related to model evaluation on MF.
* VAE: contains code related to model evaluation on VAE.

## Requirements

Before running the code, make sure to install all required packages and supported versions listed in the requirements.txt file.

## Usage

To use this code, follow these steps:
+ Create data to work with by running the Data_preprocessing notebooks.
+ Run either the MF or VAE notebooks that contain notebooks with these models.

## Baselines

* The Data_preprocessing folder contains a Python file for LIME implementation.
* We utilized Python's shap package for SHAP, using the KernelExplainer, and passing transformed data (in clusters dimension).
* The remaining classical baselines are included in the main notebooks.



