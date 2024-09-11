# Credit Card Fraud Detection with GPT-Powered Text-to-SQL

This repository contains a Python-based application designed to simplify querying credit card fraud data by converting natural language queries into SQL using the **GPT API**. Users can interact with the dataset without requiring SQL expertise, making data analysis more accessible.

## Key Features

- **Database Setup**: Load the credit card fraud data into an **SQLite** database for structured querying.
- **Text-to-SQL**: Leverage the **GPT API** to automatically convert natural language questions into SQL queries.
- **Query Execution & Results**: Execute SQL queries on the database and display results in a **pandas DataFrame**.
- **SQL Query Display**: The generated SQL query is displayed alongside the query results for transparency and learning.

## Installation

 Obtain your GPT API key and add it to your environment variables:
    ```bash
    export api_key ='your-api-key'
    ```

## How to Use

1. **Set up the database**: 
    - Load the `Credit_Card_Fraud.csv` file into the SQLite database using the provided scripts in the Jupyter Notebook.

2. **Run the Jupyter Notebook**:
    - Open the notebook and enter your natural language queries in the specified cell. The GPT API will convert your question into an SQL query.

3. **View the Results**:
    - The notebook will execute the SQL query and display the results in a pandas DataFrame. It will also show the corresponding SQL query for transparency.

## Example

**Input**:  
*"Show all fraud cases from 2019"*

**Generated SQL Query**:  
```sql
SELECT * FROM FRAUD_TABLE WHERE IS_FRAUD = 1 AND YEAR = 2019;
