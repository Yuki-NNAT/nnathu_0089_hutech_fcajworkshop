---
title: "Week 8 Worklog"
date: 2026-06-06
weight: 8
chapter: false
pre: " <b> 1.8. </b> "
---

### Week 8 Objectives

* Create and configure Amazon Cognito for the AI Recipe Finder project.
* Set up a User Pool and App Client for user authentication.
* Integrate Amazon Cognito authentication into the FastAPI backend.
* Build functionality to verify Access Tokens issued by Amazon Cognito.
* Build a mechanism to retrieve authenticated user information.
* Synchronize users from Amazon Cognito to the `users` table in Amazon RDS.
* Configure the connection between Amazon Cognito, the FastAPI backend, and the database.
* Test API requests without an Access Token.
* Test authentication and user synchronization using a valid Access Token.
* Review token handling and user information processing to reduce security risks.

### Tasks carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Create an Amazon Cognito User Pool for the AI Recipe Finder project.<br>- Configure email as the sign-in method.<br>- Set up the required user account attributes.<br>- Configure the password policy and account verification mechanism.<br>- Create an App Client for authentication.<br>- Verify the supported sign-up, account confirmation, and sign-in flows.<br>- Record the required information, including the AWS Region, User Pool ID, and App Client ID. | 08/06/2026 | 08/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/cognito-user-pools.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-client-apps.html> |
| 3 | - Study the structure of JSON Web Tokens issued by Amazon Cognito.<br>- Differentiate ID Tokens, Access Tokens, and Refresh Tokens.<br>- Build a shared authentication dependency for the FastAPI backend.<br>- Retrieve the Access Token from the HTTP Authorization Header using the Bearer Token format.<br>- Retrieve the public key from the Cognito User Pool JSON Web Key Set (JWKS).<br>- Verify the JWT signature, algorithm, expiration time, and important claims.<br>- Verify that the token belongs to the configured User Pool and App Client.<br>- Standardize `401 Unauthorized` responses for missing, expired, or invalid tokens. | 09/06/2026 | 09/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-the-access-token.html><br><https://docs.aws.amazon.com/cognito/latest/developerguide/amazon-cognito-user-pools-using-tokens-verifying-a-jwt.html> |
| 4 | - Build functionality to synchronize authenticated users with Amazon RDS.<br>- Use the Cognito `sub` claim as the unique user identifier.<br>- Extract the user's email and username from the authentication information.<br>- Complete the ORM Model, Pydantic Schema, CRUD, and Auth Service for users.<br>- Search for users in the `users` table using the `cognito_sub` field.<br>- Build a mechanism to automatically create a user record on the first login.<br>- Reuse the existing record on subsequent logins to prevent duplication.<br>- Handle cases where the email already exists or user information is invalid. | 10/06/2026 | 10/06/2026 | <https://docs.aws.amazon.com/cognito/latest/developerguide/user-pool-settings-attributes.html> |
| 5 | - Configure Amazon Cognito environment variables on both the local backend and Amazon EC2.<br>- Do not hardcode the User Pool ID, App Client ID, or configuration values in the source code.<br>- Integrate the authentication dependency into the Auth API Router.<br>- Build the `GET /auth/me` API to return the current user's information.<br>- Deploy the updated backend with authentication functionality to Amazon EC2.<br>- Restart the `systemd service` and verify the runtime logs.<br>- Send a request to `GET /auth/me` without an Access Token.<br>- Verify that the API correctly returns `401 Unauthorized`.<br>- Confirm that error responses do not expose configuration details or internal processing information. | 11/06/2026 | 11/06/2026 |  |
| 6 | - Prepare a user account in Amazon Cognito and obtain a valid Access Token.<br>- Send the Access Token to the `GET /auth/me` API using the Bearer Token format.<br>- Verify that the backend successfully validates the JWT signature and claims.<br>- Verify that the backend retrieves the authenticated user's identity from the token.<br>- Verify that a first-time user is added to the `users` table in Amazon RDS.<br>- Verify that the API returns the correct information for the authenticated user.<br>- Send another request using the same account and confirm that no duplicate user record is created.<br>- Compare the `cognito_sub` and email values between Amazon Cognito and the `users` table.<br>- Test malformed tokens, invalid tokens, and expired tokens.<br>- Summarize the results and confirm that the authentication and user synchronization flow works correctly on the backend. | 12/06/2026 | 12/06/2026 |  |

### Week 8 Achievements

* Successfully created and configured an Amazon Cognito User Pool for the AI Recipe Finder project.

* Completed the basic authentication configuration:

  * Email sign-in method.
  * User account attributes.
  * Password policy.
  * Account verification mechanism.
  * App Client for authentication.
  * AWS Region, User Pool ID, and App Client ID for backend configuration.

* Successfully integrated Amazon Cognito authentication into the FastAPI backend.

* Built functionality to receive the Access Token from the HTTP Authorization Header using the following format:

  ```text
  Authorization: Bearer <access_token>