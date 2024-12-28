# Data Integration and Automation Project

## Project Overview -- Extract Tranform Load (ETL)
This repository showcases an ETL pipeline designed to automate the integration of external API data into an organizational relational database (SQL Server database). The contents shown in this repository is for demonstrative purposes and efforts have been made to protect student and institutional data, this repository is meant to demonstrate my ability to handle and transform data from an API creating a pipeline to our company database so that reporting is possible. 

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
- `data_fetcher.py`: Script for fetching data from external APIs. This is the E, Extract.
- `data_transformer.py`: Contains the data cleaning and transformation logic. This is the T, Transform.
- `data_storage.sql`: SQL scripts for integrating processed data into the database. This is the L, Load.

## Setup and Installation
- **Environment Setup:** To replicate this project or use parts of it, start by setting up a Python virtual environment and installing dependencies.
- **Running the Scripts:** Ensure that you have set the necessary environment variables and configurations as per your setup.

## Contributing
- While this project is mainly for demonstration, I encourage you to connect and learn with me. Follow me on [LinkedIn](https://www.linkedin.com/in/steven-orizaga) for more updates and shared scripts.

## Editor Notes
- Thanks for reading! I am learning how to create real-world applicable solutions and welcome feedback. I am very passionate about this type of Data Engineering work and would love to develop further to make this my full-time focus.
