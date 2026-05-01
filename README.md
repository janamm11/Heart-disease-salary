# 1.Heart Disease Analysis (EDA)

## Project Overview

This project performs Exploratory Data Analysis on the **Heart Failure Clinical Records** dataset. The goal is to understand the data, clean it, and explore relationships between medical features and patient survival (death_event).

## Dataset

- **File**: `heart.csv`
- **Initial Shape**: Checked at the beginning
- **Target Variable**: `death_event` (and `death_event_s`)

## Data Cleaning & Preprocessing

- Converted all column names to lowercase
- Checked and removed duplicate rows
- Handled missing values:
  - Analyzed missing values per column and per row
  - Dropped rows containing any missing values
- Fixed data types:
  - Converted binary columns to boolean
  - Converted `sex` to category then mapped to 0/1
  - Converted `age` to integer
  - Cleaned and standardized `death_event_s` column ("aliv" → "alive")
- Removed inconsistent string values

## Exploratory Analysis

### Univariate & Multivariate Analysis
- Visualized missing values (stacked bar plot)
- Pairplot for numerical features
- Histogram of `age` grouped by survival status
- Scatter plot with regression line between `serum_creatinine` and `serum_sodium`
- Violin plot to check smoking behavior by gender and survival
- Boxplots to compare `serum_creatinine` and `ejection_fraction` between survived and deceased patients

### Correlation Analysis
- Correlation heatmap among numerical features

## Key Observations

- Dataset was reduced after removing duplicates and rows with missing values
- 7 out of 13 columns are boolean type
- Two columns (`death_event` and `death_event_s`) contain the same information in different formats
- Most patients have low percentage of missing values; few rows had very high missingness
- Smoking appears to be a weak predictor in this dataset
- Clear differences observed in `serum_creatinine` and `ejection_fraction` between survived and deceased patients

## Potential Questions for Further Analysis

1. Which risk factors best predict whether a patient will survive or die?
2. Do males exhibit riskier health behaviors compared to females?
3. Does age influence risky health behaviors such as smoking?

## Technologies Used
- Python
- Pandas
- NumPy
- Seaborn
- Matplotlib

---

**Project Purpose**:  
Practice of data cleaning, type conversion, handling inconsistencies, and visual EDA on a medical dataset.

Part of EDA Portfolio.



# 2.Data Science Salaries Analysis (2020-2022)

## Project Overview

This project analyzes the **Data Science Job Salaries** dataset to understand salary trends, factors affecting pay, and differences across job titles, experience levels, company sizes, and locations.

## Dataset
- **File**: `ds_salaries.csv`
- **Target Variable**: `salary_in_usd`

## Data Cleaning & Preprocessing
- Removed unnecessary columns (`Unnamed: 0`, `salary`, `salary_currency`)
- Mapped abbreviated values to meaningful labels:
  - Experience Level: EN → Entry Level, MI → Mid Level, SE → Senior, EX → Executive
  - Employment Type: PT → Part-time, FT → Full-time, CT → Contract, FL → Freelance
  - Remote Ratio: 0 → No Remote, 50 → Partially Remote, 100 → Fully Remote
  - Company Size: S → Small, M → Medium, L → Large
- Removed duplicate records
- Checked for missing values

## Univariate Analysis
- Statistical summary of `salary_in_usd`
- Boxplot to detect outliers (salaries above $300,000 considered outliers)
- Count plots for:
  - Experience Level
  - Remote Ratio
  - Company Size
  - Company Location

## Multivariate Analysis & Key Insights
- **Highest Paying Job Titles**: Principal Data Engineer, Principal Data Scientist, Data Architect, Analytics Engineer, and Director of Data Science earn the highest average salaries.
- **Experience Level vs Salary**: Executive level has the highest average salary.
- **Company Size vs Salary**: Employees in Large companies earn higher average salary compared to Medium and Small companies.
- **Employment Type vs Salary**: Contract-based employees appear to earn more than Full-time employees (may be influenced by outliers).
- **Highest Paying Countries**: Russia and US are the top two highest paying countries for data science roles.
- **Salary in US**: Highest paying job titles within the United States were analyzed.
- **Senior & Executive Level Jobs**: Average salary for different job titles at Senior and Executive levels were explored.

### Salary Trends Over Years (2020–2022)
- Overall salary in data science roles has increased over the years.
- **Medium Size Companies**: Paid less in 2021 compared to 2020.
- **Large Size Companies**: Salary trend analyzed over the years.
- **Small Size Companies**: Salary trend analyzed over the years.

## Technologies Used
- Python
- Pandas
- Matplotlib
- Seaborn


**Project Purpose**:  
Exploratory Data Analysis on Data Science Salaries to understand key factors influencing compensation.

Part of EDA Portfolio.
