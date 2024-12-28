# -------------------------------------------------------------------------------
# Project Overview: Automated Pipeline for API Integration
# -------------------------------------------------------------------------------
# This project automates the process of calling an API, storing data in a 
# structured SQL database, and preparing it for analysis in Power BI.
# 
# Below is an outline of the three main stages:
#
# 1. Pipeline: API Call
#    - Purpose: Retrieve data from the API, including information on users, 
#      groups, risk scores, phishing tests, and training campaigns.
#    - Description: This stage uses API endpoints to gather raw data, transforming it 
#      into a structured format for ingestion.
#
# 2. Pipeline: SQL Table and Schema Creation
#    - Purpose: Set up the SQL database structure for storing data.
#    - Description: This stage defines tables and schemas for all required entities, 
#      including users, groups, risk score histories, and phishing and training details.
#      It includes drop-and-create commands to ensure the tables are up-to-date with the 
#      most recent schema and enforce data integrity.
#
# 3. Pipeline: SQL Table Insertion
#    - Purpose: Insert the retrieved and processed data from the API into the SQL tables.
#    - Description: This stage handles the actual insertion of data into the SQL database 
#      while preserving foreign key constraints and ensuring that data types are aligned 
#      with the database schema. All data insertions are done within a transaction for 
#      atomicity, meaning that any insertion failure results in a full rollback, preserving 
#      database consistency.
#
# -------------------------------------------------------------------------------
# End of Project Overview
# -------------------------------------------------------------------------------
