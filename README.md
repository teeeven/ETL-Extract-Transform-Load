# Extract Tranform Load (ETL)

## Project Overview -- Data Integration and Automation Project
This repository showcases an ETL pipeline designed to automate the integration of external API data into an organizational relational database (SQL Server database). The contents shown in this repository is for demonstrative purposes and efforts have been made to protect student and institutional data, this repository is meant to demonstrate my ability to handle and transform data from an API creating a pipeline to our company database so that reporting is possible. 
Project Overview: Automated Pipeline for API Integration
This project automates the process of calling an API, storing data in a structured SQL database, and preparing it for analysis in Power BI.

Below is an outline of the three main stages:
1. Pipeline: API Call
    - Purpose: Retrieve data from the API, including information on users, 
      groups, risk scores, phishing tests, and training campaigns.
    - Description: This stage uses API endpoints to gather raw data, transforming it 
      into a structured format for ingestion.

 2. Pipeline: SQL Table and Schema Creation
    - Purpose: Set up the SQL database structure for storing data.
    - Description: This stage defines tables and schemas for all required entities, 
      including users, groups, risk score histories, and phishing and training details.
      It includes drop-and-create commands to ensure the tables are up-to-date with the 
      most recent schema and enforce data integrity.

 3. Pipeline: SQL Table Insertion
    - Purpose: Insert the retrieved and processed data from the API into the SQL tables.
    - Description: This stage handles the actual insertion of data into the SQL database 
      while preserving foreign key constraints and ensuring that data types are aligned 
      with the database schema. All data insertions are done within a transaction for 
      atomicity, meaning that any insertion failure results in a full rollback, preserving 
      database consistency.

## Technologies Used
- Python: Used for the general scripting language, it handles the API interactions and data processing using libraries like Pandas and SQLAlchemy. In deployment, I've used Python's virtual environments to ensure proper dependency management.
- SQL: Employed for the data storage and designing the schema for the data to be stored with referential integrity.
- Power BI: Using DirectQuery, a means to connect to the SQL Server Database, a report is then designed in Power BI to create a visual narrative for the data that has been processed.
- Automation Scripts: Scheduled tasks for running the processes automatically.

## Challenges Faced
- Managing API rate limits and ensuring data integrity during transfers.
- Developing data cleaning and transformation scripts to meet specific reporting needs.
- Designing the database schema of tables to permanently store this information and in processing these types in dependency order.
- Implementing automation to ensure the pipeline runs efficiently without manual intervention.

## Project Outcomes
- Achieved full automation of the data retrieval and integration process, significantly reducing manual workload.
- Enhanced the timeliness and accuracy of reports, supporting better decision-making.

## How to Use This Repository
The three workbook files below are selected from a larger parent .py and .env file (not posted to GitHub) which consolidates the code to a single file. This is meant to elaborate on each step while keeping much of the content generalized.
- `data_fetcher.ipynb`: Script for fetching data from external APIs. This is the E, Extract.
- `data_transformer.ipynb`: Contains the data cleaning, schema creation, and transformation logic. This is closest to the T, Transform., as we are getting it dialed in to fit to the designed database schema
- `data_loader.sql`: This is the 'transaction' that enables integrating processed data into the database. This is the L, Load.

## Setup and Installation
- **Environment Setup:** To replicate this project or use parts of it, start by setting up a Python virtual environment and installing dependencies.
- **Running the Scripts:** Ensure that you have set the necessary environment variables and configurations as per your setup.

## Contributing
- While this project is mainly for demonstration, I encourage you to connect and learn with me. Follow me on [LinkedIn](https://www.linkedin.com/in/steven-orizaga) for more updates and shared scripts.

## Editor Notes
- Thanks for reading! I am learning how to create real-world applicable solutions and welcome feedback. I am very passionate about this type of Data Engineering work and would love to develop further to make this my full-time focus.
