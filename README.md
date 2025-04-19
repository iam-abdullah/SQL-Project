

# 📊 COVID-19 Data Exploration using SQL

This project explores global COVID-19 data using SQL, focusing on key metrics such as infection rates, death percentages, vaccination progress, and continent-level analysis. The data is queried from two CSV-based tables: `CovidDeaths_csv` and `CovidVaccinations_csv`.

---

## 📁 Dataset Tables

- **CovidDeaths_csv**
  - Columns: `location`, `continent`, `date`, `population`, `total_cases`, `new_cases`, `total_deaths`, `new_deaths`, etc.

- **CovidVaccinations_csv**
  - Columns: `location`, `date`, `new_vaccinations`, etc.

---

## 🔍 SQL Analysis Overview

### 1. **Initial Exploration**
- Filtered out rows with null continents.
- Ordered data for better visibility.

### 2. **Cases vs Deaths**
- Calculated death percentage = `(total_deaths / total_cases) * 100`
- Focused on India for a location-specific view.

### 3. **Cases vs Population**
- Calculated infection percentage = `(total_cases / population) * 100`
- Identified highly impacted countries.

### 4. **Infection Rates**
- Found countries with the highest infection rate based on population.

### 5. **Death Counts**
- Aggregated total death counts per country and continent.

### 6. **Global Metrics**
- Calculated global totals and overall death percentage.

### 7. **Vaccination Progress**
- Used SQL window functions to compute rolling vaccinations.
- Compared vaccinated people vs total population using:
  - **CTE (Common Table Expression)**
  - **Temp Table**

---

## 🧮 SQL Concepts Used
- `GROUP BY`, `ORDER BY`
- `JOIN` (on date and location)
- `WINDOW FUNCTIONS` (`SUM() OVER`)
- `CTEs`
- `Temp Tables`
- `CAST` and `CONVERT`
- Mathematical expressions and aliasing

---

## 🚀 How to Use

1. Make sure you have access to a SQL environment (e.g., SQL Server, PostgreSQL, MySQL).
2. Load the CSVs into respective tables: `CovidDeaths_csv`, `CovidVaccinations_csv`.
3. Run the SQL queries in sequence or selectively explore the area of interest.
4. Optional: Visualize the results using BI tools like Power BI, Tableau, or Python.

---

## 📌 Notes

- The data assumes `continent` and `location` are clean and consistently available.
- Integer conversion (`CAST` or `CONVERT`) is used for aggregating certain fields like deaths and vaccinations.
- This project is aimed at understanding trends, patterns, and insights from COVID-19 data at a global and national level.

---



---

## 👨‍💻 Author

Created by **Md Abdullah**  
Feel free to contribute or fork for enhancement!

