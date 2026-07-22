---
title: "Week 7 Worklog"
date: 2026-05-30
weight: 7
chapter: false
pre: " <b> 1.7. </b> "
---

### Week 7 Objectives

* Build the backend architecture for the project using FastAPI.
* Connect the backend to Amazon RDS for MySQL.
* Develop ORM Models, Pydantic Schemas, CRUD, Service Layer, and API Routers.
* Develop APIs for retrieving recipe and nutrition data.
* Test API functionality in the local environment.
* Create and configure an Amazon EC2 server.
* Deploy the FastAPI backend to Amazon EC2.
* Connect the backend running on EC2 to the Amazon RDS database.
* Review the source code against risks related to the OWASP Top 10.
* Add input validation and API error handling.
* Verify the backend after deployment.

### Tasks carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Initialize the FastAPI backend structure for the AI Recipe Finder project.<br>- Organize the source code into configuration, database connection, models, schemas, CRUD, services, and API routers.<br>- Install the required libraries, including FastAPI, Uvicorn, SQLAlchemy, PyMySQL, and Pydantic.<br>- Create environment configuration files to store database connection information.<br>- Build the SQLAlchemy Engine and database session management mechanism.<br>- Configure the connection pool, verify database connectivity, and close sessions after each request.<br>- Test the connection between the local backend and the `food_ai_db` database on Amazon RDS. | 01/06/2026 | 01/06/2026 |  |
| 3 | - Build ORM Models corresponding to the database tables designed in Amazon RDS.<br>- Develop models for users, recipes, nutrition data, favorite recipes, and activity history.<br>- Define primary keys, foreign keys, relationships, and appropriate data types.<br>- Create Pydantic Schemas for request validation and response formatting.<br>- Separate schemas for recipe lists, recipe details, and nutrition information.<br>- Develop CRUD classes using SQLAlchemy.<br>- Build the Service Layer to handle business logic and separate it from the API Router. | 02/06/2026 | 02/06/2026 |  |
| 4 | - Develop API Routers for recipe and nutrition data.<br>- Create an API to retrieve paginated recipe lists.<br>- Create an API to retrieve random recipes.<br>- Create an API to retrieve recipe details by recipe ID.<br>- Create an API to retrieve nutrition information by `fdc_id`.<br>- Configure Response Models for each API.<br>- Test APIs using the FastAPI Swagger UI.<br>- Verify successful responses, resource not found scenarios, and invalid query parameters.<br>- Confirm that the backend can retrieve actual data from Amazon RDS. | 03/06/2026 | 03/06/2026 |  |
| 5 | - Create an Amazon EC2 instance running Ubuntu.<br>- Configure the key pair, VPC, Security Group, and required network rules.<br>- Connect to EC2 via SSH.<br>- Install Python, virtual environment, Git, Nginx, and required dependencies.<br>- Deploy the backend source code from GitHub to EC2.<br>- Configure environment variables and Amazon RDS connection settings.<br>- Run the backend using Uvicorn and verify connectivity between EC2 and RDS.<br>- Create a `systemd service` to automatically start and restart the backend if failures occur.<br>- Configure Nginx as a reverse proxy for FastAPI.<br>- Test the APIs after deployment on Amazon EC2. | 04/06/2026 | 04/06/2026 | <https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/EC2_GetStarted.html><br><https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/connect-linux-inst-ssh.html> |
| 6 | - Review the backend source code based on risks related to the OWASP Top 10.<br>- Check for SQL Injection risks and verify that SQLAlchemy ORM is used instead of raw SQL string concatenation.<br>- Verify the management of sensitive information and ensure that connection credentials are not hardcoded.<br>- Confirm that the `.env` file is excluded from GitHub.<br>- Restrict the values of `page`, `limit`, and other API input parameters.<br>- Use Pydantic Schemas for input validation and data constraints.<br>- Add handling for missing resources, invalid input data, and database query errors.<br>- Standardize HTTP status codes and error response formats.<br>- Prevent internal errors, stack traces, and database details from being exposed to users.<br>- Re-test the APIs after implementing security improvements and error handling. | 05/06/2026 | 05/06/2026 | <https://owasp.org/www-project-top-ten/><br><https://owasp.org/www-project-api-security/> |

### Week 7 Achievements

* Completed the FastAPI backend architecture by separating responsibilities into the following components:

  * API Router.
  * Dependencies.
  * ORM Models.
  * Pydantic Schemas.
  * CRUD.
  * Service Layer.
  * Database Session.
  * Environment Configuration.

* Successfully connected the backend to the `food_ai_db` database on Amazon RDS for MySQL using SQLAlchemy and PyMySQL.

* Configured database connection management:

  * Verified database connectivity before use.
  * Reused connections through a connection pool.
  * Automatically rolled back transactions when errors occurred.
  * Closed database sessions after each request.
  * Used the `utf8mb4` character set.

* Developed ORM Models and Pydantic Schemas for data retrieval, validation, and formatting.

* Completed the core APIs for recipe data:

  * `GET /recipes`: Retrieve a paginated list of recipes.
  * `GET /recipes/random`: Retrieve a random recipe.
  * `GET /recipes/{recipe_id}`: Retrieve recipe details by recipe ID.

* Completed the API for nutrition data:

  * `GET /nutrition/{fdc_id}`: Retrieve food and calorie information from USDA FoodData Central by ID.

* Completed API testing using Swagger UI:

  * Verified data retrieval from Amazon RDS.
  * Tested pagination.
  * Tested existing and non-existing resources.
  * Tested invalid parameters.
  * Verified response structures based on Pydantic Schemas.
  * Verified HTTP status codes.

* Successfully created and configured an Amazon EC2 instance running Ubuntu for backend deployment.

* Completed the runtime environment setup on Amazon EC2:

  * Python and virtual environment.
  * Dependencies listed in `requirements.txt`.
  * Git.
  * Uvicorn.
  * Nginx.
  * Systemd.

* Deployed the backend source code from GitHub to Amazon EC2 and configured the required environment variables.

* Successfully connected the FastAPI backend running on Amazon EC2 to Amazon RDS for MySQL.

* Configured a `systemd service` to:

  * Run the backend as a background service.
  * Automatically start when the server boots.
  * Automatically restart when the process fails.
  * Support backend status monitoring and log inspection.

* Configured Nginx as a reverse proxy for the FastAPI application.

* Verified that the APIs were functioning correctly and successfully retrieving production data after deployment on Amazon EC2.

* Completed a security review based on the OWASP Top 10 and OWASP API Security guidelines:

  * Reduced SQL Injection risks by using parameterized ORM queries.
  * Prevented sensitive information and database credentials from being stored directly in the source code.
  * Excluded the `.env` file from Git.
  * Validated and restricted user input.
  * Limited detailed information in error responses.
  * Used appropriate HTTP methods and status codes.
  * Reviewed deployment configurations and network access permissions.
  * Reviewed backend dependencies.

* Added input validation using Pydantic:

  * Validated data types.
  * Restricted pagination parameter values.
  * Rejected invalid input values.
  * Reduced the risk of requests generating excessively large database queries.

* Standardized API error handling:

  * Returned `404 Not Found` when resources did not exist.
  * Returned `422 Unprocessable Entity` for invalid input data.
  * Logged internal errors without exposing stack traces to users.
  * Rolled back database sessions when queries or data processing failed.

* Completed the core backend implementation and deployment environment on Amazon EC2, making it ready for Amazon Cognito authentication integration and the development of user-based APIs in the following week.