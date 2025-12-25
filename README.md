# Incremental Sales & Customer Analysis (Power BI)

A single-page **Power BI** dashboard for analyzing **sales performance** and **customer/product behavior**.  
It’s built on a simple **star schema** (FactSales + Dimensions) and designed for quick, interactive decision-making.

---

## Dashboard Preview

![Sales Analysis Dashboard](Images/Project(Sales).jpg)

---

## What This Dashboard Answers

- How are **sales trending over time** (monthly/periodic patterns)?
- Which **regions** drive the most revenue?
- Which **product categories** generate the most **sales vs quantity**?
- How many **customers**, **orders**, and **distinct products sold** are involved?
- What are the top/lowest performing segments after applying filters?

---

## Key KPIs (from the included dataset)

- **Total Sales:** ~50.08M  
- **Total Quantity Sold:** ~550K  
- **Total Orders:** ~100K  
- **Total Customers (active):** 144  
- **Total Sold Products (distinct):** 63  
- **Avg Sales per Customer:** ~347.77K  
- **Last Data Update:** 2025-08-28

> Note: “Avg Sales per Customer” = Total Sales / Active Customers.

---

## Dataset (CSV)

All data files are included in [`Database/`](Database):

- `Database/FactSales.csv` — transactions (SaleID, CustomerID, ProductID, DateID, Quantity, LastUpdatedTime)
- `Database/DimProducts.csv` — product master (Category, UnitPrice, etc.)
- `Database/DimCustomers.csv` — customer info (Region, etc.)
- `Database/DimDates.csv` — date table (calendar & fiscal attributes)

**Date range covered:**
- Date table: **2024-01-01 → 2025-12-31**
- Fact sales: **2024-01-01 → 2025-08-27**

---

## Data Model (Star Schema)

**Relationships**
- `FactSales[CustomerID]` → `DimCustomers[CustomerID]`
- `FactSales[ProductID]` → `DimProducts[ProductID]`
- `FactSales[DateID]` → `DimDates[Date]`

This structure enables fast slicing by **time**, **region**, and **category**.

---

 
