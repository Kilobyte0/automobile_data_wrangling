#  Automobile Data Cleaning and Preprocessing Project

## Overview

This project demonstrates a complete data cleaning and preprocessing workflow using the Automobile Dataset from the UCI Machine Learning Repository. The goal was to transform raw data containing missing values and categorical features into a clean, structured dataset ready for exploratory data analysis (EDA), visualization, and machine learning applications.

Data preprocessing is a critical step in any analytics project because the quality of insights and predictive models depends heavily on the quality of the underlying data. This project focuses on identifying data quality issues, handling missing values, engineering new features, and encoding categorical variables.

---

## Dataset Information

**Dataset:** Automobile Dataset

**Source:** UCI Machine Learning Repository. You can find it [here.](https://archive.ics.uci.edu/ml/machine-learning-databases/autos/imports-85.data)

The dataset contains information about various automobile characteristics, including:

* Vehicle make
* Fuel type
* Body style
* Engine specifications
* Fuel efficiency
* Horsepower
* Vehicle price

---

## Project Objectives

* Load and inspect the raw dataset.
* Assign meaningful column names.
* Identify missing values and data quality issues.
* Replace invalid entries with appropriate missing-value indicators.
* Handle missing numerical and categorical data.
* Perform feature engineering.
* Convert categorical variables into machine-learning-friendly formats.
* Export a clean dataset for future analysis.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Jupyter Notebook

---

## Data Cleaning Process

### 1. Data Inspection

The dataset was loaded into a Pandas DataFrame and inspected using:

* `.head()`
* `.shape()`
* `.isnull().sum()`

This helped identify the overall structure and missing values within the dataset.

### 2. Missing Value Handling

The dataset contained missing values represented by the symbol `?`.

These values were converted to `NaN` to allow proper handling with Pandas.

Missing numerical values were replaced using mean imputation for:

* normalized_losses
* bore
* stroke
* horsepower
* peak_rpm

Missing categorical values were replaced using mode imputation for:

* num_doors

Rows containing missing values in the price column were removed because price serves as the target variable for future analyses.

---

## Feature Engineering

### Fuel Consumption Conversion

A new feature was created by converting fuel efficiency from Miles Per Gallon (MPG) to Liters per 100 Kilometers (L/100km).

This provides a more internationally recognized measurement of fuel consumption.

---

## Categorical Encoding

To prepare the dataset for machine learning, categorical variables were transformed into dummy variables using one-hot encoding.

Encoded features include:

### Fuel Type

* fuel-type-gas
* fuel-type-diesel

### Aspiration

* aspiration-std
* aspiration-turbo

---

## Final Output

The cleaned dataset was exported as:

```python
clean_df.csv
```

This dataset is ready for:

* Exploratory Data Analysis (EDA)
* Data Visualization
* Statistical Analysis
* Machine Learning
* Predictive Modeling

---

## Key Learnings

Through this project, I gained hands-on experience in:

* Data cleaning techniques
* Missing value treatment
* Mean and mode imputation
* Feature engineering
* One-hot encoding
* Data preparation for machine learning
* Working with real-world datasets in Python

---

## Future Improvements

* Perform exploratory data analysis (EDA).
* Build regression models to predict vehicle prices.
* Analyze feature importance.
* Develop interactive dashboards and visualizations.
* Compare different data preprocessing techniques.

---

## Author

[Muhydeen Abdulrazaq](www.linkedin.com/in/muhydeen-abdulrazaq-5071ba235)

Data Analyst | SQL | Python | Data Visualization | Business Intelligence

This project is part of my data analytics learning journey and showcases practical skills in data preprocessing and feature engineering.
