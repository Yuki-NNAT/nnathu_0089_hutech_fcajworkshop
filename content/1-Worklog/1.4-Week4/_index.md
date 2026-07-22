---
title: "Week 4 Worklog"
date: 2026-05-11
weight: 4
chapter: false
pre: " <b> 1.4. </b> "
---

### Objectives for Week 4:

* Research Amazon RDS, Amazon EC2, and Amazon Cognito.
* Understand the functions, components, and operating mechanisms of each service.
* Evaluate the role of each service in the AI Recipe Finder project.
* Learn how the backend connects to and queries data from Amazon RDS.
* Learn how Amazon Cognito authenticates users for the frontend and backend.
* Explore how Amazon EC2, Amazon RDS, and Amazon Cognito are connected.
* Identify fundamental networking, authorization, and security requirements when connecting AWS services.

### Tasks Completed This Week:

| Day | Tasks | Start Date | Completion Date | References |
| --- | --- | --- | --- | --- |
| 2 | - Researched an overview of Amazon RDS.<br>- Learned about the role of Amazon RDS in deploying and managing relational databases on AWS.<br>- Studied fundamental components such as DB instances, database engines, storage, endpoints, ports, and backups.<br>- Reviewed the database management systems supported by Amazon RDS.<br>- Evaluated the feasibility of using Amazon RDS for MySQL to store recipe, nutrition, user, and activity history data for the project. | 11/05/2026 | 11/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Welcome.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.html> |
| 3 | - Researched an overview of Amazon EC2.<br>- Learned about the role of EC2 in providing virtual servers on AWS.<br>- Studied components such as EC2 instances, Amazon Machine Images, instance types, key pairs, storage, and Elastic IP addresses.<br>- Learned about Security Groups and inbound and outbound rules.<br>- Evaluated the feasibility of using EC2 to deploy and operate the project's FastAPI backend. | 12/05/2026 | 12/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/concepts.html><br><https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-security-groups.html> |
| 4 | - Researched an overview of Amazon Cognito.<br>- Learned about the role of Cognito in managing user registration, sign-in, and authentication.<br>- Studied User Pools, App Clients, Hosted UI, and authentication tokens.<br>- Learned about the registration, account confirmation, sign-in, and sign-out processes.<br>- Examined how Cognito could protect features that require authentication, particularly the AI chatbot and users’ personal data. | 13/05/2026 | 13/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/cognito/latest/developerguide/what-is-amazon-cognito.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html> |
| 5 | - Studied the connection method between Amazon EC2 and Amazon RDS.<br>- Researched the roles of VPCs, subnets, endpoints, ports, and Security Groups in the connection process.<br>- Learned how the backend running on EC2 uses connection information to access the RDS database.<br>- Learned how to restrict database access using Security Groups instead of allowing connections from all IP addresses.<br>- Reviewed methods for protecting database credentials and using encrypted connections. | 14/05/2026 | 14/05/2026 | <https://www.youtube.com/@AWSStudyGroup><br><https://cloudjourney.awsstudygroup.com/><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ConnectToInstance.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/Overview.RDSSecurityGroups.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/database-authentication.html> |
| 6 | - Studied the connection flow between the frontend, Amazon Cognito, the backend running on EC2, and Amazon RDS.<br>- Researched how the frontend redirects users to Cognito for authentication and receives authentication tokens.<br>- Learned how the frontend includes tokens in requests sent to the backend API.<br>- Learned how the backend validates tokens before processing protected API requests.<br>- Determined how the backend uses authenticated user information to query or update the corresponding data in Amazon RDS.<br>- Summarized the roles of and connection methods between the researched services. | 15/05/2026 | 15/05/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-with-identity-providers.html><br><https://docs.aws.amazon.com/wellarchitected/latest/security-pillar/welcome.html> |

### Results Achieved in Week 4:

* Understood that Amazon RDS is a managed relational database service on AWS.

* Determined that Amazon RDS for MySQL could be used to store:

  * Recipe and food information.
  * Nutritional data.
  * User information.
  * Favorite recipes.
  * Search and chat histories.

* Understood the fundamental components of Amazon RDS:

  * DB instance.
  * Database engine.
  * Endpoint and port.
  * Storage.
  * Backup.
  * Security Group.

* Understood that Amazon EC2 provides virtual servers for deploying and operating applications on AWS.

* Determined that Amazon EC2 could be used to deploy the FastAPI backend of the AI Recipe Finder project.

* Understood the fundamental EC2 components, including:

  * Amazon Machine Image.
  * Instance type.
  * Key pair.
  * Security Group.
  * Storage.
  * Public IP address and Elastic IP address.

* Understood that a Security Group acts as a virtual firewall that controls inbound and outbound traffic for AWS resources.

* Understood that Amazon Cognito supports user registration, sign-in, sign-out, and authentication management.

* Studied the main components of Amazon Cognito:

  * **User Pool:** Manages user accounts and user information.
  * **App Client:** Represents an application that uses Cognito for authentication.
  * **Hosted UI:** Provides a Cognito-managed interface for registration and sign-in.
  * **Token:** Contains user information and authentication status.

* Determined that Cognito would be used to protect the AI chatbot and APIs related to users’ personal data.

* Understood the fundamental connection method between EC2 and RDS:

  1. The FastAPI backend is deployed on EC2.
  2. The backend uses the endpoint, port, and credentials to connect to RDS.
  3. The RDS Security Group only permits connections from EC2 through the required database port.
  4. The backend processes queries and returns the results to the frontend through APIs.

* Defined the planned authentication flow:

  1. The user accesses the frontend.
  2. The frontend redirects the user to Amazon Cognito for registration or sign-in.
  3. Cognito authenticates the user and returns tokens to the frontend.
  4. The frontend includes the token in requests sent to protected APIs.
  5. The backend validates the token.
  6. The backend processes the request and accesses the corresponding data in Amazon RDS.
  7. The result is returned to the frontend for display.

* Understood the roles of VPCs, subnets, Security Groups, endpoints, and ports in connecting AWS services.

* Identified several fundamental security requirements:

  * Do not expose database credentials.
  * Do not make the RDS port publicly accessible to the entire Internet unless necessary.
  * Only allow appropriate sources to connect to EC2 and RDS.
  * Validate tokens before granting access to protected APIs.
  * Apply the principle of least privilege when assigning permissions.
  * Prioritize encrypted connections when transmitting data.

* Completed the objectives of researching Amazon RDS, Amazon EC2, and Amazon Cognito, establishing a foundation for refining the project architecture and workflow in the following week.