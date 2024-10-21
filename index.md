---
title: Home
layout: home
---

# watsonx.Governance Starter Lab

This tutorial guides you through the process of creating, deploying, and monitoring a premium regression model using IBM Watson Studio and watsonx.governance. We'll use a pre-built Jupyter notebook to train our model and then walk through the steps to manage its lifecycle.

## Step 1: Set Up Your Watson Studio Project

1. Log into Cloud Pak for Data
2. Create a new project by clicking on "New project" and selecting "Create an empty project".
3. Give your project a name and description, then select a Cloud Object Storage service.

## Step 2: Import the Jupyter Notebook

1. In your project, click on "Add to project" and select "Notebook".
2. Choose "From file" and upload the provided `premium_regression_model.ipynb` file.
3. Select the runtime environment (preferably Python 3.x with GPU support) and click "Create".

## Step 3: Run the Notebook

1. Open the imported notebook.
2. Read through the notebook to understand the premium regression problem and dataset.
3. Run each cell in order, following any instructions within the notebook.
4. The notebook will guide you through data preprocessing, model training, and initial evaluation.

## Step 4: Create an AI Use Case in watsonx.governance

1. Navigate to watsonx.governance from your IBM Cloud dashboard.
2. Click on "AI Governance" in the left menu, then "AI use cases".
3. Click "New AI use case" and fill in the details:
   - Name: Premium Regression Model
   - Description: Predicting insurance premiums based on customer data
   - Risk level: Medium (adjust as needed)
   - Select the appropriate inventory

## Step 5: Track the Model in watsonx.governance

1. In your Watson Studio project, locate your trained model.
2. Click on the model and select "View AI factsheet".
3. Click "Track asset" to associate it with your AI use case.
4. Select the appropriate approach and version for your model.

## Step 6: Deploy the Model

1. In Watson Studio, go to your project's "Deployments" tab.
2. Click "New deployment space" and set it up for production.
3. Find your model in the project assets, click the three dots, and select "Promote to space".
4. In the deployment space, deploy the model by clicking the three dots next to it and selecting "Deploy".

## Step 7: Monitor and Manage the Model

1. In the deployment space, find your deployed model.
2. Click on the model, go to the "Evaluations" tab, and click "Activate".
3. Set up the evaluation dimensions relevant to premium regression (e.g., Mean Absolute Error, R-squared).
4. Review the payload and feedback data schema, then click "Activate" to start monitoring.

## Step 8: Test the Deployed Model

1. In the deployment space, go to your model's "Test" tab.
2. Enter sample input data to test the premium prediction.
3. Review the results to ensure they make sense for your use case.

## Step 9: Continuous Monitoring

1. Regularly check the "Monitoring" dashboard for your model.
2. Pay attention to performance metrics, data drift, and model health.
3. Set up alerts for critical thresholds to be notified of any issues.

## Step 10: Reporting and Compliance

1. To generate a report on your model's current state:
   - Go to your model in the deployment space.
   - Click on the "AI Factsheet" tab.
   - Select "Export report" and choose your preferred format.
2. Use these reports for internal reviews or compliance purposes.

## Conclusion

You've now successfully created, deployed, and set up monitoring for a premium regression model using IBM Watson Studio and watsonx.governance. This process ensures that your model is trackable, monitorable, and compliant with your organization's AI governance policies.

Remember to regularly review your model's performance and make updates as necessary to maintain its accuracy and reliability in predicting insurance premiums.

For any issues or questions, please refer to the IBM Watson Studio and watsonx.governance documentation or contact IBM support.
