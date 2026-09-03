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
### 📂 Dataset Access

The original dataset is not included in this repository because of its large file size.

**Dataset Link:**  
(https://drive.google.com/drive/folders/1ubNIe9UiA2nrQRK05bcI3WxPotdp2QEP?usp=drive_link)

---

## 🔄 Project Workflow

```text
Data Collection
      ↓
Data Import
      ↓
Data Understanding
      ↓
Exploratory Data Analysis
      ↓
Data Cleaning
      ↓
Data Transformation
      ↓
Feature Engineering
      ↓
Statistical Analysis
      ↓
Data Visualization
      ↓
Insights & Interpretation
      ↓
Decision Support
      ↓
Documentation

---
🔍 Exploratory Data Analysis

The dataset was initially explored to understand its structure and identify important data-quality issues.

The following checks were performed:

Dataset dimensions
Column names
Data types
Missing values
Duplicate records
Unique values
Country distribution
Commodity distribution
Measurement units
Date range
Import-value distribution
Descriptive statistics

The initial dataset contained 3,188,530 records and 15 columns.

A total of 55 records with missing measurement units were identified and removed because the measurement unit was required for meaningful trade analysis.

The final cleaned dataset contained 3,188,475 records.

---
🧹 Data Cleaning & Preprocessing

The following data-cleaning steps were performed:

Missing Values

Missing values were checked across the dataset.

The 55 records with missing unit values were removed.

Duplicate Records

Duplicate records were checked after loading and cleaning the dataset.

No duplicate records remained in the final cleaned dataset.

Country Name Standardization

Country names were reviewed and standardized where required.

For example:

Türkiye → Turkey
Date Transformation

The date column was converted into an appropriate date format.

Additional time-based features such as year and month were created for further analysis.

Quantity Handling

The value_qt column contains multiple measurement units.

Therefore, quantities across different units were not directly combined because values measured in Kgs, Nos, Sqm, etc. are not directly comparable.

The analysis therefore focuses primarily on value_rs, the import value in Indian Rupees.

---

⚙️ Feature Engineering

Additional features were created to support time-based and analytical comparisons.

The main engineered features include:

Year
Month
Additional helper columns used for statistical analysis and visualization

These features enabled yearly trend analysis and comparisons across countries, commodities, and trade subregions.
---

📈 Statistical Analysis

Statistical analysis was performed primarily on the value_rs variable.

Statistical Measure	Result
Mean	₹699.02
Median	₹18.42
Mode	₹0
Variance	207,986,172.44
Standard Deviation	₹14,421.73
Skewness	90.41
Kurtosis	11,190.26
Interpretation
The mean is much higher than the median, showing that a relatively small number of high-value records strongly influence the average.
The mode is ₹0, indicating that zero-value records occur frequently.
The high standard deviation indicates substantial variation in import values.
The very high positive skewness indicates a strong right-skewed distribution with a long upper tail.
The high kurtosis indicates the presence of extreme observations.

Extreme values were not automatically removed because they may represent genuine high-value trade transactions.
---

📊 Data Visualizations & Findings
1. Import Value Box Plot

The box plot was used to examine the spread, distribution, and extreme values of import value.

Interpretation

The box plot shows a highly right-skewed distribution with several extreme high-value observations. This indicates substantial variation in individual import transaction values.

2. Import Value Distribution – Log Transformation

A log transformation was applied for visualization to reduce the effect of extreme values and make the distribution easier to interpret.

Interpretation

The log-transformed distribution provides a clearer view of the concentration of lower and medium-value records while reducing the visual dominance of extremely high-value observations.

3. Total Import Value by Year

Yearly import values were calculated to understand changes in India's import activity over time.

Key Values
Year	Import Value
2015	₹141.00M
2016	₹139.96M
2017	₹167.28M
2018	₹210.20M
2019	₹206.21M
2020	₹168.80M
2021	₹255.07M
2022	₹349.15M
2023	₹325.77M
2024	₹262.10M
2025	₹3.30M
Interpretation

India's total import value generally increased from 2015 and reached its highest level in 2022 at approximately ₹349.15 million.

Import value declined during 2023 and 2024.

The unusually low recorded value for 2025 requires further validation and investigation before drawing long-term conclusions.

4. Top 10 Import Countries by Total Import Value

The top importing partner countries were identified based on their total import value.

Interpretation

India's import value is concentrated among a relatively small number of major Asian trading partners.

China is the leading major import source, followed by countries including the United Arab Emirates, Saudi Arabia, Iraq, Indonesia, Republic of Korea, Singapore, Hong Kong, Japan, and Qatar.

5. Top 10 Commodities by Total Import Value

The top commodities were ranked according to their total import value.

Key Findings

The highest-value commodity categories include:

Petroleum Oils and Oils Obtained from Bituminous Materials
Petroleum Crude
Other
Others
Non-Industrial Diamonds
Steam Coal
Liquefied Natural Gas
Other Non-Monetary Unwrought Forms of Gold
Monolithic Integrated Circuits – Digital
Crude Palm Oil and its Fractions
Interpretation

Import value is concentrated among a relatively small number of high-value commodities, particularly petroleum and energy-related products.

The categories "Other" and "Others" are source-level categories and should not be interpreted as specific commodity types.

6. Unit-wise Import Value

Import value was compared across the measurement units present in the dataset.

Interpretation

The chart shows that import value is concentrated across a few major measurement units, particularly Kgs and Nos.

This comparison represents trade value grouped by measurement unit rather than a direct comparison of physical quantities because the units measure different things.

7. Import Value by Trade Subregion

Import activity was compared across the major Asian trade subregions.

Interpretation

Import value varies considerably across Asian trade subregions, with some subregions contributing substantially more to India's total import value than others.

This indicates that India's import activity is geographically concentrated rather than evenly distributed across Asian subregions.

8. Yearly Import Value of Top 5 Import Countries

A multivariate analysis was performed to compare the yearly import-value trends of the five leading import countries.

Interpretation

China remained the strongest major import source across most of the period.

China's import value increased from approximately ₹39.22 million in 2015 to a peak of approximately ₹82.26 million in 2023, before declining to approximately ₹67.83 million in 2024.

The United Arab Emirates also showed strong import values, reaching approximately ₹38.43 million in 2024.

The five countries show an unusually sharp decline in recorded value in 2025, consistent with the overall yearly pattern. This should be investigated further.
---

💡 Key Insights
1. Import Value Increased Over Time

India's total import value increased from approximately ₹141.00 million in 2015 to approximately ₹349.15 million in 2022, the highest value observed during the period.

2. China is a Major Import Source

China consistently appears as the leading major import source in the analysis.

3. Petroleum Products Have High Import Value

Petroleum oils and petroleum crude are among the highest-value commodity categories, highlighting the importance of energy-related imports.

4. Import Values are Highly Skewed

The mean import value of approximately ₹699.02 is substantially higher than the median of ₹18.42, indicating that high-value transactions strongly influence the overall average.

5. Large Variation Exists Between Transactions

The standard deviation of approximately ₹14,421.73 indicates substantial variation in individual import values.

6. Trade is Geographically Concentrated

Import activity varies considerably across Asian trade subregions and is concentrated among major trading partners.

7. 2025 Requires Further Investigation

The recorded import value for 2025 is substantially lower than previous years despite a substantial number of trade records. This unusual pattern should be validated before using 2025 for long-term trend conclusions.
---


🧠 Types of Analysis Performed
Descriptive Analysis
Dataset structure and dimensions
Missing-value analysis
Duplicate checks
Unique-value analysis
Mean
Median
Mode
Variance
Standard deviation
Skewness
Kurtosis
Country analysis
Commodity analysis
Unit analysis
Yearly trend analysis
Diagnostic Analysis

The analysis was used to understand:

Why mean and median differ significantly
The effect of extreme import values
Major country contributions
Major commodity contributions
Yearly fluctuations
Differences across trade subregions
The unusual 2025 pattern
Differences between measurement units
Predictive Analysis

Predictive modelling was not performed in the current project.

Predictive modelling and forecasting can be considered as future enhancements.

Prescriptive Analysis

Formal optimization modelling was not performed.

However, the findings provide decision-support recommendations for monitoring major countries, commodities, trade trends, and unusual values.
---

🎯 Decision Support

The findings can support trade monitoring and business decision-making by helping stakeholders:

Monitor major import partners such as China and the UAE.
Track high-value commodity categories, particularly petroleum and energy-related products.
Monitor significant changes in yearly import values.
Investigate unusually high or low trade records.
Examine extreme observations before making business decisions.
Validate unusual periods such as 2025.
Focus trade analysis on major countries and commodities.
Identify geographically concentrated import activity.
---

⚠️ Limitations
The analysis is based on the available India Data Portal dataset.
Quantity values use different measurement units and therefore cannot be directly aggregated across all records.
value_dl represents the same trade value in another currency and was not the primary analytical variable.
Extreme values were retained because they may represent genuine transactions.
The categories "Other" and "Others" are source-level commodity categories.
The unusually low recorded value in 2025 requires further validation.
The project focuses on descriptive and diagnostic analytics rather than predictive modelling.
---



