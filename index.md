---
title: Home
layout: home
nav_order: 1
---

# watsonx.Governance Starter Lab

This quick tutorial guides you through the process of managing the lifecycle of a Home Pricing regression model using watsonx.governance. We'll cover both the optional creation of a new model and the management of an existing one, demonstrating how different roles within an organization interact with the AI governance process.

## Prerequisites

- Access to Cloud Pak for Data environment
- (Optional) Familiarity with Python for model creation

## Step 1 (OPTIONAL): Create and deploy your own Regression Model
Follow instructions [here](https://ashwinpo.github.io/watsonx-gov-lab/docs/Creating-a-Model.html)
If you decided to skip this step, please use the Home Pricing Random Forest Model that has already been created and deployed for the following steps.

## Step 2: Create an AI Use Case in watsonx.governance

**Role: Model Owner or Model Risk Manager**

1. Expand the left hamburger menu, select "AI use cases" under "AI Governance".
2. Click "New AI use case" and provide the following details:
   - Name: "Home Pricing Model"
   - Description: "Predicting Median Home Value to improve coverage assessment accuracy"
   - Owner: Select your username by searching for it
   - Use-Case Type: AI
   - Business Entities: Add State Farm Corp which is a glossary of business entities we've created as a sample
     
3. Click "Save" to establish the AI use case.

![New AI Use Case](../assets/images/New_AI_Use_Case.png)

## Step 3: Track the Model in watsonx.governance

**Role: Data Scientist or ML Engineer**

1. Expand the left hamburger menu, and go to Projects. If you created your own project, select that project. Otherwise, select the Project named "Lab Sample - Home Pricing".
2. Click on the model "HomePricing_LR".
**Note**: These next steps may already be done if you are using the Lab Sample project.
4. Click "Track asset" to associate it with your AI use case. 
5. Select the appropriate approach (Linear Regression for LR, Decision Tree for RF) and version for your model.
6. Create a New Record for this asset
7. Set is as experimental for now and save.
**Note**: These steps will now be applicable to all.
9. Export the AI Factsheet Report as a PDF by clicking the link in the top right and explore the provided document.
10. Click the arrow in the top right corner of the Governance tile to view details which will take you to the AI Use Case view again. Observe how this model is now in the development segment of the Lifecycle view.

## Step 5: Monitor and Manage the Model

**Role: MLOps Engineer and Data Scientist**

1. Expand the left hamburger menu, and go to Deployments. Go to Spaces and find the space you deployed or Lab Sample - Home Pricing if you skipped the model creation steps.
2. Click on a model's name to open its deployment details.
3. Navigate to the "Evaluations" tab 
4. Here we can see the following evaluation dimensions:
   - Mean Absolute Error (MAE)
   - Root Mean Square Error (RMSE)
   - R-squared (R²)
   - Feature importance
   - Data drift detection

## Conclusion

You've now explored some of the end-to-end lifecycle management of a regression model using watsonx.governance. This process ensures that your AI models are not only performant but also trackable, monitorable, and compliant with your organization's governance policies.


