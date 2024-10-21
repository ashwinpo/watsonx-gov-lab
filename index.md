---
title: Home
layout: home
---

# watsonx.Governance Starter Lab

This comprehensive tutorial guides you through the process of managing the lifecycle of a premium regression model using IBM Watson Studio and watsonx.governance. We'll cover both the optional creation of a new model and the management of an existing one, demonstrating how different roles within an organization interact with the AI governance process.

## Prerequisites

- Access to Cloud Pak for Data environment
- (Optional) Familiarity with Python for model creation

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

## Step 4: Create an AI Use Case in watsonx.governance

**Role: Model Owner or Model Risk Manager**

1. From the Cloud Pak for Data dashboard, navigate to watsonx.governance.
2. In the left menu, expand "AI Governance" and click "AI use cases".
3. Click "New AI use case" and provide the following details:
   - Name: "Premium Regression Model Lifecycle"
   - Description: "End-to-end management of a model predicting insurance premiums based on customer data"
   - Risk level: Medium (adjust based on your organization's risk assessment)
   - Inventory: Select an appropriate existing inventory or create a new one
4. Click "Create" to establish the AI use case.

## Step 5: Track the Model in watsonx.governance

**Role: Data Scientist or ML Engineer**

1. In your Watson Studio project, locate your premium regression model (either the one you created or an existing one).
2. Click on the model name to open its details page.
3. On the right side of the page, click "View AI factsheet".
4. In the AI factsheet view, click "Track asset" to associate it with your AI use case.
5. Select the appropriate approach (e.g., "Regression Analysis for Premium Prediction") and version for your model.
6. Confirm the tracking to enable governance features for this model.

## Step 6: Deploy the Model

**Role: MLOps Engineer**

1. From your Watson Studio project, click on the "Deployments" tab.
2. Click "New deployment space" and configure it for production use:
   - Provide a name (e.g., "Premium Model Production Space")
   - Select the appropriate Cloud Object Storage
   - Set the space type to "Production"
3. Once created, find your premium regression model in the project assets.
4. Click the three dots next to the model and select "Promote to space".
5. Choose the production deployment space you just created.
6. In the deployment space, locate the promoted model.
7. Click the three dots next to it and select "Deploy".
8. Configure the deployment settings (e.g., number of replicas, hardware size) based on your expected load.
9. Click "Create" to initiate the deployment.

## Step 7: Monitor and Manage the Model

**Role: MLOps Engineer and Data Scientist**

1. In the deployment space, find your deployed premium regression model.
2. Click on the model name to open its deployment details.
3. Navigate to the "Evaluations" tab and click "Activate".
4. Set up the following evaluation dimensions:
   - Mean Absolute Error (MAE)
   - Root Mean Square Error (RMSE)
   - R-squared (R²)
   - Feature importance
   - Data drift detection
5. Review the payload schema, ensuring it matches your model's input requirements.
6. Set up the feedback data schema to capture actual premium values for comparison.
7. Click "Activate" to initiate continuous monitoring.

## Step 8: Test the Deployed Model

**Role: Quality Assurance Engineer or Data Scientist**

1. In the deployment space, go to your model's "Test" tab.
2. Prepare a set of diverse test cases covering different customer profiles.
3. Enter sample input data for each test case, including:
   - Age
   - BMI
   - Number of children
   - Smoking status
   - Region
4. Click "Predict" for each test case and review the predicted premium.
5. Assess the results for reasonableness and consistency with domain knowledge.
6. Document any unexpected predictions for further investigation.

## Step 9: Continuous Monitoring

**Role: MLOps Engineer and Data Scientist**

1. Regularly access the "Monitoring" dashboard for your deployed model.
2. Pay close attention to:
   - Performance metrics trends (MAE, RMSE, R²)
   - Data drift indicators for input features
   - Model health scores
   - Prediction distribution changes
3. Set up alerts for critical thresholds:
   - Performance degradation (e.g., 10% increase in MAE)
   - Significant data drift (e.g., > 0.1 drift score for key features)
   - Unusual prediction patterns (e.g., sudden increase in high-premium predictions)
4. Establish a review process for triggered alerts, involving both technical and business stakeholders.

## Step 10: Reporting and Compliance

**Role: Model Risk Manager or Compliance Officer**

1. To generate a comprehensive report on your model's current state:
   - Navigate to your model in the deployment space
   - Click on the "AI Factsheet" tab
   - Select "Export report" and choose your preferred format (e.g., PDF for easy sharing)
2. Customize the report to include:
   - Model performance metrics
   - Data drift analysis
   - Feature importance over time
   - Alert history and resolutions
   - Model retraining log
3. Use these reports for:
   - Regular model review meetings
   - Audit trail documentation
   - Regulatory compliance evidence
   - Stakeholder communications

## Conclusion

You've now explored the end-to-end lifecycle management of a premium regression model using IBM Watson Studio and watsonx.governance. This process ensures that your AI models are not only performant but also trackable, monitorable, and compliant with your organization's governance policies.

Key takeaways:
- AI governance is a collaborative effort involving multiple roles
- Continuous monitoring is crucial for maintaining model reliability
- Regular reporting supports transparency and compliance efforts


