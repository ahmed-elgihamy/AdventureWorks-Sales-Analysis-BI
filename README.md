
![image](https://github.com/user-attachments/assets/5e8e7397-ed7d-4dff-9f6e-ca467a3b9a38)

# 📊 AdventureWorks Sales Analysis

This Power BI project connects to the **AdventureWorks2022** dataset in **DirectQuery mode**, providing an in-depth analysis of sales performance, order trends, territories, products, and shipping methods. The dashboard supports decision-making through a clean star schema and actionable metrics.

---

## 🔗 Data Source

- **Database**: AdventureWorks2022  
- **Download Link**: [AdventureWorks2022.bak](https://github.com/Microsoft/sql-server-samples/releases/download/adventureworks/AdventureWorks2022.bak)  
- **Connection Mode**: DirectQuery

---

## 📥 Imported Tables

| Schema       | Table Name             |
|--------------|------------------------|
| Sales        | SalesOrderHeader       |
| Sales        | SalesOrderDetail       |
| Sales        | SalesTerritory         |
| Sales        | vSalesPerson           |
| Purchasing   | ShipMethod             |
| Production   | Product                |
| Production   | ProductSubcategory     |
| Production   | ProductCategory        |

---

## 🧩 Created Tables

- **Status Table** – Derived from the `ufnGetSalesOrderStatusText` function  
- **Date Table** – Created using Power Query or DAX for time-based analysis

---

## 🧹 Data Preparation

- Renamed tables and columns for better readability
- Removed unused columns to optimize performance
- Resolved data inconsistencies in:
  - `TotalDue`
  - `Freight`
  - `TaxAmt`
  - `SubTotal`

---

## 🌟 Star Schema Design

**Fact Table:**
- `SalesOrderDetail` (joined with `SalesOrderHeader`)

**Dimension Tables:**
- `Product` ➝ with subcategory and category hierarchy
- `ShipMethod`
- `SalesTerritory`
- `vSalesPerson`
- `Status`
- `Date`

---

## 📐 Measures

| Measure Name       | Description                       |
|--------------------|-----------------------------------|
| `No. Orders`       | Count of distinct orders          |
| `Total Subtotal`   | Sum of SubTotal values            |
| `Total Tax`        | Sum of TaxAmt values              |
| `Total Freight`    | Sum of Freight values             |
| `Total Due`        | Sum of TotalDue values            |
| `Total Quantity`   | Sum of OrderQty values            |

---

## 📌 Key Features

- Clean star schema for intuitive reporting
- Accurate and dynamic sales KPIs
- Detailed breakdown by product, territory, and salesperson
- Date-based filtering and time intelligence support
- Optimized for performance using DirectQuery

---

## 🛠️ Tools & Technologies

- **Power BI**
- **SQL Server**
- **DAX**
- **Power Query**
- **DirectQuery Mode**

---

## 📈 Dashboard Title

> **AdventureWorks Sales Analysis**

---
