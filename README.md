# Power BI Data Modelling Project

A Power BI data modelling project focused on transforming messy sample business data into a structured analytical model.

> This is a guided learning project based on a YouTube tutorial. The dataset was provided by the tutorial creator and contains sample data.

---

## 📌 Project Overview

The project started with multiple raw business tables containing sales, customers, products, campaigns, inventory, orders, and other business information.

The main objective was to understand how to transform these tables into a proper Power BI data model and use the model to create meaningful analytical reports.

### Before

![Before Data Modelling](screenshots/Before-Data-Modelling.png)

### After

![After Data Modelling](screenshots/After-Data-Modelling.png)

---

## 🏗️ Data Model

The final model is organized around **fact and dimension tables**.

### Dimension Tables

- `dim_customer`
- `dim_products`
- `dim_date`
- `dim_geo`
- `dim_campaign`
- `dim_order_flags`

### Fact Tables

- `fact_sales`
- `fact_inventory`
- `fact_campaign_spend`
- `fact_promotion_coverage`
- `fact_order_process`
- `fact_sales_targets`

A separate `_measures` table was also created to keep DAX measures organized.

---

## 🔗 Relationships

Relationships were created between the fact and dimension tables using the appropriate keys.

The model uses concepts such as:

- One-to-many relationships
- Primary and foreign keys
- Cardinality
- Cross-filter direction
- Active relationships
- Dimension-to-fact filtering

The goal was to create a model where dimensions such as **Date, Customer, Product, and Geography** could correctly filter the relevant fact tables.

---

## 📅 Date Modelling

A dedicated date table was created using:

```DAX
dim_date =
CALENDARAUTO()
