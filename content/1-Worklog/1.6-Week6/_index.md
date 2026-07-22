---
title: "Week 6 Worklog"
date: 2026-05-25
weight: 6
chapter: false
pre: " <b> 1.6. </b> "
---

### Objectives for Week 6:

* Inspect and analyze the structure of the selected datasets.
* Clean and standardize the recipe and nutritional datasets.
* Verify data quality after processing.
* Design a database suitable for the project’s features.
* Define the tables, data fields, primary keys, foreign keys, and relationships.
* Create and configure Amazon RDS for MySQL.
* Create the required database tables.
* Import the cleaned data into Amazon RDS.
* Verify the record counts, structure, and integrity of the imported data.

### Tasks Completed This Week:

| Day | Tasks | Start Date | Completion Date | References |
| --- | --- | --- | --- | --- |
| 2 | - Inspected the structure of the Food.com Recipes and Interactions dataset.<br>- Identified the data fields required for recipe search and recommendation features.<br>- Analyzed data types, missing values, invalid data, and duplicate records.<br>- Inspected fields with complex structures, including ingredients, raw ingredients, preparation steps, and category tags.<br>- Developed a recipe data preprocessing workflow using Python and pandas. | 25/05/2026 | 25/05/2026 | <https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags/data> |
| 3 | - Cleaned and standardized the recipe data.<br>- Converted the ingredient, preparation step, and category tag fields into consistent structures.<br>- Analyzed and processed duplicate records.<br>- Added statistical fields such as ingredient count, preparation step count, and category tag count.<br>- Rechecked required fields and removed records that did not meet the project’s requirements.<br>- Analyzed the USDA FoodData Central dataset and extracted the fields required for calorie lookup.<br>- Standardized the nutritional data into a structure suitable for import into MySQL. | 26/05/2026 | 26/05/2026 | <https://fdc.nal.usda.gov/data-documentation.html> |
| 4 | - Designed the database for the AI Recipe Finder project.<br>- Identified the main entities, including users, recipes, nutrition, favorite recipes, search history, and chat history.<br>- Designed the `users`, `recipes`, `nutrition`, `favorites`, `search_history`, and `chat_history` tables.<br>- Defined data types, primary keys, foreign keys, and required constraints.<br>- Determined that recipe fields containing complex data structures would be stored in JSON format.<br>- Designed indexes for fields frequently used in searches or table relationships.<br>- Completed the SQL files for creating the tables and indexes. | 27/05/2026 | 27/05/2026 |  |
| 5 | - Created an Amazon RDS DB instance using MySQL.<br>- Configured the deployment region, MySQL version, DB instance class, and storage capacity.<br>- Set up the administrator username and database connection information.<br>- Configured the VPC, subnet, public access setting, and Security Group.<br>- Configured an inbound rule to allow access to MySQL port 3306 from an authorized IP address.<br>- Verified the DB instance status and retrieved its connection endpoint.<br>- Connected to Amazon RDS from MySQL Workbench using an SSL connection.<br>- Created the database and executed the SQL file to initialize the tables. | 28/05/2026 | 28/05/2026 | <https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/CHAP_GettingStarted.CreatingConnecting.MySQL.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/USER_ConnectToInstance.html><br><https://docs.aws.amazon.com/AmazonRDS/latest/UserGuide/UsingWithRDS.SSL.html> |
| 6 | - Developed and executed a Python program to import the cleaned data into Amazon RDS.<br>- Imported nutritional data into the `nutrition` table.<br>- Imported recipe data into the `recipes` table in batches to reduce errors and use resources efficiently.<br>- Detected and handled records containing invalid JSON data during the import process.<br>- Compared the number of records before and after the data import.<br>- Executed sample queries to verify the recipe and nutritional data.<br>- Verified primary keys, foreign keys, indexes, and database constraints.<br>- Summarized the results and confirmed that the data was ready for backend development. | 29/05/2026 | 29/05/2026 |  |

### Results Achieved in Week 6:

* Completed the analysis, cleaning, and standardization of the Food.com recipe dataset.

* The processed recipe data includes the following main information:

  * Recipe ID.
  * Recipe name.
  * Description.
  * Standardized ingredient list.
  * Original ingredient list.
  * Preparation steps.
  * Number of servings and serving size.
  * Category tags.
  * Statistical fields related to ingredients, preparation steps, and tags.

* Completed the processing of the USDA FoodData Central dataset.

* The nutritional data was standardized into the following main fields:

  * Food ID (`fdc_id`).
  * Food name.
  * Data type.
  * Calorie value.

* Completed data quality verification after cleaning:

  * Verified the data structure and data types.
  * Checked for missing data.
  * Checked for duplicate records.
  * Validated JSON fields.
  * Checked for invalid values.
  * Randomly inspected several records after processing.

* Completed the database design for the project with the following tables:

  * `users`: Stores user information synchronized from Amazon Cognito.
  * `recipes`: Stores recipe data.
  * `nutrition`: Stores food and calorie data.
  * `favorites`: Stores users’ favorite recipes.
  * `search_history`: Stores users’ search history.
  * `chat_history`: Stores users’ chatbot conversation history.

* Defined the main relationships between the tables:

  * One user can save multiple favorite recipes.
  * One recipe can be saved as a favorite by multiple users.
  * One user can have multiple search history records.
  * One user can have multiple chat history records.
  * User data is linked to Amazon Cognito through `cognito_sub`.

* Applied appropriate primary keys, foreign keys, unique constraints, and indexes to maintain data integrity and support efficient queries.

* Successfully created an Amazon RDS DB instance using MySQL and completed the basic configuration:

  * Selected the MySQL version and DB instance class.
  * Configured the storage capacity.
  * Configured the VPC and Security Group.
  * Configured MySQL port 3306.
  * Retrieved the DB instance endpoint.
  * Connected using MySQL Workbench.
  * Used SSL to secure the database connection.

* Successfully created the `food_ai_db` database on Amazon RDS and initialized the tables according to the database design.

* Successfully imported the data into Amazon RDS:

  * **`nutrition` table:** 13,359 records.
  * **`recipes` table:** Approximately 402,000 valid records.

* Identified several recipe records that could not be imported because of invalid JSON data and skipped them to maintain database quality.

* Verified the imported data using the following queries:

  * Counted the total number of records in each table.
  * Retrieved random recipe records.
  * Inspected ingredient lists and preparation steps.
  * Queried calorie data by food ID.
  * Verified table structures, indexes, and constraints.

* Confirmed that the `recipes` and `nutrition` tables would be treated as static, read-only data sources after the import process was completed.

* Completed the preparation of the Amazon RDS database, making it ready for FastAPI backend development and integration in the following week.