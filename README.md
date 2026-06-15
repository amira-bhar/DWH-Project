# Data Warehouse Project

**Integrating CRM and ERP Systems using Medallion Architecture**

---

## Project Overview

End-to-end data warehouse implementation using Bronze → Silver → Gold layers.

| Layer | Purpose |
|-------|---------|
| Bronze | Raw data from sources |
| Silver | Cleaned & standardized data |
| Gold | Business-ready tables (Star Schema) |

---

## Tech Stack

- SQL Server / Azure SQL
- T-SQL Stored Procedures
- Git / GitHub

---

## Folder Structure
├── sql/
│ ├── 01_bronze/ # Table creation + data loading
│ ├── 02_silver/ # Cleansing + standardization
│ └── 03_gold/ # Dimensions + fact tables
├── docs/ # Documentation
└── reports/ # Project report

## How to Run
-- 1. Create database
CREATE DATABASE DataWarehouse;

-- 2. Run scripts in order
EXEC load_bronze;
EXEC load_silver;
EXEC load_gold;

## Author
Amira Bhar | Academic Year: 2025/2026