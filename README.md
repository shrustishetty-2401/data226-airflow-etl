# Airflow Country Capital ETL Pipeline

This project implements an ETL pipeline using Apache Airflow and Snowflake.

## Pipeline Steps

1. Extract  
Fetch country and capital data from a public API.

2. Transform  
Clean the data and filter valid country-capital pairs.

3. Load  
Load the processed data into Snowflake.

## Technologies Used

- Apache Airflow
- Snowflake
- Python
- REST API

## DAG Structure

extract → transform → load

## Features

- Uses Airflow Variables
- Uses Snowflake Connection
- Full refresh implemented using SQL transaction
- Data loaded into Snowflake table `COUNTRY_CAPITALS`

## Example Query

```sql
SELECT *
FROM USER_DB_RABBIT.PUBLIC.COUNTRY_CAPITALS;
