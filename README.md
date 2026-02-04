 #  Data Quality & Trust Index Dashboard

## Dashboard Screenshot

![Image](https://github.com/user-attachments/assets/d8469c59-164b-4c23-a74e-4ecf46205c75)

![Image](https://github.com/user-attachments/assets/44b36c30-a84d-482f-a774-343a2925583d)



##  Project Overview

This project focuses on **measuring and quantifying data reliability** instead of assuming data is clean. Using Power BI and advanced DAX, I built a **Data Quality & Trust Index Dashboard** that evaluates business data across key quality dimensions and produces a single, executive-friendly **Trust Index score**.

The dashboard is designed to answer one critical question:

> **Can we trust this data for decision-making?**

---

##  Objectives

* Measure data quality in a structured, repeatable way
* Identify which quality dimensions degrade trust the most
* Provide an executive-level trust score supported by diagnostics
* Avoid aggressive data cleaning and instead *quantify* data issues

---

##  Dataset

**Source:** Online Retail II dataset (2010–2011)

**Why this dataset?**

* Contains real-world data quality issues
* Missing customer information
* Invalid quantities and prices
* Duplicate transaction patterns
* Ideal for demonstrating data trust measurement

---

##  Data Quality Dimensions

The Trust Index is built using four objectively measurable dimensions:

| Dimension        | Description                                                 |
| ---------------- | ----------------------------------------------------------- |
| **Completeness** | Missing critical fields such as Customer ID and Description |
| **Accuracy**     | Invalid values (Quantity ≤ 0, Price ≤ 0)                    |
| **Consistency**  | Logical validity of transactional records                   |
| **Uniqueness**   | Duplicate Invoice–Product combinations                      |

Each dimension is calculated independently and contributes to the final Trust Index.

---

##  Trust Index Logic (DAX)

The  **Data Trust Index** is a weighted score:

```DAX
Data Trust Index :=
[Completeness %] * 0.35 +
[Accuracy %] * 0.30 +
[Consistency %] * 0.20 +
[Uniqueness %] * 0.15
```


##  Dashboard Pages

###  Page 1 – Executive Trust Overview

* Displays the **Data Trust Index (0.90)** as a single KPI to indicate overall data reliability.
* Includes a **Trust Status indicator (High Trust)** for instant executive interpretation.
* **Dimension Summary bar chart** compares Completeness, Accuracy, Consistency, and Uniqueness to highlight relative strengths and weaknesses.

###  Page 2 – Data Quality & Issue Breakdown

* Shows total counts of **Duplicate, Inaccurate, Incomplete, and Inconsistent records**.
* Issue-level bar chart highlights **Incomplete Records (missing Customer IDs)** as the primary contributor to data quality risk.
* Enables stakeholders to move from high-level trust metrics to specific data quality problem areas.

---

##  Modeling & Design Decisions

* Minimal cleaning in Power Query (only structural hygiene)
* Data quality issues are **flagged, not fixed**
* All quality metrics are calculated using **DAX measures**
* Disconnected tables used for flexible, scalable visuals

---

##  Key Insight

> "Data trust should be measured, not assumed. This dashboard quantifies reliability before decisions are made."

---

##  Tools & Technologies

* Power BI
* DAX (CALCULATE, SWITCH, VAR, context-aware measures)
* Power Query (light preprocessing)

---

##  Use Cases

* Data governance monitoring
* Pre-report data validation
* Executive decision support
* BI quality assurance

 
---

## 👤 Author

**Prathiba**
Aspiring Data Analyst | Power BI | SQL | DAX

---

 
