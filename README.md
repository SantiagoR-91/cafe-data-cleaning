# cafe-data-cleaning
# ☕ Café Sales Data Cleaning – Python Project

This project is a hands-on exercise in cleaning and preparing transactional café sales data using Python and pandas. The dataset contains missing values, inconsistent totals, and a variety of data types.

## 📂 Dataset Overview

The raw dataset included:
- Null values in `unit_price`, `quantity`, and `total_spent`
- All fields stored as objects
- Inconsistent totals where `quantity × unit_price ≠ total_spent`

---

## 🛠️ Cleaning Steps

- Converted key columns to numeric types (`float`, `int`)
- Filled missing values using logical calculations:
  - Estimated `unit_price` from average per item
  - Back-calculated `total_spent` and `quantity` where possible
- Converted text fields (`Item`, `Payment Method`) to categorical types
- Parsed and converted `Transaction Date` to datetime
- Renamed columns for consistency and clarity (e.g., `Price Per Unit` → `unit_price`)
- Flagged 29 rows where calculated totals did not match original values

---

## 🧪 Data Integrity Handling

> ⚠️ `29` rows showed inconsistencies between `quantity × unit_price` and `total_spent`.  
> These were **not removed** to preserve data authenticity and reflect real-world conditions.  
> A new column `inconsistent_total` was added to flag them for transparency.

---

## 📁 Output

Cleaned data was exported to `cleaned_cafe_sales.csv`, ready for use in dashboards or BI tools.

---

## 🧰 Tools Used

- Python
- pandas
- PyCharm / Jupyter

---

## 📎 Why This Matters

This project highlights practical data wrangling skills and attention to data quality — key abilities for any data analyst working with real-world business data.

---
