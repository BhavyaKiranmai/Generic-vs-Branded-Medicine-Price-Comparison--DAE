
# Generic vs Branded Medicine Price Comparison

## DAE Cornerstone Project – Data Analysis Essentials

---

## 1. Project Overview

The **Generic vs Branded Medicine Price Comparison** project is a Data Analysis Essentials (DAE) Cornerstone Project developed using Python and pharmaceutical product data.

The main objective of this project is to analyze pharmaceutical products, identify **potential generic-name medicines** using a project-defined name-to-ingredient matching method, and compare their listed prices with other medicines having comparable characteristics.

Medicines are considered comparable in this project based on:

- Primary Ingredient
- Strength
- Dosage Form

The project follows an eight-stage data analysis pipeline:

1. Data Loading & Reading
2. Data Acquisition & Filtering
3. Data Extraction
4. Data Validation & Cleaning
5. Data Aggregation & Representation
6. Data Analysis
7. Data Visualization
8. Results & Interpretation

> **Important:** "Potential Generic" and "Potential Branded" are project-defined analytical categories. They are not official regulatory classifications.

---

# 2. Problem Statement

Medicines having the same active ingredient, strength, and dosage form may have different listed prices.

Pharmaceutical datasets can contain:

- Missing values
- Invalid prices
- Duplicate records
- Inconsistent medicine names
- Different manufacturer formats
- Missing strength information
- Incomplete product information

These issues can make direct medicine price comparison difficult.

This project develops a structured data analysis pipeline to clean and validate pharmaceutical product data, create comparable medicine groups, identify potential generic-name medicines, and compare their listed prices with other medicines in the same comparison groups.

The project aims to identify and quantify observed price differences between potential generic-name medicines and other comparable medicines.

---

# 3. Objectives

The main objectives of this project are:

- To load and inspect the pharmaceutical product dataset.
- To understand the structure and attributes of the dataset.
- To identify the fields required for medicine comparison.
- To handle missing and invalid values.
- To filter invalid and non-positive medicine prices.
- To check duplicate product records.
- To clean and standardize medicine-related text fields.
- To create comparison-related features.
- To group medicines according to primary ingredient, strength, and dosage form.
- To identify potential generic-name medicines using a project-defined matching method.
- To compare potential generic-name medicine prices with other medicines in the same comparison group.
- To calculate price differences.
- To calculate percentage price differences.
- To perform grouping, sorting, aggregation, and filtering using Pandas.
- To visualize the analysis results.
- To interpret the findings.
- To document project limitations and future scope.

---

# 4. Scope of the Project

The project focuses on pharmaceutical product data available in the selected dataset.

The analysis uses attributes such as:

- Product ID
- Medicine Name
- Manufacturer
- Price
- Primary Ingredient
- Primary Strength
- Dosage Form
- Pack Size
- Pack Unit
- Number of Active Ingredients
- Active Ingredients
- Therapeutic Class
- Packaging Information

The project creates comparable medicine groups using:

**Primary Ingredient + Strength + Dosage Form**

Potential generic-name medicines are then identified using a project-defined medicine-name and ingredient matching method.

The price of a potential generic-name medicine is compared with the average price of other products in the same comparison group.

---

# 5. Significance of the Project

This project demonstrates how data analysis techniques can be applied to pharmaceutical product data.

It provides a structured workflow for:

- Data loading
- Data inspection
- Data cleaning
- Data validation
- Feature extraction
- Data transformation
- Grouping
- Aggregation
- Price comparison
- Statistical analysis
- Data visualization
- Result interpretation

The project demonstrates the practical application of Python-based data analysis techniques to a real-world dataset.

---

# 6. Dataset Information

## Dataset Name

**Indian Pharmaceutical Products Dataset**

## Dataset Source

The dataset is based on the Indian Pharmaceutical Products Dataset available on Kaggle.

Dataset source:

https://www.kaggle.com/datasets/rishgeeky/indian-pharmaceutical-products

## Dataset Format

The dataset is provided in CSV format.
The dataset contains information about pharmaceutical products including medicine names, manufacturers, prices, dosage forms, primary ingredients, strengths, active ingredients, therapeutic classes, and packaging information.

## Initial Dataset Size

The dataset used at the beginning of the Review-2 pipeline contains:

- **Records:** 253,973
- **Columns:** 15

## Initial Dataset Columns

```text
product_id
brand_name
manufacturer
price_inr
is_discontinued
dosage_form
pack_size
pack_unit
num_active_ingredients
primary_ingredient
primary_strength
active_ingredients
therapeutic_class
packaging_raw
manufacturer_raw

8. Data Loading & Inspection

The pharmaceutical dataset was loaded into Python using the Pandas library.

The dataset was read using pd.read_csv() and inspected before performing any processing.

The initial dataset used in the Review-2 pipeline contained:

253,973 records
15 columns

The following inspection operations were performed:

Checking the dataset shape
Viewing the first few records
Checking column names
Checking data types
Checking missing values
Examining unique values
Understanding the structure of the dataset

The inspection helped identify the important attributes required for further processing and analysis.
