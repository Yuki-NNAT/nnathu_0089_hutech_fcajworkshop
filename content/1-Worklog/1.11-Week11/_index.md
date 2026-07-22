---
title: "Week 11 Worklog"
date: 2026-06-27
weight: 11
chapter: false
pre: " <b> 1.11. </b> "
---

### Week 11 Objectives

* Perform comprehensive testing of the AI Recipe Finder system based on the main user workflows.
* Verify the integration between the frontend, Amazon Cognito, FastAPI backend, AI component, and Amazon RDS.
* Identify, classify, and resolve the remaining issues after the integration process.
* Review and optimize the performance of the backend and the database.
* Finalize the deployment version on AWS.
* Update the technical documentation for system operation and handover.

### Tasks carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Create a comprehensive system testing checklist based on the completed functionalities.<br>- Identify the main testing workflows, including user sign-in, user authentication, viewing the recipe list, viewing recipe details, and retrieving nutrition data.<br>- Identify workflows involving the frontend, backend, Amazon Cognito, AI component, and Amazon RDS.<br>- Prepare valid data, invalid data, and boundary test cases.<br>- Define the expected results and corresponding HTTP status codes for each test case.<br>- Assign responsibilities and agree on the issue reporting process with the team members. | 29/06/2026 | 29/06/2026 |  |
| 3 | - Perform end-to-end testing of all main workflows from the frontend to the backend and database.<br>- Verify the sign-in process through Amazon Cognito and the transmission of the Access Token to the backend.<br>- Test both public APIs and APIs requiring authentication.<br>- Verify user information synchronization with the `users` table in Amazon RDS.<br>- Verify the retrieval of recipe lists, recipe details, and nutrition data.<br>- Collaborate in testing the data exchange workflow between the backend and the AI component.<br>- Monitor logs to record issues, occurrence times, and related components.<br>- Summarize the testing results for each system function. | 30/06/2026 | 30/06/2026 |  |
| 4 | - Classify the recorded issues according to the frontend, backend, Amazon Cognito, AI component, database, or deployment configuration.<br>- Resolve issues within the scope of the backend and database.<br>- Adjust endpoints, Pydantic Schemas, exception handling, or error messages when necessary.<br>- Test scenarios involving missing tokens, invalid tokens, invalid input data, or non-existent resources.<br>- Verify transaction rollback when database operations fail.<br>- Perform regression testing on the updated functionalities.<br>- Record issues that require coordination with the frontend or AI team members for further resolution. | 01/07/2026 | 01/07/2026 |  |
| 5 | - Measure the response time of frequently used APIs.<br>- Review queries for retrieving recipe lists, recipe details, nutrition data, and user information.<br>- Verify the use of pagination to limit the amount of returned data.<br>- Review indexes related to frequently searched or linked fields.<br>- Verify the SQLAlchemy connection pool configuration and connection reuse with Amazon RDS.<br>- Monitor CPU usage, memory usage, service status, and runtime logs on Amazon EC2.<br>- Optimize components causing slow responses or inefficient resource usage.<br>- Recheck the results and response times after optimization. | 02/07/2026 | 02/07/2026 |  |
| 6 | - Update the source code containing bug fixes and optimizations to GitHub.<br>- Deploy the finalized backend version to Amazon EC2.<br>- Restart the backend service and verify its operational status.<br>- Re-test the APIs and critical integration workflows after deployment.<br>- Review the environment variable configuration, CORS settings, and Amazon RDS connectivity.<br>- Monitor logs to ensure that no critical issues appear after the update.<br>- Complete the API documentation, backend configuration guide, deployment guide, and operation guide.<br>- Update the system architecture, source code structure, and technical notes for project handover.<br>- Summarize the testing results, resolved issues, and remaining limitations. | 03/07/2026 | 03/07/2026 |  |

### Week 11 Expected Outcomes

* Complete the comprehensive testing checklist for the AI Recipe Finder system.
* Verify the main workflows, including:

  * User sign-in and authentication using Amazon Cognito.
  * Sending the Access Token from the frontend to the backend.
  * Synchronizing and retrieving user information.
  * Viewing recipe lists and recipe details.
  * Retrieving nutrition data.
  * Exchanging data between the backend and the AI component.
  * Connecting to and retrieving data from Amazon RDS.

* Record and classify issues according to each system component.
* Resolve issues within the scope of the backend and database.
* Re-test the updated functionalities to minimize regression issues.
* Verify that the backend properly handles invalid tokens, invalid input data, and non-existent resources.
* Review the response time of the main APIs.
* Optimize database queries, pagination, indexes, and database connection configuration when necessary.
* Verify the status of backend resources and services on Amazon EC2.
* Update the finalized source code on GitHub.
* Deploy and verify that the final backend version operates reliably on Amazon EC2.
* Complete the API documentation, backend configuration, deployment, and operation guides.
* Summarize the testing results, resolved issues, and remaining limitations.
* Prepare the content for writing the internship report and handing over the project in Week 12.