# Vendor Performance Analysis for Supply Chain Optimization

## Project Overview

This project focuses on evaluating supplier performance using procurement, sales, profitability, and operational data to identify high-performing vendors, assess supply chain risk, and support data-driven sourcing decisions.

Vendor performance directly impacts inventory availability, procurement costs, customer service levels, and overall supply chain efficiency. The objective of this project was to develop a structured analytical framework capable of measuring supplier effectiveness and identifying opportunities for procurement optimization.

The project combines data ingestion, exploratory data analysis, KPI evaluation, profitability analysis, and supplier performance assessment to generate actionable supply chain insights.

---

## Project Files

| File                              | Objective                                                          |
| --------------------------------- | ------------------------------------------------------------------ |
| EDA.ipynb                         | Exploratory analysis of vendor, sales, and operational performance |
| Vendor Performance Analysis.ipynb | Supplier KPI evaluation and business insights                      |
| ingestion_db.py                   | Automated CSV ingestion pipeline into SQLite database              |

---

## View Notebooks

### Exploratory Data Analysis

📓 [View Notebook](https://nbviewer.org/github/chandran1994/Python-Vendor-Performance-Analysis-Project/blob/main/EDA.ipynb)

### Vendor Performance Analysis

📓 [View Notebook](https://nbviewer.org/github/chandran1994/Python-Vendor-Performance-Analysis-Project/blob/main/Vendor%20Performance%20Analysis.ipynb)

---

## Data Engineering Component

The project includes an automated ingestion pipeline that loads raw CSV files into a SQLite database for analytical processing.

The ingestion process:

```text
CSV Files
    ↓
Data Validation
    ↓
SQLite Database
    ↓
Analytical Processing
```

The ingestion script automatically scans source files and loads them into database tables for downstream analysis.

### Ingestion Workflow

```python
for file in os.listdir('data'):
    df = pd.read_csv('data/'+file)
    ingest_db(df, file[:-4], engine)
```

This creates a reproducible analytical workflow and reduces manual data loading effort.

---

# Analytical Workflow

```text
Vendor Transaction Data
            ↓
Data Cleaning
            ↓
Data Ingestion
            ↓
Exploratory Data Analysis
            ↓
Vendor KPI Analysis
            ↓
Profitability Evaluation
            ↓
Risk Assessment
            ↓
Procurement Recommendations
```

---

## Data Preparation

The project began with data cleaning and preprocessing to ensure reliable supplier performance evaluation.

Key preprocessing activities included:

* Missing value treatment
* Duplicate removal
* Vendor-level aggregation
* KPI calculations
* Profitability analysis
* Data validation
* Feature engineering

The resulting dataset provided a consolidated supplier performance view for analysis.

---

## Vendor Sales Performance Analysis

The first stage focused on evaluating supplier contribution to overall sales performance.

### Analysis Performed

```python
Total Sales by Vendor

Revenue Contribution Analysis

Vendor Ranking

Top Supplier Identification
```

The analysis quantified each vendor's contribution to business revenue and highlighted suppliers that play a critical role in maintaining sales performance.

---

## Vendor Profitability Analysis

Sales volume alone does not provide a complete picture of supplier effectiveness.

To address this, profitability metrics were evaluated across vendors.

### Analysis Performed

```python
Profit by Vendor

Margin Analysis

Profit Distribution

Vendor Profit Ranking
```

This analysis identified vendors that generated strong margins and revealed situations where high sales volume did not necessarily translate into high profitability.

---

## Product Category Analysis

Supplier performance was further evaluated across product categories to understand vendor specialization and dependency risks.

### Analysis Performed

```python
Category-Level Sales

Category-Level Profitability

Vendor Category Contribution

Demand Concentration Analysis
```

The analysis highlighted suppliers dominating key product categories and identified areas where excessive supplier concentration may create supply chain risk.

---

## Regional Performance Analysis

Geographic supplier performance was examined to understand sourcing effectiveness across regions.

### Analysis Performed

```python
Regional Sales Analysis

Regional Profitability

Geographic Supplier Comparison

Regional Vendor Ranking
```

This provided insight into sourcing strengths and regional supplier performance differences.

---

## Operational Performance Analysis

Operational KPIs were analyzed to evaluate supplier consistency and reliability.

### Analysis Performed

```python
Order Fulfillment Analysis

Delivery Performance Metrics

Operational KPI Evaluation

Vendor Reliability Assessment
```

Operational performance indicators help identify suppliers capable of supporting stable inventory availability and service-level requirements.

---

## Vendor Performance Framework

The project evaluated suppliers using multiple performance dimensions rather than relying on a single metric.

```text
Vendor Performance
        ├── Sales Contribution
        ├── Profitability
        ├── Product Coverage
        ├── Regional Performance
        └── Operational Reliability
```

This framework provides a more balanced approach to supplier evaluation and procurement decision-making.

---

## Key Supply Chain Insights

The analysis identified:

* Strategic revenue-generating suppliers
* High-margin vendors
* Operationally reliable suppliers
* Supplier concentration risks
* Regional sourcing opportunities
* Vendors requiring performance improvement

These findings support a more proactive supplier management strategy.

---

## Business Recommendations

### Strategic Supplier Management

```text
High Sales
      +
High Profitability
      +
Operational Reliability
      ↓
Strategic Supplier
```

Strengthen relationships with suppliers demonstrating consistent performance across multiple KPIs.

### Supplier Risk Reduction

Reduce dependency on vendors controlling large portions of critical product categories.

### Procurement Optimization

Use profitability and operational metrics alongside purchase cost when evaluating supplier performance.

### Vendor Scorecards

Develop supplier performance scorecards tracking:

* Revenue contribution
* Profitability
* Fulfillment performance
* Operational reliability
* Category importance

### Regional Sourcing Optimization

Allocate procurement volume toward regions demonstrating stronger supplier performance and operational consistency.

---

## Business Value

This project demonstrates how analytics can improve supplier visibility and procurement decision-making.
