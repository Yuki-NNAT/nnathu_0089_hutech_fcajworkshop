---
title: "Week 3 Worklog"
date: 2026-05-04
weight: 3
chapter: false
pre: " <b> 1.3. </b> "
---

### Week 3 Objectives:

* Discuss potential project ideas with the team and select a suitable topic.
* Define the project idea, objectives, and scope.
* Analyze the main features of the AI Recipe Finder system.
* Research the AWS services that could be used to implement the project.
* Develop a preliminary workflow showing how the system components interact.
* Establish an initial task direction for the team members.

### Tasks carried out this week:

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| Monday | - Meet with the team to propose potential project ideas.<br>- Discuss the feasibility, scope, and AWS applicability of each idea.<br>- Compare the proposed topics based on development time, data availability, required technologies, and team capabilities.<br>- Agree on a suitable topic for further research. | 05/04/2026 | 05/04/2026 |  |
| Tuesday | - Finalize the AI Recipe Finder project idea.<br>- Define the problem that the project aims to solve.<br>- Identify the target users and their main needs.<br>- Analyze the project objectives, scope, and expected outcomes. | 05/05/2026 | 05/05/2026 |  |
| Wednesday | - Analyze the main features of the system.<br>- Define the recipe recommendation feature based on user-provided ingredients.<br>- Propose an AI-powered semantic search feature.<br>- Define a chatbot feature for cooking assistance and nutrition advice.<br>- Propose calorie analysis and user information management features.<br>- Establish the requirement that users must sign in before accessing the AI chatbot. | 05/06/2026 | 05/06/2026 |  |
| Thursday | - Research and propose AWS services for the project.<br>- Propose Amazon RDS for storing recipe, nutrition, and user data.<br>- Propose Amazon EC2 or AWS App Runner for backend deployment.<br>- Propose AWS Amplify for frontend deployment.<br>- Propose Amazon Cognito for user registration, sign-in, and authentication.<br>- Propose Amazon Bedrock for AI-related features.<br>- Propose Amazon S3 for storing datasets and project files.<br>- Consider AWS IAM and Amazon CloudWatch for permissions, monitoring, and system management. | 05/07/2026 | 05/07/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/> |
| Friday | - Study how the frontend, backend, database, and AI components should be organized.<br>- Develop a preliminary workflow for the AI Recipe Finder system.<br>- Define the user flow from authentication and ingredient input to recipe recommendations.<br>- Define the data flow between the frontend, backend, Amazon RDS, and AI services.<br>- Agree on the implementation direction for the following weeks.<br>- Assign preliminary responsibilities to the team members. | 05/08/2026 | 05/08/2026 | https://www.youtube.com/@AWSStudyGroup<br><https://docs.aws.amazon.com/wellarchitected/latest/framework/welcome.html> |

### Week 3 Achievements:

* Completed the process of discussing, evaluating, and selecting a project idea with the team.

* Selected **AI Recipe Finder** as the project topic for further analysis and implementation.

* Defined the main project objectives:

  * Recommend recipes based on ingredients provided by users.
  * Support intelligent recipe discovery using AI Semantic Search.
  * Provide a chatbot for cooking assistance and nutrition advice.
  * Analyze calories and selected nutritional information.
  * Deploy the system using AWS cloud services.

* Identified the planned system features:

  * User registration, sign-in, and profile management.
  * Recipe search and detailed recipe information.
  * Recipe recommendations based on available ingredients.
  * AI-powered semantic recipe search.
  * A chatbot for cooking and nutrition assistance.
  * Recipe calorie analysis.
  * Favorite recipes and search history management.
  * Authentication requirements for accessing the AI chatbot.

* Proposed the following AWS services:

  * **Amazon RDS:** Store recipe, nutrition, user, and activity history data.
  * **Amazon EC2 or AWS App Runner:** Deploy the FastAPI backend.
  * **AWS Amplify:** Build and deploy the frontend.
  * **Amazon Cognito:** Manage user registration, sign-in, and authentication.
  * **Amazon Bedrock:** Support chatbot and AI features.
  * **Amazon S3:** Store datasets and required project files.
  * **AWS IAM:** Manage roles and permissions between AWS services.
  * **Amazon CloudWatch:** Monitor system activity, logs, and resource status.

* Developed a preliminary system workflow:

  1. The user accesses the web application.
  2. The user registers or signs in through Amazon Cognito.
  3. The user enters ingredients or a recipe-related search query.
  4. The frontend sends the request to the backend through an API.
  5. The backend processes the request and queries Amazon RDS.
  6. Semantic search and chatbot requests are sent to the AI service.
  7. The backend combines the required data and returns the result to the frontend.
  8. The frontend displays recipe recommendations, recipe details, or chatbot responses.

* Identified the main system components: frontend, backend, database, user authentication, and AI services.

* Established an initial direction for assigning team responsibilities and continuing with architecture design and data preparation in the following week.