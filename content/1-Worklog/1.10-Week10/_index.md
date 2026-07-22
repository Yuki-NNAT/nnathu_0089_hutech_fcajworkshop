---
title: "Week 10 Worklog"
date: 2026-06-20
weight: 10
chapter: false
pre: " <b> 1.10. </b> "
---

### Week 10 Objectives

* Complete the backend functionalities required for system integration.
* Recheck the connection established in the previous week between the frontend, Amazon Cognito, and the backend.
* Verify data exchange between the backend and the AI component.
* Receive and analyze issues that arise during the integration process.
* Adjust APIs, data structures, and backend configurations based on the integration results.
* Confirm that all components can connect and operate correctly according to the designed workflow.
* Prepare the system for the overall testing phase in the following week.

### Tasks carried out this week

| Day | Task | Start Date | Completion Date | Reference Material |
| --- | --- | --- | --- | --- |
| 2 | - Review the progress of the implemented backend functionalities.<br>- Compare the existing API list with the requirements of the frontend and AI components.<br>- Identify the endpoints, data fields, or functionalities that need to be adjusted for the integration process.<br>- Verify the consistency of field names, data types, and response structures.<br>- Summarize the topics that need to be discussed with each team member.<br>- Create an integration testing checklist for the frontend, backend, database, and AI component. | 22/06/2026 | 22/06/2026 |  |
| 3 | - Complete the remaining backend functionalities required for integration.<br>- Adjust the Pydantic Schemas according to the data structures used by the system components.<br>- Standardize the request and response formats of the related APIs.<br>- Verify the handling of optional or missing data fields.<br>- Add appropriate error messages so that API consumers can identify the causes of errors.<br>- Verify API compatibility after the adjustments. | 23/06/2026 | 23/06/2026 |  |
| 4 | - Recheck the connection established in the previous week between the frontend, Amazon Cognito, and the backend.<br>- Verify that the frontend calls the APIs through the backend deployed on Amazon EC2.<br>- Verify the URL, HTTP method, Authorization Header, query parameters, and request body.<br>- Verify that the Access Token is sent in the correct Bearer Token format when calling authenticated APIs.<br>- Verify the response structure and HTTP status codes received by the frontend.<br>- Verify the CORS configuration for localhost and the frontend hosted on AWS Amplify.<br>- Monitor the backend logs to identify issues occurring during data exchange. | 24/06/2026 | 24/06/2026 |  |
| 5 | - Collaborate with the frontend team member to verify API workflows from the user interface.<br>- Verify request and response data while the frontend interacts with the backend.<br>- Collaborate with the AI team member to verify recipe and nutrition data retrieval through the backend.<br>- Compare the endpoints and input/output data structures used by the AI component.<br>- Test scenarios involving missing data, invalid data, or non-existent resources.<br>- Monitor request logs to identify the source of issues.<br>- Classify issues related to the frontend, backend, AI component, database, or deployment configuration.<br>- Record the testing results and the required adjustments. | 25/06/2026 | 25/06/2026 |  |
| 6 | - Adjust the backend based on the issues and feedback received during integration.<br>- Resolve inconsistencies between requests and responses.<br>- Modify the Pydantic Schemas, endpoints, CORS configuration, or environment variables if necessary.<br>- Re-test the workflows that previously encountered issues.<br>- Verify that data is correctly stored in and retrieved from Amazon RDS.<br>- Update the backend source code on GitHub and deploy the new version to Amazon EC2.<br>- Restart the backend service and verify its operational status after deployment.<br>- Summarize the resolved issues and the remaining tasks dependent on other team members' progress.<br>- Prepare the system for the overall testing phase in the following week. | 26/06/2026 | 26/06/2026 |  |

### Week 10 Expected Outcomes

* Review and complete the backend functionalities required for system integration.
* Standardize the request and response structures between the backend and the components consuming the APIs.
* Complete the integration testing checklist for:

  * Frontend.
  * FastAPI backend.
  * AI component.
  * Amazon Cognito.
  * Amazon RDS.
  * Amazon EC2.

* Recheck the frontend connection established in the previous week.
* Verify that the frontend sends the Access Token in the correct format when calling authenticated APIs.
* Verify the URL, HTTP method, headers, query parameters, and request body sent by the frontend.
* Verify the CORS configuration for localhost and the frontend hosted on AWS Amplify.
* Verify the response structure and HTTP status codes received by the frontend.
* Verify data exchange between the backend and the AI component.
* Verify recipe and nutrition data retrieval through the backend.
* Record and classify issues according to each system component.
* Adjust the Pydantic Schemas, endpoints, CORS configuration, environment variables, and error handling based on the integration results.
* Re-test the adjusted workflows and verify that data is transmitted in the correct format.
* Update the modified backend version to GitHub and deploy it to Amazon EC2.
* Verify the operational status of the backend after deploying the new version.
* Summarize the items that could not yet be tested due to dependencies on the progress of other team members.
* Prepare the system version for the overall testing activities in the following week.