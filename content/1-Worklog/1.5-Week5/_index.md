---
title: "Week 5 Worklog"
date: 2026-05-18
weight: 5
chapter: false
pre: " <b> 1.5. </b> "
---

### Objectives for Week 5:

* Identify the technologies to be used for developing the AI Recipe Finder project.
* Select appropriate AWS services for each system component.
* Finalize the overall deployment architecture of the project.
* Finalize the workflow between the frontend, backend, database, authentication, and AI components.
* Search for datasets suitable for recipe recommendation and nutritional analysis.
* Analyze the structure, quality, and applicability of each dataset.
* Select the official datasets in preparation for the data-processing phase.

### Tasks Completed This Week:

| Day | Tasks | Start Date | Completion Date | References |
| --- | --- | --- | --- | --- |
| 2 | - Summarized the functional and non-functional requirements of the AI Recipe Finder project.<br>- Identified the main system components, including the frontend, backend, database, user authentication, and AI.<br>- Evaluated technologies based on the team’s capabilities, implementation timeline, and AWS budget.<br>- Selected React and Tailwind CSS for frontend development.<br>- Selected FastAPI and Python for backend API development.<br>- Selected MySQL as the database management system. | 18/05/2026 | 18/05/2026 |  |
| 3 | - Identified the official AWS services to be used in the project.<br>- Selected AWS Amplify for frontend deployment.<br>- Selected Amazon EC2 for deploying the FastAPI backend.<br>- Selected Amazon RDS for MySQL to store system data.<br>- Selected Amazon Cognito to manage user registration, sign-in, and authentication.<br>- Selected Amazon Bedrock to support the chatbot and AI-powered features.<br>- Considered AWS IAM and Amazon CloudWatch for access control, logging, and system monitoring. | 19/05/2026 | 19/05/2026 | <https://docs.aws.amazon.com/amplify/><br><https://docs.aws.amazon.com/ec2/><br><https://docs.aws.amazon.com/rds/><br><https://docs.aws.amazon.com/cognito/><br><https://docs.aws.amazon.com/bedrock/> |
| 4 | - Finalized the overall system architecture.<br>- Determined that the React frontend would be deployed on AWS Amplify.<br>- Determined that the FastAPI backend would be deployed on Amazon EC2 and provide REST APIs to the frontend.<br>- Determined that Amazon RDS for MySQL would store recipe, nutrition, user, and activity history data.<br>- Determined that Amazon Cognito would handle user authentication and provide authentication tokens.<br>- Determined that Amazon Bedrock would support the chatbot and process AI-related requests.<br>- Considered the connection methods, permissions, and data protection requirements between the system components. | 20/05/2026 | 20/05/2026 | <https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html><br><https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html><br><https://youtu.be/l8isyDe-GwY?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i><br><https://skillbuilder.aws/learn/U89MJTNSM8/aws-wellarchitected-foundations/RCY5NFM8R9> |
| 5 | - Finalized the overall workflow of the AI Recipe Finder project.<br>- Defined the registration and sign-in flow between the frontend, Amazon Cognito, and backend.<br>- Defined the recipe search and ingredient-based recommendation flow.<br>- Defined the data query flow between the backend and Amazon RDS.<br>- Defined the chatbot and intelligent search processing flow between the backend and AI services.<br>- Determined how to store user information, favorite recipes, search history, and chat history.<br>- Agreed on the responsibilities of each system component and the implementation direction for the following weeks. | 21/05/2026 | 21/05/2026 | <https://youtu.be/l8isyDe-GwY?list=PLahN4TLWtox2a3vElknwzU_urND8hLn1i><br><https://skillbuilder.aws/learn/U89MJTNSM8/aws-wellarchitected-foundations/RCY5NFM8R9><br><https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |
| 6 | - Searched for datasets related to recipes, ingredients, and nutritional information.<br>- Examined the Food.com Recipes and Interactions dataset on Kaggle.<br>- Examined nutritional data from USDA FoodData Central.<br>- Analyzed the data fields, number of records, formats, and usability of each dataset.<br>- Evaluated the suitability of the datasets for recipe recommendation and calorie analysis.<br>- Selected the Food.com recipe dataset and USDA FoodData Central nutritional dataset as the project’s primary data sources.<br>- Determined that the datasets would be downloaded and processed locally before the cleaned data was imported into Amazon RDS.<br>- Identified requirements for data cleaning, duplicate detection, and data normalization. | 22/05/2026 | 22/05/2026 | <https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags/data><br><https://fdc.nal.usda.gov/download-datasets><br><https://fdc.nal.usda.gov/data-documentation.html> |

### Results Achieved in Week 5:

* Identified the main technologies to be used in the project:

  * **Frontend:** React and Tailwind CSS.
  * **Backend:** FastAPI and Python.
  * **Database:** MySQL.
  * **System communication:** REST API.
  * **Authentication:** Tokens provided by Amazon Cognito.
  * **Source code management:** Git and GitHub.

* Finalized the AWS services to be used in the architecture:

  * **AWS Amplify:** Deploys and hosts the frontend application.
  * **Amazon EC2:** Hosts the FastAPI backend.
  * **Amazon RDS for MySQL:** Stores the system’s relational data.
  * **Amazon Cognito:** Manages user accounts and authentication.
  * **Amazon Bedrock:** Supports the chatbot and AI-powered features.
  * **AWS IAM:** Manages roles and access permissions.
  * **Amazon CloudWatch:** Monitors logs and system status.

* Finalized the overall project architecture:

  1. Users access the React frontend deployed on AWS Amplify.
  2. Amazon Cognito handles user registration and sign-in and provides authentication tokens.
  3. The frontend sends requests to the FastAPI backend running on Amazon EC2.
  4. The backend validates tokens for APIs that require authentication.
  5. The backend queries data stored in Amazon RDS for MySQL.
  6. Chatbot and intelligent search requests are processed with support from Amazon Bedrock.
  7. The backend aggregates the results and returns responses to the frontend.

* Finalized the main system workflows:

  * User registration, sign-in, and authentication.
  * Recipe search and recipe detail viewing.
  * Ingredient-based recipe recommendations.
  * AI-powered semantic search.
  * A chatbot that provides cooking assistance and nutritional advice.
  * Recipe calorie analysis.
  * Favorite recipe management.
  * Search history and chat history storage.

* Determined that users must be authenticated before accessing the AI chatbot and features involving personal data.

* Examined and selected two primary data sources:

  * **Food.com Recipes and Interactions:** Provides recipe, ingredient, preparation step, and category tag data.
  * **USDA FoodData Central:** Provides food and nutritional data to support calorie analysis.

* Defined the role of each dataset:

  * The Food.com dataset is used for recipe search and recommendation features.
  * The USDA FoodData Central dataset is used to look up and calculate nutritional information.

* Defined the data preparation process:

  1. Download the datasets from their official sources to the local environment.
  2. Inspect the data structure and data types.
  3. Analyze missing and invalid data.
  4. Identify and process duplicate records.
  5. Normalize recipe and ingredient names.
  6. Convert fields containing complex data structures.
  7. Verify data quality after cleaning.
  8. Import the finalized data into Amazon RDS for MySQL.

* Completed the objectives of selecting technologies, finalizing the architecture and workflows, and choosing the datasets, establishing a foundation for beginning project implementation in Week 6.