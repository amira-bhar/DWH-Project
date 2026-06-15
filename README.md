# Data Warehouse Project

**Integrating CRM and ERP Systems using Medallion Architecture**

---

## Project Overview

This project implements an end-to-end data warehouse integrating CRM and ERP source systems using the **Medallion Architecture** (Bronze → Silver → Gold).

**The problem:** Manual reporting takes weeks, produces inconsistent data, and is full of errors.

**The solution:** An automated ETL pipeline that delivers clean, historical, business-ready data in hours — a single source of truth for all analytics.

**Key results:**
- Report generation: Weeks → Hours
- Data consistency: ✅ Single source of truth
- Automation: ✅ Zero manual steps

---

## Tech Stack

- SQL Server / Azure SQL
- T-SQL Stored Procedures
- Git / GitHub

## Data Architecture
The data architecture for this project follows Medallion Architecture Bronze, Silver, and Gold layers:

1. **Bronze Layer**: Stores raw data as-is from the source systems. Data is ingested from CSV Files into SQL Server Database.
2. **Silver Layer**: This layer includes data cleansing, standardization, and normalization processes to prepare data for analysis.
3. **Gold Layer**: Houses business-ready data modeled into a star schema required for reporting and analytics.
---

## Folder Structure
```
DWH-Project/
│
├── datasets/                           # Raw datasets used for the project (ERP and CRM data)
│
├── docs/                               # Project documentation
│   ├── data_catalog.md                 # Catalog of datasets, including field descriptions and metadata
│   └── naming-conventions.md           # Consistent naming guidelines for tables, columns, and files
│
├── scripts/                            # SQL scripts for ETL and transformations
│   ├── bronze/                         # Scripts for extracting and loading raw data
│   ├── silver/                         # Scripts for cleaning and transforming data
│   └── gold/                           # Scripts for creating analytical models
│
├── tests/                              # Test scripts and quality files
│
├── README.md                           # Project overview and instructions
├── LICENSE                             # License information for the repository
└── .gitignore                          # Files and directories to be ignored by Git
```


## How to Run
```
-- 1. Create database
CREATE DATABASE DataWarehouse;

-- 2. Run scripts in order

EXEC load_bronze;

EXEC load_silver;

EXEC load_gold;
```


## Author
Amira Bhar | Academic Year: 2025/2026