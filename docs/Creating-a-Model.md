---
title: Creating a Model
nav_order: 2
---
# Creating a Model for tracking in watsonx.governance

This tutorial guides you through the process of creating a Home Pricing regression model using Projects on Cloud Pak for Data via an existing Jupyter Notebook.


## Step 1: Create a Deployment Space


## Step 2: Set Up Your Project

**Role: Data Scientist or ML Engineer**

1. Log into Cloud Pak for Data using your credentials.
2. In the top-left corner, click on the hamburger menu and select "Projects".
3. Click "New project" and select "Create an empty project".
4. Provide a meaningful name with your initials (e.g., "Home Pricing Dev - AP") and description for your project.
5. Click "Create" to finalize the project setup.

## Step 3: Import the Jupyter Notebook (Optional for Model Creation)

**Role: Data Scientist**

If you're creating a new model:

1. In your project, click "Add to project" in the top-right corner and select "Notebook".
2. Choose "From URL" and enter this URL: `https://github.com/ashwinpo/watsonx-gov-lab/blob/main/Housing%20Modeling.ipynb`.
3. For the runtime environment, select one of the runtimes with Python 3.11.
4. Click "Create" to import the notebook.

## Step 4: Run the Notebook

**Role: Data Scientist**

If you're creating a new model:

1. Open the imported notebook.
2. Execute each cell in order, following any inline instructions.
3. You will need to add your user credentials to one of the code blocks when deploying the model from code.
4. After running all cells, you should have a trained Home Pricing regression model saved in your project.
5. Download the training and testing files locally.

## Step 5: Setup Monitoring for the Model
**Role: Data Scientist**


