---
title: Basic Governance Workflows
nav_order: 5
---
# Basic Governance Workflows

## Overall Objectives

- View AI Use Case
- Introduction to a workflow
- Create AI Case
- Progress use case through Use Case Request workflow
- Complete Applicability Assessment
- View Risk Identification questionnaire
- Complete Use Case Review

## Viewing Use Case and Model

1. Everyone log in to Governance Console
2. Click to Inventory → Use Cases
3. Click into '1.1 HR Recruitment'
4. View Use Case
5. View associated fields + guidance text on right side
6. Click into 'Risk Identification' assessment. Look through a few questions
7. View associated mandates
8. View performance monitoring
9. Click into 'Use Case Approval'
10. View associated Models
11. View the model
12. Move through the model info. View the parent use case
13. View Change Request
14. View Model Tree
15. See creation of a Model Issue

## Viewing Use Case Request Workflow

1. Go to workflows from the gear icon → Solution Configuration → Workflow
2. Search 'Use Case Request'; click into workflow
3. Start with workflow properties:
   - Type; auto vs manual start
   - Scheduled start
   - Oversight
   - Applicability
4. Click action from Start to Use Case Data Gathering
5. Click into the operation:
   - View the operation
   - Setting field of the current object
6. Click Use Case Data Gathering:
   - View type
   - Assignee and subscribers
   - Task view overrides
7. Click action pointing into Initial Approval
8. Scroll to operation for creating applicability assessment. Click into it:
   - View the operation of creating an object and object is a questionnaire assessment
   - Also view how we are assigning the type of assessment

## Hands on Creation

1. Click into the Hamburger Menu in the top left corner in the Governance Console
2. Under Inventory, click Use Cases
3. Click New to create a new AI Use Case. The Use Case represents the business need for using AI models. For example your Use Case could be detecting fraudulent claims or reducing the manual effort in the candidate selection process.
4. Enter in a name followed by your initials (i.e. 'Fraud Detection – EG')
5. Assign yourself in the Owner field
6. Enter in a description for your Use Case
7. Click Add under Primary Business Entity. Then search for 'State Farm' business entity. Select is and add.
8. Save Use Case
9. You should now be looking at the Use Case. Notice how the status is equal to 'Proposed'
10. On the right side of the screen, you can read the general information on the object you are looking at or instructions of what to complete during a workflow stage. Here the Use Case is in the stage 'Use Case Data Gathering' so it is giving information of what to review.
11. In the General section, assign one or multiple Stakeholder Departments. This field will be used when Use Case Reviews are created. Each stakeholder department will be assigned a review.
12. In the Use Case Details section, change the field Uses Foundation Models to Yes. Save the changes using the save button in top right corner.
13. Under the blue action button in the top right, click Submit for Initial Approval
14. Click home icon on top left corner.
15. Click my tasks. These are the tasks assigned to you. You should see three tasks:
    - One for your Use Case
    - One for a Risk Identification questionnaire
    - One for a Applicability Assessment questionnaire
    - Here you can see the name of the object, object type, workflow name, and workflow stage.
16. Click into the Applicability Assessment
17. Complete questionnaire by answering questions. Feel free to experiment with different answers to see how the questionnaire changes based on responses.
18. Once completed, click Applicability Assessment Complete under blue action button
19. Click back to My Tasks from the home screen and click into your use case
20. Scroll to the Regulatory Information section and notice the applicability assessment completion and the EU AI Risk Category. More likely than not, your answers in the assessment has given an Out of Scope value for the Risk Category. This is a simple example and can be customized for other regulations or mandates.
21. On the right side screen under All Key Items, click the Risk Level. Assign a risk level to your use case. Save your changes.
22. Click Submit for Stakeholder Review under blue action button. Within the Use Case Request workflow, this action will automatically create a Use Case review for each stakeholder department you selected earlier.
23. Scroll to Use Case Approvals section, this is where you can see the created reviews.
24. Click into a Review and view associated objects. Here you can see the parent use case being reviewed, and the completed assessments. You have only completed the Risk Identification assessment.
25. Assign yourself as the Reviewer, then leave a Review Comment. Finally, assign a risk rating. This can be different to the risk rating you assigned on the use case itself. This can help differentiate the risk rating across different departments.
26. Save your changes and then click Approve Use Case under the blue action button.
27. Click back to your Use Case
28. Click action to Approve for Development. You have completed the Use Case Request workflow!

## Completion Summary

You have successfully created an AI Use Case, representing a business problem that requires the use of AI models. You governed the Use Case by progressing it through an initial Use Case Request workflow, approving it at various stages. You also got an introduction into how that workflow is created and how it can be customized. Also, you completed an Applicability Assessment, similar to how other questionnaire assessments would be completed. The final step you did was completing the Use Case Review and then progressing the Use Case to Approved for Development. Great job! The next steps would be to create your models, evaluate them through the Monitoring Console, and then govern them via the Governance Console.