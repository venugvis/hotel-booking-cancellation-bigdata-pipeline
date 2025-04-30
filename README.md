# Hotel Booking Cancellation Analysis

This project uses data analysis, machine learning, and visual storytelling to explore the patterns and predictors of hotel booking cancellations. It is designed as a complete end-to-end data analytics portfolio project.

## Problem Statement

Hotels face operational and financial challenges when customers cancel their bookings. This analysis aims to:
* Identify what factors influence cancellations.
* Develop a model that can predict cancellations before they occur.
* Communicate findings visually for stakeholders.

---

## Project Workflow

| Stage | Description |
|-------|-------------|
| **Data Cleaning** | PySpark was used to clean, transform, and export a large hotel booking dataset. |
| **SQL EDA**       | SQL queries helped analyze customer behaviour and trends (e.g., hotel type, market segment). |
| **Python EDA**    | Further pattern exploration using visualizations (Seaborn, Matplotlib). |
| **Modelling**      | Trained Logistic Regression, Random Forest, and Gradient Boosting to predict cancellations. |
| **Storytelling**  | Built a Tableau dashboard for business-friendly insights. |

---

## Exploratory Insights

Key findings:
* **City hotels** had a higher cancellation rate (~30%) than resort hotels (~23%).
* **Online travel agencies** had the highest cancellation rate among market segments.
* **Higher lead times** and **zero special requests** were strong cancellation signals.
* **Repeated guests** were far less likely to cancel than first-timers.
* **Non-refundable bookings** had an extremely high cancellation rate.

---

## Modelling Summary

| Model              | Accuracy | Precision (1) | Recall (1) | F1 Score (1) |
|-------------------|----------|----------------|-------------|--------------|
| Logistic Regression | 0.77     | 0.71           | 0.29        | 0.41         |
| Random Forest       | 0.80     | 0.70           | 0.49        | 0.58         |
| Gradient Boosting   | 0.80     | 0.71           | 0.47        | 0.56         |


**Random Forest** performed best in balancing accuracy and recall.

Top features by importance:
* `lead_time`
* `adr` (average daily rate)
* `arrival_date_day_of_month`
* `market_segment`

---

## Tableau Dashboard

The visual storytelling dashboard was built using Tableau Public:
> **[View Dashboard](https://public.tableau.com/app/profile/vishnu.venugopal2180/)**

---

## Dataset

> Source: [Hotel Booking Demand Dataset - Kaggle](https://www.kaggle.com/datasets/jessemostipak/hotel-booking-demand)

---

## Tools Used

* **PySpark** for big data cleaning
* **SQLite / pandasql** for SQL-based EDA
* **Pandas, Seaborn, Matplotlib** for visualization
* **Scikit-learn** for ML modeling
* **Tableau** for visual storytelling

---

## How to Reproduce

```bash
git clone https://github.com/venugvis/hotel-booking-cancellation-analysis.git
cd hotel-booking-cancellation-analysis
pip install -r requirements.txt
