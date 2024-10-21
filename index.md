---
title: Home
layout: home
---

In this article, I describe how IBM watsonx.governance empowers organizations to establish an enterprise AI model inventory and enables evaluation and continuous model performance assurance. Model inventory collects and organizes metadata about AI models throughout the lifecycle. Therefore, the model inventory allows organizations to respond to regulatory scrutiny and concerns with evidence quicker, thereby containing any financial penalties. Continuous model performance assurance enables organizations to manage risk and prevent loss exposures due to AI, maintain brand image, and be socially responsive, free of bias and discrimination.

I cover the entire lifecycle flow of model build (adapt and test), evaluate, approve, deploy, monitor, and manage using the IBM watsonx platform for a given use case.

I describe the end-to-end lifecycle to adapt Generative AI Foundational Models (or Large Language Models) leveraging prompt engineering techniques such as zero-shot, one-shot, or few-shot prompting for a specific use case.

I close this article by covering approaches on how to ultimately infuse and operationalize AI in existing business applications and workflows by performing inference using a fit-for-purpose adapted Generative AI Foundation Model and how to ensure the usage of AI is trustworthy and responsive continuously.

A typical AI model follows the following lifecycle:


The AI life cycle for adaptation of Generative AI Foundational Models
Tips:

To access the IBM watsonx.ai GA environment, click here and log in using your IBM ID.

Getting Started with IBM watsonx
The section describes the key steps to start with IBM watsonx.

Once logged in to the IBM Cloud, search for watsonx in the IBM Cloud Catalog and click on the watsonx tile.

IBM Cloud Catalog
2. Once the watsonx screen is displayed, click Launch in the watsonx.ai tile.


IBM watsonx.ai
3. To start with watsonx.governance, search watsonx.governance in the IBM Cloud Catalog, then click on the watsonx.governance tile. Select the right plan and click on the Create button to create the watsonx.governance service.


IBM Cloud Catalog

Available subscription plans for the watsonx.governance service
4. Once watsonx.governance service is created, click on the Launch watsonx.governance button to monitor Generative AI Foundation Models.


Launching of watsonx.governance for monitoring Generative AI Foundation Models or Large Language Models
Next, let me introduce the business use case used in this article to showcase the usage of Generative AI Foundation Models and their model lifecycle management.

Use Case Definition
A large car rental company has embarked on the “Customer of One” initiative and started vigorously requesting customer comments and feedback during checkout and return of the car rentals. To improve and personalize the customer experience, the company’s customer experience and marketing departments would like to understand whether customers were satisfied with their rental experience based on customer comments collected.

Model Lifecycle Management Approach
Step 1: Propose an AI use case

In this step, the Model Requestor or the Model Owner proposes an AI use case.

Once IBM watsonx.ai is launched, go to the hamburger menu on the top left-hand corner and click the AI use cases link under AI Governance.

AI use cases
2. Check whether an inventory is already defined. If not, create a new inventory. Click the gear icon next to the AI use cases, click on Inventories in the Manage screen, then click New Inventory and fill in the inventory information.


Creating a model inventory

Creating a new inventory
3. Click the AI use cases link under AI Governance again in the hamburger menu and then create a new AI use case by clicking the New AI use case button. Then fill in the Name, Description, Risk level, and select the Inventory.


Creating a new AI use case

New AI use case information to be filled by the model owner or the model requestor
4. Once the use case is finalized, the Model Owner or the Model Requestor changes the status of the use case to Use case approved. Open the AI use case by navigating to AI Governance>> AI use cases from the hamburger menu on the top left-hand corner, click on the edit button next to Status on the side panel and change the Status to Use case approved.


Changing the status of an AI use case

Various statuses for an AI use case
Step 2: Build prompt templates based on a Generative AI Foundation Model

In this step, a Model Developer, a Prompt Engineer, or an AI Engineer builds and tests multiple prompt templates using more than one Foundation Model available on IBM watsonx.ai. One of these prompt templates ultimately becomes the champion model, and the rest will become challenger models.

Click on the hamburger menu in the top left-hand corner and click Project >> View all projects >> New project button. Click on Create an empty project tile and fill in the Name and Description of the project. Also, select a Cloud Object Storage service. If no Cloud Object Storage service is available, create one from the IBM Cloud Catalog. Also, the Model Developer changes the status of the use case to Development in progress.


New project
2. Open the newly created project by navigating from the hamburger menu. Click Project >> View all projects and then select the project name.

3. Once in the project, build a new prompt by clicking the New asset button, then click the Experiment with foundation models and build prompt tile.


Creating a new prompt template

Experimenting with Generative AI Foundation Models and building prompts
4. Once the Prompt Lab page is displayed, select the base Generative AI Foundation Model from the supported list of Foundation Models below (including prompt-tuned models), enter the instructions, change the input and output fields, if necessary, and add examples.


Generative AI Foundation Models available in watsonx.ai, including prompt tune models

Prompt Engineering using zero-shot, one-shot, or few-shot prompting
5. Try and test your prompts.


Testing the prompts
6. Define prompt variables. At least define one to capture the prompt inputs by clicking the (#) on the top right-hand menu.


Prompt variables

Adding prompt variables
7. Once the prompt variables are defined, add the prompt variables to prompt input in the Try section by clicking # in the prompt input field and selecting the prompt variables. The prompt variable gets added in the prompt input with curly brackets.


Viewing the list of the prompt variables before adding the prompt variables to the prompt input

Selecting the prompt variables that will be part of the prompt input

Prompt variables added to the input field under Try
8. Save the prompt engineering work as a prompt template. Click Save Work link >> Save As. Select Prompt Template, provide prompt template Name, select the Task as Classification, and click the Save button. The prompt template gets saved in the current project. Also, the Model Developer changes the status of the use case to Developed.


Saving prompt as prompt template

Saving the prompt template in a project
9. Navigate to project by click Go to the Project >> Assets, select the newly saved prompt template, click on three dots on the right, and click View AI factsheet.


Saved prompt template

View AI factsheet
10. Enable tracking of the life cycle of the prompt template adapted from a Generative AI Foundation Model. Also, note the metadata about the prompt template. Choose an existing AI use case or create/define a new one for tracking facts about the prompt template. Choose an existing approach or create/define a new one to capture the path for solving the use case’s goal and tracking facts about the prompt template adapted from a Generative AI Foundation Model. An approach might reflect the Generative AI Foundation Model and model architecture used. Each approach can include multiple versions. Click the Track asset button to enable tracking of the prompt template asset in a use case. Also, the Model Developer changes the status of the use case to Ready for AI asset validation.


Tracking the prompt template adapted from a Generative AI Foundation Model in an AI use case and viewing the prompt template metadata

Selecting an AI use case for tracking

Selecting an approach to capture the path for solving the use case

Assigning model versions
Step 3: Evaluate and approve the prompt template

A Model Validator or a Model Reviewer evaluates the prompt template leveraging the validation data set in this step. The Model Validator could be another AI Engineer, another Prompt Engineer, or a member of the Model Risk Management Office.

Create a deployment space for validation by clicking on the top right hamburger menu followed by clicking Deployments >> New deployment space, entering Name and Description, and selecting Deployment stage as Testing. Also, select the Cloud Object Storage service for deployment space to use.

Creating new deployment space for validation deployment

Creating validation deployment space after providing deployment space information
2. Find the prompt template in the project. Go to the hamburger menu on the top left-hand corner, click Project >> Assets, and select the saved prompt template. Click on the three dots on the right, click Promote to space, and select the target space as the validation deployment space. An asset gets created in the validation deployment space with the prompt template name.


Promoting the prompt template

Promoting the prompt template to the validation deployment space
3. Find the promoted prompt template in the validation deployment space. Go to the hamburger menu in the top left-hand corner, click the Deployments link, select the validation deployment space where the prompt template was promoted, go to the Assets tab, and find the new prompt template asset. Click on the three dots on the right and select Deploy. The deployed prompt template in the validation deployment space is now ready for evaluation.


Deploying the prompt template based on a Generative AI Foundation Model in the validation deployment space

Creating the validation deployment
4. Find the prompt template deployment in the validation deployment space. Go to the hamburger menu in the top left-hand corner, click the Deployments link, select the validation deployment space where the prompt template was promoted and deployed, go to the Deployments tab, and find the new prompt template deployment. Click on the prompt template deployment, the Evaluations tab, and Activate. Then, select evaluation dimensions. Upload the test data set file with input and reference output data, then map the prompt variables to test data fields/columns. Submit for evaluation by clicking the Evaluate button.


Activating monitoring for the validation deployment

Selecting evaluation dimension

Mapping prompt variables to test data fields

Submitting for evaluation
5. The Model Validator or the Model Reviewer reviews the quality metrics and model health and then approves the prompt template adapted from a Generative AI Foundation Model for production deployment. Also, the Model Validator changes the status of the use case to AI asset approved.


Quality metrics after the evaluation

Detailed quality metrics

Model health metrics
Step 4: Deploy the prompt template for production

A Model Ops Engineer deploys the prompt template in the production deployment space in this step.

Create a deployment space for production by clicking on the top right hamburger menu followed by clicking Deployments >> New deployment space, entering Name and Description, and selecting Deployment stage as Production. Also, select the Cloud Object Storage service for deployment space to use.

Creating new deployment space for production deployment

Creating production deployment space after providing deployment space information
2. Find the prompt template in the project. Go to the hamburger menu on the top left-hand corner, click Project >> Assets, and select the saved prompt template. Click on the three dots on the right, click Promote to space, and select the target space as the production deployment space. An asset gets created in the production deployment space with the prompt template name. Also, the Model Ops Engineer changes the status of the use case to Promoted to production space.


Promoting the prompt template to the production deployment space

Deploying the prompt template based on a Generative AI Foundation Model
3. Find the promoted prompt template in the production deployment space. Go to the hamburger menu in the top right-hand corner, click the Deployments link, select the production deployment space where the prompt template was promoted, go to the Assets tab, and find the new prompt template asset. Click on the three dots on the right and select Deploy. The deployed prompt template in the production deployment space is now ready for active monitoring. Also, the Model Ops Engineer changes the status of the use case to Deployed for operation.


Deploying the prompt template based on a Generative AI Foundation Model in the production deployment space

Creating the production deployment
Step 5: Monitor and manage the production deployment of the prompt template

The Model Ops Engineer activates the prompt template in the production deployment space for active monitoring in this step.

Find the prompt template deployment in the production deployment space. Go to the hamburger menu in the top left-hand corner, click the Deployments link, select the production deployment space where the prompt template was promoted and deployed, go to the Deployments tab, and find the new prompt template deployment. Click on the prompt template deployment, click the Evaluations tab, and click Activate. Then, select the evaluation dimensions. Review the payload and feedback data schema. Submit for active monitoring by clicking the Activate button. Also, the Model Ops Engineer changes the status of the use case to In operation.
Tips:

IBM watsonx.governance provides a multitude of generative AI quality metrics based on use cases such as text summarization, classification, content generation, entity extraction, and question answering. The following generative AI quality metrics are supported by watsonx.governance as of December 2023: ROGUE, SARI, METEOR, Text quality, BLEU, Sentence similarity (Jaccard similarity and Cosine similarity), PII, HAP, Readability, Exact match, Multi-label/class metrics (F1 score, precision, recall).


Activating monitoring of the production deployment

Selecting evaluation dimension

Review the payload and feedback schema and activate production monitoring of the prompt template deployment

Payload data schema

Feedback data schema
2. Test the prompt template deployment in the production deployment space. Go to the hamburger menu in the top right-hand corner, click the Deployments link, select the production deployment space where the prompt template was promoted and deployed, go to the Deployments tab, and find the new prompt template deployment. Click on the prompt template deployment and go to the Test tab. Enter a positive prompt input and then click the Generate button. Review the prompt results to ensure the right output is generated. Enter a negative prompt input and then click the Generate button again. Review the generated output again.


Testing the production deployment

Validating the prompt result
3. The Model Ops Engineer then actively monitors the alerts for metric breaches and takes corrective actions when the alerts are raised, collaborating with the Model Owner, the Model Developer, and the Model Reviewer. To view the alerts associated with an AI use case, go to the AI use case by navigating AI Governance >> AI use cases from the hamburger menu on the top left-hand corner, click three dots on the right next to the AI use case and select Preview alerts.


Monitoring dashboard for prompt template deployment

Quality F1 measure against time

Performance metrics

Drift against time

Model health metrics

Previewing alerts

Alerts raised
4. Additionally, the Model Risk Officer or a member of the Model Risk Management Office can export a report on the current state of an AI use case at any time. Go to the hamburger menu in the top left-hand corner, click the Deployments link, select the production deployment space where the prompt template was promoted and deployed, go to the Assets tab, find the prompt template asset, and click the prompt template asset. Then, click the AI Factsheet tab, click the Export report link, select the report format, select the report template, and click the Export button to save a report in the chosen report format in the local drive for further investigation or to provide evidence to related compliance inquiry. A sample report can be found at https://github.com/sghosh04/watsonx/blob/main/data/Sample%20AI%20Asset%20Report.pdf. The report contains information about the AI Asset in a format that is easy to share and print.


Exporting a report for an AI use case

Selecting the report format and report template to export the report

Sample report
Step 6: Infuse and operationalize business applications and workflows with AI inference using the deployed prompt template

Once the prompt template is deployed and activated for continuous monitoring, the Application Developers could infuse applications and workflows with AI inference using the deployed prompt template adapted from a Generative AI Foundation Model. See the attached notebook on automating and invoking the deployed prompt template. The notebook provides three approaches to making inference calls on the deployed prompt template. The first two use Python SDK, and the third uses REST API.

The notebook first determines the deployment space ID, deployment ID, inference URL, and prompt variables for the prompt template.

2. The notebook then prepares the payload for inference calls.


3. The notebook then showcases three approaches to make inference calls on the deployed prompt template based on a Generative AI Foundation Model.

4. In the first approach, the Application Developer calls the inference endpoint using the Watson Machine Learning API client and the prompt template deployment using the Python SDK.


Approach 1 using Watson Machine Learning API client
5. In the second approach, the Application Developer calls the inference endpoint using Model Inference, pointing to the prompt template deployment using the Python SDK.


Approach 2 using Model Inference object leveraging Python SDK
6. In the third approach, the Application Developer calls the inference endpoint using the REST API.


Approach 3 using REST API
One can find the code snippet shown above in a Jupyter notebook at the following GitHub location: https://github.com/sghosh04/watsonx/blob/main/sample_notebooks/infer_with_gen_ai_model_on_watson_x.ipynb

Summary — Can one trust Generative AI Foundation Models?

While Generative AI, powered by Large Language Models (LLM) or Foundation Models, offers many use cases and applications for businesses, it also introduces new questions, risks, and complexities. Where did the training data for a Generative AI Foundation Model come from, what is the lineage of the training data, and can the training data be trusted? Did the training data contain hate, abuse, or profanity (HAP)? If so, the generated output at the inference point will also have HAP content. Are the models leaking personally identifiable information (PII) or the business’s confidential data in the generated output? Can the generated output be explained, and can the generated output provide source attribution? Hence, continuous monitoring of the Generative AI Foundation Models and their adaptation for business use cases is critical. Monitoring helps identify HAP, PII, and confidential data in the generated output, requiring appropriate filtering. IBM watsonx.governance provides organizations with tools and automation to help answer these questions, manage risk, embrace transparency, anticipate compliance and scrutiny with future AI-focused regulation, and unleash their AI workforce to focus on innovation and growth. This article demonstrates how organizations could leverage IBM watsonx.governance to address their challenges with the adoption of Generative AI.
