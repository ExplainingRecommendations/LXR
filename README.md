# LXR

Learning to eXplain Recommendations (LXR) framework is a model-agnostic, post-hoc approach for explaining recommender systems. Being model-agnostic, LXR can work with any differentiable recommender. LXR does not require knowledge of the recommender's internal architecture or access to its parameters. Its sole prerequisite for the recommender model is its differentiability, and the ability to access the gradients with respect to the input. 
The LXR framework is based on an explainer model which is trained in order to produce explanation masks that score the significance of the user's personal data with respect to a recommended item. 

## A general overview 

![image](https://user-images.githubusercontent.com/130644098/233769872-571f3fd4-e02d-40ec-b3b4-16675db379eb.png)

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
+Create data to work with by running the Data_preparation notebook.
+Run either the MF or VAE notebooks that contain notebooks with these models.

## Baselines

In the Data_preprocessing folder, you can find a LIME Python file that implements LIME. For SHAP, we used the Python shap package. Keep in mind that you should create a WrapCustomModel for your specific model that you want to explain (your recommender). This takes as input your original input and transforms it into n_clusters dimension. Then after running your model, it should transform your results to num_items dimension to be passed to SHAP's KernelExplainer. 
All other classical baselines are oart of the main notebooks.




