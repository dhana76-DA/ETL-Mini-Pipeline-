# ETL-Mini-Pipeline— Python Extract → Transform → Load 

Retail Sales ETL Mini Pipeline
Project Overview

This project demonstrates a mini ETL (Extract, Transform, Load) pipeline built using Python in Google Colab. The objective is to extract raw retail sales data from a CSV file, clean and transform it into an analytics-ready format, and load the processed data into structured outputs such as CSV files and a SQLite database.

The project follows standard data engineering practices including folder organization, data validation, transformation logic, and output verification.

Project Objectives

Load a raw retail sales dataset from a Kaggle CSV file
Organize the project using a clear folder structure
Clean missing values and remove duplicate records
Standardize column names and data types
Create derived business metrics such as profit margin and sales segments
Split the transformed data into multiple analytical outputs

Tools & Technologies Used

Google Colab – Development and execution environment
Python (pandas) – Data extraction, transformation, and loading
SQLite – Lightweight relational database for structured storage
CSV Files – Input and output data format
Excel – Data preview and validation
GitHub – Version control and project hosting
ZIP Files – Packaging final outputs for submission

Project Folder Structure
project/
│
├── raw/
│   └── retail_sales_raw.csv
│
├── processed/
│   └── retail_sales_processed.csv
│
└── output/
    ├── customers.csv
    ├── products.csv
    ├── orders.csv
    └── retail_sales.db
    
ETL Workflow Description
1️ Extract

The raw retail sales dataset is loaded from a Kaggle CSV file into Google Colab.
A copy of the raw dataset is saved in the raw/ directory for reference and audit purposes.

2️ Transform

The following transformations are applied:
Removal of duplicate records
Handling missing values in quantity, price, and sales columns
Standardization of column names (lowercase, underscores)
Conversion of data types (date, numeric fields)

Creation of derived columns:
Profit
Margin
High-value sale flag
Bulk order flag

3 Load

The cleaned and transformed dataset is saved to the processed/ folder as a CSV file
The data is split into multiple outputs:
Customers table
Products table
Orders table
Final outputs are exported as CSV files and also loaded into a SQLite database

Data Validation

Row counts are validated before and after transformation
Duplicate records are verified to be removed
Missing values are checked in the processed dataset
SQLite tables are queried to confirm successful data loading

Final Deliverables

Cleaned and processed CSV files
SQLite database containing structured tables
Zipped project output for easy submission
Reproducible ETL pipeline code in Google Colab

Conclusion

This ETL mini pipeline successfully converts raw retail sales data into structured, analytics-ready datasets. The project demonstrates essential data engineering skills such as data cleaning, transformation, validation, and loading using industry-standard tools and workflows.

This project implements an end-to-end ETL pipeline using Python and pandas. Raw retail sales data was extracted from a CSV file, cleaned to handle missing values and duplicates, and transformed by standardizing formats and creating business-ready metrics such as profit and margin. The processed data was then split into customer, product, and order datasets and saved in structured folders for analytics and reporting use.

In the load phase, the transformed datasets were exported as CSV files and also stored in a SQLite database. Separate tables for customers, products, and orders were created to support structured querying and analytics. The database load was verified using SQL queries to ensure data integrity and successful ingestion.


The SQLite connection was properly closed using conn.close() after data loading. This was verified by attempting to execute a query on the closed connection, which raised a database operation error. The database could be successfully accessed again only after reopening a new connection.

Row count validation was performed to ensure data integrity across ETL stages. The processed dataset contained fewer rows than the raw dataset due to removal of duplicates and invalid records. Output tables were validated to confirm consistency between processed data and final loaded datasets.

The final processed CSV files and SQLite database were downloaded from Google Colab using the built-in file download utility. All outputs were also compressed into a single ZIP file for easy submission and portability.
