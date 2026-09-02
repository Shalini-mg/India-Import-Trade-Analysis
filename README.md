# India Import Trade Analysis

## Project Overview

This project analyzes India's import trade with Asian countries from 2015 to 2025 using Python. The analysis focuses on identifying major import partners, high-value commodities, yearly trade trends, regional patterns and variations in import values.

The project includes data exploration, cleaning, transformation, feature engineering, statistical analysis and data visualization.

---

## Project Objectives

- Identify major importing countries based on import value and trade activity.
- Identify major commodities contributing to India's imports.
- Analyze import trends from 2015 to 2025.
- Compare import activity across major countries and Asian trade subregions.
- Analyze the distribution and variation of import values using statistical measures.
- Identify significant trade patterns and generate data-driven insights.

---

## Dataset

- Source: India Data Portal
- Period: 2015–2025
- Region: Asian Countries
- Initial Records: 3,188,530
- Final Records After Cleaning: 3,188,475
- Original Columns: 15
- Final Columns After Feature Engineering: 21

Key variables include:

- Country
- Trade Region and Subregion
- Commodity
- HS Code
- Measurement Unit
- Import Quantity
- Import Value in Rupees
- Import Value in Dollars
- Date

---

## Tools and Technologies

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Google Colab
- GitHub

---

## Data Cleaning and Preparation

The dataset was prepared by:

- Examining missing values and duplicate records.
- Removing 55 records with missing measurement units.
- Standardizing country names such as Türkiye to Turkey.
- Converting date information into appropriate date format.
- Creating year and month features.
- Examining zero-value records.
- Selecting import value in rupees as the primary analytical variable.

The final cleaned dataset contained **3,188,475 records**.

---

## Statistical Analysis

Statistical analysis was performed on import value in rupees.

| Measure | Result |
|---|---:|
| Mean | ₹699.02 |
| Median | ₹18.42 |
| Mode | ₹0 |
| Variance | 207,986,172.44 |
| Standard Deviation | ₹14,421.73 |
| Skewness | 90.41 |
| Kurtosis | 11,190.26 |

The large difference between the mean and median shows that import values are highly positively skewed. A relatively small number of high-value transactions strongly influence the average import value.

---

## Key Analysis Performed

### Descriptive Analysis

The analysis examined dataset structure, missing values, unique categories, import-value statistics, countries, commodities, units and yearly trends.

### Diagnostic Analysis

Mean, median, skewness, extreme values, yearly changes and variations between major countries, commodities and subregions were investigated.

### Predictive Analysis

Predictive modelling was not included in the current project. Import forecasting can be considered as future work.

### Decision-Support Analysis

Observed patterns were converted into practical insights that can support trade monitoring and further analytical investigation.

---

## Key Findings

- India’s total import value increased from approximately **₹141.0M in 2015** to a peak of approximately **₹349.1M in 2022**.
- China emerged as the leading import source among the analyzed Asian countries.
- Petroleum-related commodities were among the largest contributors to import value.
- Petroleum oils contributed approximately **₹290.6M**, while petroleum crude contributed approximately **₹172.6M**.
- Import-value distribution was highly positively skewed with a skewness of approximately **90.41**.
- Import values showed substantial variation, with a standard deviation of approximately **₹14,421.73**.
- Import values declined after the 2022 peak.
- The unusually low import value observed in 2025 requires additional validation and investigation before drawing long-term conclusions.

---

## Visualizations

The project includes:

- Import Value Box Plot
- Log-Transformed Import Value Distribution
- Total Import Value by Year
- Top 10 Import Countries
- Top 10 Commodities
- Unit-wise Import Value
- Import Value by Asian Trade Subregion
- Yearly Import Trend of Top 5 Countries

---
Conclusion

The project demonstrates an end-to-end Python data analytics workflow using a large real-world international trade dataset.

The analysis identified major import partners, high-value commodities, yearly trade trends, statistical variation and regional trade patterns. It also demonstrates practical skills in data cleaning, exploratory data analysis, feature engineering, statistical analysis, visualization and business-oriented interpretation.

