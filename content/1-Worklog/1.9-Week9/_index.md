---
title: "Week 9 Worklog"
date: 2026-06-13
weight: 9
chapter: false
pre: " <b> 1.9. </b> "
---

### Week 9 Objectives

* Add the required APIs to the AI Recipe Finder backend.
* Develop features related to data and user accounts.
* Complete the ORM Models, Pydantic Schemas, CRUD, Service Layer, and API Routers for each feature.
* Add or modify the database structure when necessary.
* Apply Amazon Cognito authentication to personalized APIs.
* Validate input data, access permissions, and API error responses.
* Deploy the new backend version to Amazon EC2.
* Support the frontend and AI components in connecting to the backend.
* Identify and resolve issues that arise during integration.

### Tasks carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Gather API requirements from the frontend and AI components.<br>- Review the backend structure and completed APIs.<br>- Identify additional backend features required for authenticated users.<br>- Review the structure of the `users`, `favorites`, `search_history`, and `chat_history` tables in Amazon RDS.<br>- Review primary keys, foreign keys, unique constraints, and related indexes.<br>- Define the request, response, HTTP status codes, and authentication requirements for each API.<br>- Plan the implementation based on the Router, Schema, CRUD, and Service architecture. | 15/06/2026 | 15/06/2026 |  |
| 3 | - Add APIs for user account management.<br>- Build request schemas for input validation.<br>- Add functionality to update the current user's username.<br>- Develop the `PATCH /auth/me/username` API.<br>- Use the authenticated user obtained from the authentication dependency instead of receiving `user_id` directly from the client.<br>- Validate empty usernames, invalid formats, or usernames exceeding the allowed length.<br>- Check whether the username is already in use if the system enforces a unique constraint.<br>- Standardize responses according to the user information schema.<br>- Test the API with missing tokens, invalid tokens, and valid tokens. | 16/06/2026 | 16/06/2026 |  |
| 4 | - Continue adding personalized APIs for user accounts.<br>- Complete the required ORM Models, Pydantic Schemas, CRUD, Service Layer, and Routers.<br>- Apply the Amazon Cognito authentication dependency to APIs that require authentication.<br>- Associate data with users through the `user_id` determined from `cognito_sub`.<br>- Verify access permissions to ensure users can only access data belonging to their own accounts.<br>- Handle cases where resources do not exist or duplicate data is detected.<br>- Use transactions, commits, and rollbacks appropriately when modifying data.<br>- Verify that data is correctly stored in Amazon RDS. | 17/06/2026 | 17/06/2026 |  |
| 5 | - Complete and test the APIs added during the week.<br>- Test valid and invalid requests using Swagger UI.<br>- Verify the `401 Unauthorized`, `404 Not Found`, `409 Conflict`, and `422 Unprocessable Entity` scenarios.<br>- Review the response schemas and error response contents.<br>- Verify that the APIs do not expose tokens, stack traces, or database information.<br>- Recheck input validation and pagination where applicable.<br>- Update the source code on GitHub.<br>- Pull the latest version on Amazon EC2.<br>- Restart the `systemd service` and verify the runtime logs.<br>- Test the APIs after deployment. | 18/06/2026 | 18/06/2026 |  |
| 6 | - Provide endpoint information, HTTP methods, request formats, and response formats to the frontend and AI team members.<br>- Support the frontend in sending the Access Token to the backend through the Authorization Header.<br>- Support the frontend in connecting to the APIs deployed on Amazon EC2.<br>- Support the AI component in retrieving and submitting data through the backend.<br>- Verify URL configuration, CORS, tokens, and request data during integration.<br>- Monitor backend logs to identify the causes of issues.<br>- Resolve issues related to authentication, input validation, database connectivity, and response structure.<br>- Re-test the complete workflow after resolving issues.<br>- Record unfinished tasks for continued implementation in the following week. | 19/06/2026 | 19/06/2026 |  |

### Week 9 Expected Outcomes

* Identify the list of APIs that need to be added based on the requirements of the frontend and AI components.

* Complete the user account management APIs:

  * `GET /auth/me`: Retrieve the current user's information.
  * `PATCH /auth/me/username`: Update the current user's username.

* Personalized APIs use the Amazon Cognito authentication dependency to identify the authenticated user.

* Users do not need and are not allowed to provide `user_id` directly to access their personal data.

* Complete the required backend components for the implemented features:

  * ORM Models.
  * Pydantic Schemas.
  * CRUD.
  * Service Layer.
  * API Router.
  * Authentication Dependency.

* Add input validation:

  * Validate data types.
  * Validate length and format.
  * Remove unnecessary whitespace.
  * Reject empty or invalid values.
  * Prevent requests that generate excessively large database queries.

* Standardize HTTP status codes:

  * `200 OK` for successful retrieval or updates.
  * `401 Unauthorized` when the token is missing or invalid.
  * `404 Not Found` when the resource does not exist.
  * `409 Conflict` when data violates a unique constraint.
  * `422 Unprocessable Entity` when the input data is invalid.

* Verify access permissions and ensure that users can only access data belonging to their own accounts.

* Verify that data is correctly stored in and retrieved from Amazon RDS.

* Deploy the new backend version to GitHub and Amazon EC2.

* Restart the backend service and confirm that the APIs continue to operate correctly after deployment.

* Support the frontend and AI components in connecting to the backend.

* Identify and resolve integration issues, including:

  * Incorrect API endpoints.
  * CORS issues.
  * Missing or invalid Authorization Headers.
  * Invalid Access Tokens.
  * Request data that does not match the required schema.
  * Response structures that do not meet the requirements of integrated components.
  * Amazon RDS connection issues.
  * Environment configuration issues on Amazon EC2.

* Complete the backend foundation for continuing the development of Favorite Recipes, Search History, and Chat History APIs.