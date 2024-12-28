# Extract Transform Load (ETL)

## Project Overview -- Data Integration and Automation Project
This repository showcases an ETL pipeline designed to automate the integration of external API data into an organizational relational database (SQL Server database). The contents shown in this repository are for demonstrative purposes, and efforts have been made to protect student and institutional data. This repository is meant to demonstrate my ability to handle and transform data from an API, creating a pipeline to our company database so that reporting is possible.

### Automated Pipeline for API Integration
This project automates the process of calling an API, storing data in a structured SQL database, and preparing it for analysis in Power BI.

Below is an outline of the three main stages:

1. **Pipeline: API Call**
   - **Purpose**: Retrieve data from the API, including information on users, groups, risk scores, phishing tests, and training campaigns.
   - **Description**: This stage uses API endpoints to gather raw data, transforming it into a structured format for ingestion.

2. **Pipeline: SQL Table and Schema Creation**
   - **Purpose**: Set up the SQL database structure for storing data.
   - **Description**: This stage defines tables and schemas for all required entities, including users, groups, risk score histories, and phishing and training details. It includes drop-and-create commands to ensure the tables are up-to-date with the most recent schema and enforce data integrity.

3. **Pipeline: SQL Table Insertion**
   - **Purpose**: Insert the retrieved and processed data from the API into the SQL tables.
   - **Description**: This stage handles the actual insertion of data into the SQL database while preserving foreign key constraints and ensuring that data types are aligned with the database schema. All data insertions are done within a transaction for atomicity, meaning that any insertion failure results in a full rollback, preserving database consistency.

## Technologies Used
- **Python**: Handles the API interactions and data processing using libraries like Pandas and SQLAlchemy. Deployed within virtual environments to ensure proper dependency management.
- **SQL**: Used for data storage and schema design, ensuring referential integrity and optimization for reporting.
- **Power BI**: Utilized to connect to the SQL Server Database via DirectQuery, providing dynamic reports that create a visual narrative for the processed data.
- **Automation Scripts**: Scheduled tasks ensure the pipeline runs efficiently without manual intervention.

## Challenges Faced
- Managing API rate limits and ensuring data integrity during transfers.
- Developing robust data cleaning and transformation scripts to meet specific reporting needs.
- Designing the database schema to efficiently store data while maintaining dependency order and referential integrity.
- Implementing automation to ensure the pipeline runs seamlessly and consistently.
- Ensuring data anonymization to protect sensitive information while retaining analytical utility.

## Project Outcomes
- Achieved full automation of the data retrieval and integration process, significantly reducing manual workload.
- Enhanced timeliness and accuracy of reports, improving decision-making processes.
- Implemented anonymization techniques to safeguard sensitive information without compromising data quality.

## How to Use This Repository
The three workbook files below are selected from a larger parent `.py` and `.env` file (not posted to GitHub) which consolidates the code into a single file. These files elaborate on each step while keeping much of the content generalized:
- `data_fetcher.ipynb`: Script for fetching data from external APIs. This is the **Extract** phase.
- `data_transformer.ipynb`: Contains the data cleaning, schema creation, and transformation logic. This corresponds to the **Transform** phase, preparing data for database integration.
- `data_loader.ipynb`: Executes the process of integrating processed data into the database. This is the **Load** phase.

## Setup and Installation
1. Clone the repository to your local environment.
2. Set up a Python virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Configure your `.env` file with the necessary environment variables (e.g., database connection string).
5. Run the scripts in the order provided to execute the pipeline.

## Contributing
While this project is mainly for demonstration, I encourage you to connect and learn with me. Follow me on [LinkedIn](https://www.linkedin.com/in/steven-orizaga) for more updates and shared scripts.

## Editor Notes
Thank you for reading! I am continuously learning how to create real-world applicable solutions and welcome feedback. I am passionate about this type of Data Engineering work and aspire to make it my full-time focus.

