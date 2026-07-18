# RedFlag — Fraud Detection Dataset (Week 3 Minor Project) 🚀

Welcome to the **RedFlag** repository! This project was completed as part of the Data Analytics/Data Science track at **The Unlox Academy**. It focuses on database design, massive data ingestion, performance optimization, and preparing a large-scale transaction dataset for fraud analytics.

---

## 📌 Project Overview
The objective of this project was to design and implement a robust **MySQL** database capable of handling **200,000 synthetic transactions** generated to simulate **PayFast** (a fictional Indian payment aggregator). 

The dataset captures a high-volume, 6-month timeline (January 1, 2024 – June 30, 2024), incorporating realistic payment behaviors, multiple statuses, and geographic distributions across major Indian hubs.

---

## 🛠️ Tech Stack & Tools
* **Database Management System:** MySQL
* **Interface:** MySQL Workbench
* **Language:** SQL (DDL, DML)

---

## 💡 Key Features & Technical Implementations

### 1. Database Schema & Architecture
Designed a highly structured relational schema tailored to manage high-velocity financial data. The architecture successfully accounts for edge cases, including varied transaction statuses (`SUCCESS`, `FAILED`), transaction types (`DEBIT`, `REFUND`), and widespread geographic tracking (Delhi, Mumbai, Bengaluru, etc.).

### 2. Performance Tuning & Indexing
To ensure low latency during fraud detection queries, I implemented strategic multi-column indexing:
* `idx_user`: To track specific user transaction histories rapidly.
* `idx_time`: For time-series analysis and spotting high-velocity fraud spikes.
* `idx_merchant`: For analyzing merchant-side risk and chargeback ratios.

### 3. Bulk Data Optimization
Ingesting 200,000 records smoothly can introduce timeout challenges. I successfully troubleshooted and resolved MySQL Workbench timeout errors by modifying the environment configurations (`DBMS connection read timeout`), ensuring stable bulk processing of massive system files.

---

## 📁 Repository Structure

```text
├── Data/                 # (Optional) Place data dictionary or sample CSVs here
├── Scripts/
│   ├── schema.sql        # Database initialization, tables, and constraints
│   ├── indexing.sql      # Performance optimization scripts
│   └── queries.sql       # Initial exploratory analysis queries
└── README.md             # Project documentation
