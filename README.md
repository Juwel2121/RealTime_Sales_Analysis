# Mirrored Real-Time Sales Analysis Dashboard

A **real-time, zero-latency** sales analytics dashboard built with **Microsoft Fabric Mirroring + DirectLake** and visualized in **Power BI**.  
The goal is to monitor sales, products, profitability, and regional performance **without scheduled refreshes**—changes in the source system are reflected automatically.

---

## Dashboard Preview

![Real Time Sales Analysis](Mirrored%20Real%20Time%20Sales%20Analysis%20Dashboard_page-0001.jpg)

---

## Objective

Deliver a modern sales reporting solution that:
- updates in **near real-time** (no manual refresh),
- reduces ETL/refresh complexity,
- enables quick decisions for business teams using a single interactive report. :contentReference[oaicite:1]{index=1}

---

## Technical Architecture

**Source → Mirror → Model → Report**
- **Source System:** Azure SQL Database (live transactional sales)
- **Mirroring Layer:** Microsoft Fabric (Mirrored SQL Database)
- **Semantic Model:** DirectLake (Fabric)
- **Reporting:** Power BI Desktop + Power BI Service
- **Refresh Method:** Real-time synchronization (no scheduled refresh) :contentReference[oaicite:2]{index=2}

---

## What the Dashboard Covers

### KPI Panel (Live)
- Total Sales
- Total Orders
- Total Quantity
- Profit Margin %
- Profit
- Min Sales ID

### Visual Insights
- **Top products by sales**
- **Sales by payment method**
- **Sales & profit trend by month**
- **Sales by category**
- **Sales by region**
- Filters for **date range** and **order type** :contentReference[oaicite:3]{index=3}

---

## Included Sample Dataset (Local Demo)

This repo includes a sample dataset you can use without Fabric:

**File:** `BurgerSales.csv`  
**Rows:** 10,000  
**Date Range:** 2024-01-01 → 2024-12-31  

**Columns**
- SalesID, Date, Store, Region, Product, Category  
- QuantitySold, UnitPrice, UnitMakingCost  
- PaymentMethod, OrderType

### Sample totals (from `BurgerSales.csv`)
- Total Sales: ~498.98K  
- Total Orders: 10,000  
- Total Quantity: ~55.17K  
- Profit: ~377.31K  
- Profit Margin: ~75.62%

---

