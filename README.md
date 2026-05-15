# E-Commerce-ADF-Project

## 📌 Project Overview

This project demonstrates an end-to-end Azure Data Factory (ADF) Data Flow pipeline for processing E-Commerce customer and order data using Medallion Architecture (Bronze, Silver, Gold).

The pipeline performs:
- Data ingestion
- Data cleaning
- Join transformations
- Aggregation
- Final sink output generation

---

## 🏗️ Architecture

The project follows the Bronze → Silver → Gold architecture.

### Bronze Layer
Raw customer and orders data are ingested from source files.

### Silver Layer
Data is cleaned and transformed using Mapping Data Flow transformations.

### Gold Layer
Business-ready aggregated customer summary data is generated.

---

## ⚙️ Technologies Used

- Azure Data Factory
- Azure Data Flows
- Azure Data Lake Storage
- GitHub Integration
- CSV / JSON Files

---

## 🔄 Data Flow Process

### 1️⃣ Customer Source
Customer data is imported from JSON source.

Columns:
- customer_id
- name
- city
- email
- signup_date

---

### 2️⃣ Orders Source
Orders data is imported from Delimited Text source.

Columns:
- order_id
- customer_id
- product
- amount
- date

---

### 3️⃣ CustomerClean Transformation
Customer data columns are cleaned and renamed.

---

### 4️⃣ OrderClean Transformation
Orders data columns are cleaned and renamed.

---

### 5️⃣ Join Transformation
Customer and Orders datasets are joined using:

customer_id

Join Type:
- Inner Join

---

### 6️⃣ Aggregate Transformation
Data is aggregated by:
- customer_id
- name
- city

Calculated Columns:
- total_orders
- total_spent

---

### 7️⃣ Sink Output
Final transformed data is exported to sink dataset.

---

## 📊 Sample Output

| customer_id | name         | city       | total_orders | total_spent |
|-------------|--------------|------------|--------------|-------------|
| 101         | Ravi Kumar   | Bangalore  | 2            | 65000       |
| 102         | Anita Sharma | Hyderabad  | 1            | 20000       |
| 103         | Kiran Reddy  | Chennai    | 1            | 20000       |

---

## 📂 Repository Structure

- pipeline/ → ADF Pipelines
- dataflow/ → Mapping Data Flows
- dataset/ → Datasets
- linkedService/ → Linked Services
- factory/ → Factory Configuration

---

## 🚀 Features

- End-to-end ETL pipeline
- Mapping Data Flow transformations
- Join and Aggregation operations
- GitHub integrated ADF project
- Medallion Architecture implementation

---

## 👨‍💻 Author

Pavan Kumar SV  
MCA - T John Institute of Technology
