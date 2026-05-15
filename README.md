# E-Commerce-ADF-Project
# E-Commerce-ADF-Project

## 📌 Overview
This project demonstrates an end-to-end Azure Data Factory (ADF) pipeline for processing E-Commerce sales and customer data using Bronze, Silver, and Gold architecture.

The project includes data ingestion, transformation, aggregation, and loading using Azure Data Factory Data Flows and Pipelines.

---

## 🏗️ Architecture

The pipeline follows the Medallion Architecture:

1. Bronze Layer  
   - Raw customer and orders data ingestion

2. Silver Layer  
   - Data cleaning and transformations

3. Gold Layer  
   - Aggregated business-ready customer summary data

---

## ⚙️ Technologies Used

- Azure Data Factory (ADF)
- Azure Data Lake Storage Gen2
- Azure Databricks
- GitHub
- CSV / JSON datasets

---

## 🔄 Pipeline Flow

### Step 1: Source Data
Customer and Orders data are loaded from source files.

### Step 2: Data Cleaning
Data is cleaned and renamed using Mapping Data Flows.

### Step 3: Join Transformation
Customer and Orders datasets are joined using customer_id.

### Step 4: Aggregation
Total orders and total spending are calculated for each customer.

### Step 5: Sink Output
Final transformed data is stored in the Gold layer.

---

## 📂 Repository Structure

- pipeline/ → ADF pipelines
- dataset/ → Datasets used in ADF
- linkedService/ → Storage and service connections
- dataflow/ → Mapping data flows
- factory/ → Factory configuration

---

## 📊 Sample Output

| customer_id | name  | city      | total_orders | total_spent |
|-------------|-------|-----------|--------------|-------------|
| 101         | Ravi  | Bangalore | 2            | 95000       |
| 102         | Anita | Hyderabad | 1            | 20000       |
| 103         | Kiran | Chennai   | 1            | 20000       |

---

## 🚀 Features

- End-to-end ETL pipeline
- Bronze-Silver-Gold architecture
- Data transformation using Mapping Data Flow
- GitHub integration with ADF
- Aggregated analytical output

---

## 👨‍💻 Author

Pavan Kumar SV  
MCA - T John Institute of Technology
