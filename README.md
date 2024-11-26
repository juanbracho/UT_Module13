## Project Overview:
This project is an ETL (Extract, Transform, Load) pipeline designed for managing crowdfunding campaign data. The goal is to clean and organize the data from various sources such as CSV files, Excel files, and database dumps, then transform the data into a structured format and store it in a Postgres database.

## Project Files:
- crowdfunding_db_schema.sql: SQL file containing the schema of the database including table definitions and relationships.
- crowdfunding_db.sql: SQL dump file used to populate the database with pre-existing data.
- ETL_Mini_Project_JBracho_JAlmendarez.ipynb: The main ETL pipeline notebook that performs the extraction, transformation, and loading of data.
- category.csv: CSV file containing category data (id, category name).
- contacts.csv: CSV file containing contact details (first name, last name, email).
- contacts.xlsx: Excel file containing additional contact information.
- subcategory.csv: CSV file containing subcategory data.
- campaign.csv: CSV file containing campaign information.
- crowdfunding.xlsx: Excel file with additional campaign data.
- crowdfundingErd.png: An ERD (Entity-Relationship Diagram) that visualizes the relationships between the database tables.
- Database Structure:
 * The database schema defines the following tables:
  * Category: Stores campaign categories.
  * Subcategory: Stores subcategories tied to the campaign category.
  * Contacts: Stores contact details for campaign owners.
  * Campaign: Stores campaign-specific information such as goals, pledges, and the relationship to contacts and categories.
- Key Components:
  * Extraction: Data is extracted from CSV files (category.csv, subcategory.csv, campaign.csv) and Excel files (contacts.xlsx, crowdfunding.xlsx).
  * Transformation: Data is cleaned, formatted, and transformed in Python using libraries such as Pandas. Operations include handling missing values, formatting date columns, and mapping foreign keys between related tables.
  * Loading: The cleaned and transformed data is loaded into a PostgreSQL database using the schema defined in crowdfunding_db_schema.sql.

## Steps to Run the Project:
# Database Setup:

- Run the crowdfunding_db_schema.sql script to create the necessary database tables.
- Populate the database using the crowdfunding_db.sql file.
- Run ETL Pipeline:
- Open the ETL_Mini_Project_JBracho_JAlmendarez.ipynb Jupyter notebook.
- Follow the instructions to execute each step of the ETL process. This will extract the raw data, transform it, and load it into the database.

## Visualize Relationships:

The ERD crowdfundingErd.png helps visualize the relationships between the tables. It shows how the contacts, campaigns, categories, and subcategories are related in the database.
Prerequisites:
Python Libraries:
pandas
sqlalchemy
psycopg2-binary (for Postgres connection)
PostgreSQL: Make sure you have PostgreSQL installed and configured to run the SQL schema and dump.
pgAdmin4: (Optional) You can use pgAdmin to manage your Postgres database and verify the data after loading.
Project Contributors:
Juan Bracho
Jorge Almendarez
Future Enhancements:
Data Validation: Implement automated data validation scripts to ensure the data meets quality standards before loading.
Incremental Load: Add support for incremental data loading to handle large datasets efficiently.
Dashboards: Create visualizations (e.g., campaign performance, goal vs pledged analysis) using tools like Tableau or Matplotlib.
