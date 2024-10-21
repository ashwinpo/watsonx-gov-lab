---
title: Creating a Model
nav_order: 2
---
# Creating a model in Watson Studio

# watsonx.Governance Starter Lab

This tutorial guides you through the process of creating a premium regression model using IBM Watson Studio via an existing Jupyter Notebook.

## Step 1: Set Up Your Watson Studio Project (Optional for Model Creation)

**Role: Data Scientist or ML Engineer**

1. Log into Cloud Pak for Data using your credentials.
2. In the top-left corner, click on the hamburger menu and select "Projects".
3. Click "New project" and select "Create an empty project".
4. Provide a meaningful name (e.g., "Premium Regression Governance") and description for your project.
5. Choose an existing Cloud Object Storage service or create a new one if prompted.
6. Click "Create" to finalize the project setup.

## Step 2: Import the Jupyter Notebook (Optional for Model Creation)

**Role: Data Scientist**

If you're creating a new model:

1. In your project, click "Add to project" in the top-right corner and select "Notebook".
2. Choose "From file" and upload the provided `premium_regression_model.ipynb` file.
3. For the runtime environment, select Python 3.x (preferably with GPU support for faster computation).
4. Click "Create" to import the notebook.

## Step 3: Run the Notebook (Optional for Model Creation)

**Role: Data Scientist**

If you're creating a new model:

1. Open the imported `premium_regression_model.ipynb` notebook.
2. Carefully read through each cell to understand the premium regression problem, dataset, and modeling approach.
3. Execute each cell in order, following any inline instructions.
4. Pay special attention to:
   - Data preprocessing steps
   - Feature engineering techniques
   - Model selection and hyperparameter tuning
   - Evaluation metrics relevant to premium prediction (e.g., Mean Absolute Error, R-squared)
5. After running all cells, you should have a trained premium regression model saved in your project.


**Note:** If you decided to skip the previous steps, please use the Pure Premium Sample Model that has already been created and deployed for the following steps.
