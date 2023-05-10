# Azure Machine Learning Engineer - Capstone Project

This project is the capstone project of Udacity's *Machine Learning Engineer with Microsoft Azure* nanodegree. 
The scope of the project is to present the knowledge obtained from finishing the courses.

## Project Set Up and Installation

Setting up the project in Azure ML:
1. Create new or access a workspace in Azure with your subscription
2. Open Azure Machine Learning Studio
3. Create a Compute instance so you can run your jupyter notebooks
4. Starter files were provided by Udacity, you can find them in [this repository](https://github.com/udacity/nd00333-capstone/tree/master/starter_file)

## Dataset

### Overview

The dataset contains information about visual characteristics of cancerous cells in the breast and ground truth about the diagnosis made based on the cell data. The visuals were measured based on X-rays.

[*Source*](https://www.kaggle.com/datasets/yasserh/breast-cancer-dataset)

### Task

Based on the data we can create a classification model, so if we input the visual characteristics, a diagnosis can be made, whether the cell is benign or malignant.

### Access
*TODO*: Explain how you are accessing the data in your workspace.

For the Automated ML I have uploaded the dataset into the Azure ML Studio as a dataset. For the hyperdrive training I have uploaded the file and read it with pandas.

## Automated ML
*TODO*: Give an overview of the `automl` settings and configuration you used for this experiment
For the Automated Machine Learning, I have used the following settings and configuration.

Settings:
- *experiment_timeout_minutes*: 20 (stop after 20 mins of inactivity)
- *max_concurrent_iterations*: 5 (maximum 5 different models run at the same time)
- *primary_metric*: AUC_weighted (the metric based on which the AutoML will choose which model performs the best)
 
Configuration:
- *task*: Classification
- *label_column_name*: diagnosis (this is the column in the dataset that needs to be classified)
- *enable_early_stopping*: True (stop if the models do not improve 

### Results
*TODO*: What are the results you got with your automated ML model? What were the parameters of the model? How could you have improved it?

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Hyperparameter Tuning
*TODO*: What kind of model did you choose for this experiment and why? Give an overview of the types of parameters and their ranges used for the hyperparameter search


### Results
*TODO*: What are the results you got with your model? What were the parameters of the model? How could you have improved it?

*TODO* Remeber to provide screenshots of the `RunDetails` widget as well as a screenshot of the best model trained with it's parameters.

## Model Deployment
*TODO*: Give an overview of the deployed model and instructions on how to query the endpoint with a sample input.

## Screen Recording
*TODO* Provide a link to a screen recording of the project in action. Remember that the screencast should demonstrate:
- A working model
- Demo of the deployed  model
- Demo of a sample request sent to the endpoint and its response

## Standout Suggestions
*TODO (Optional):* This is where you can provide information about any standout suggestions that you have attempted.
