
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

- ## 7. Important Dataset Attributes

The dataset contains information about pharmaceutical products available in the Indian pharmaceutical market.

### Important Attributes

| Attribute | Description |
|---|---|
| `product_id` | Unique identifier of the medicine product |
| `brand_name` | Name of the medicine/product |
| `manufacturer` | Manufacturer or pharmaceutical company |
| `price_inr` | Listed price of the medicine in Indian Rupees |
| `is_discontinued` | Indicates whether the product is discontinued |
| `dosage_form` | Form of the medicine, such as tablet, capsule, syrup, etc. |
| `pack_size` | Quantity or size of the medicine pack |
| `pack_unit` | Unit associated with the pack size |
| `num_active_ingredients` | Number of active ingredients associated with the product |
| `primary_ingredient` | Main or primary ingredient of the medicine |
| `primary_strength` | Strength of the primary ingredient |
| `active_ingredients` | Active ingredients present in the product |
| `therapeutic_class` | Therapeutic category of the medicine |
| `packaging_raw` | Original packaging information |
| `manufacturer_raw` | Original manufacturer information |

### Main Attributes Used for Comparison

The major attributes used in the medicine comparison are:

- `brand_name`
- `price_inr`
- `primary_ingredient`
- `primary_strength`
- `dosage_form`
- `manufacturer`

---

## 8. Data Loading & Inspection

The pharmaceutical dataset was loaded into Python using the **Pandas** library.

The dataset was read using `pd.read_csv()` and inspected before performing further processing.

### Initial Dataset Information

- **Records:** 253,973
- **Columns:** 15

### Inspection Performed

The following operations were performed to understand the dataset:

- Checking the dataset shape
- Viewing the first few records
- Checking column names
- Checking data types
- Checking missing values
- Examining unique values
- Understanding the overall dataset structure

The inspection helped identify the important attributes required for further processing and analysis.

---

## 9. Data Acquisition & Filtering

The dataset used for this project is the **Indian Pharmaceutical Products Dataset**.

The dataset was acquired from Kaggle and processed in the project environment.

### Dataset Source

**Indian Pharmaceutical Products Dataset – Kaggle**

### Filtering Performed

The dataset was filtered to retain records useful for medicine price comparison.

The main filtering criteria included:

- Valid medicine product records
- Valid price information
- Relevant ingredient information
- Relevant strength information
- Relevant dosage-form information

Records with invalid or zero prices were removed because they cannot be used for meaningful price comparison.

After filtering invalid price records, the dataset contained **253,969 records**.

---

## 10. Data Extraction

Data extraction was performed to select the attributes required for further analysis.

The following important attributes were extracted:

- Product ID
- Medicine/brand name
- Manufacturer
- Price
- Dosage form
- Pack size
- Pack unit
- Number of active ingredients
- Primary ingredient
- Primary strength
- Active ingredients
- Therapeutic class

Selecting relevant attributes reduced the complexity of the dataset and made the subsequent validation, transformation and analysis easier.

---

## 11. Data Validation & Cleaning

Data validation was performed to check whether the dataset was suitable for further analysis.

The following validation checks were performed:

- Checking missing values
- Checking duplicate Product IDs
- Checking invalid prices
- Checking unknown or missing strengths
- Checking important ingredient information
- Checking dosage-form consistency
- Checking the structure of comparison groups

### Final Comparison-Ready Dataset

After validation and cleaning, the comparison-ready dataset contained:

- **225,731 records**
- **18 columns**
- **4,344 comparison groups**
- **0 missing prices**
- **0 unknown strengths**
- **0 duplicate Product IDs**

These validation checks helped ensure that the data used for analysis was consistent with the project requirements.

---

## 12. Missing-Value Handling

Missing values were identified using Pandas operations such as `isnull()` and `sum()`.

Missing values were observed in fields such as:

- `pack_size`
- `pack_unit`
- `primary_strength`

The project did not blindly remove all rows containing missing values because some missing fields were not essential for the main price-comparison analysis.

Where possible, missing pack-size information was recovered from the available packaging information.

For the final comparison analysis, important fields such as:

- Price
- Primary ingredient
- Primary strength
- Dosage form

were validated so that reliable comparison groups could be created.

The final comparison-ready dataset contained **0 missing prices**.

---

## 13. Duplicate Validation

Duplicate validation was performed to ensure that the same product was not unintentionally represented multiple times.

The `product_id` field was used as the main identifier for checking duplicate products.

### Duplicate Checks

The following checks were performed:

- Identification of duplicate Product IDs
- Counting duplicate records
- Validating Product ID uniqueness after cleaning

The final comparison-ready dataset contained:

**0 duplicate Product IDs**

This helped ensure that products were represented correctly during the analysis.

---

## 14. Data Cleaning and Filtering

Data cleaning was performed before creating comparison groups.

The main cleaning and filtering operations included:

1. Removing records with invalid or zero prices.
2. Standardizing medicine names.
3. Standardizing manufacturer names.
4. Standardizing primary ingredient values.
5. Standardizing strength values.
6. Standardizing dosage-form values.
7. Checking duplicate Product IDs.
8. Handling unsuitable records.
9. Validating important fields required for comparison.

The purpose of data cleaning was to make similar medicine records consistent so that they could be compared correctly.

---

## 15. Data Transformation

Data transformation was performed to convert raw values into standardized forms suitable for analysis.

The following standardized fields were created:

- `medicine_name_key`
- `manufacturer_key`
- `ingredient_key`
- `strength_key`
- `dosage_form_key`

These standardized fields helped reduce inconsistencies caused by:

- Different capitalization
- Extra spaces
- Text formatting
- Different representations of similar information

The transformed values were then used for comparison-group creation and further analysis.

---

## 16. Feature Engineering

Feature engineering was used to create additional analytical attributes from the existing dataset.

The project created derived features to support medicine comparison.

### Important Engineered Features

- Cleaned medicine-name representation
- Cleaned ingredient representation
- Cleaned strength representation
- Cleaned dosage-form representation
- `comparison_group`
- `medicine_type`
- Price difference
- Percentage price difference

These features were created during the project to support classification, grouping and price analysis.

---

## 17. Comparison Group Creation

A comparison group was created to identify medicines with comparable characteristics.

The project defines a comparison group using:

**Primary Ingredient + Primary Strength + Dosage Form**

The standardized values were combined to create the `comparison_group`.

### Comparison Group Structure

The comparison group is conceptually created as:

`ingredient_key + strength_key + dosage_form_key`

### Example

`amoxycillin|500mg|tablet`

represents medicines having:

- **Primary ingredient:** Amoxycillin
- **Strength:** 500 mg
- **Dosage form:** Tablet

This grouping allows the project to compare products with the same primary ingredient, strength and dosage form instead of comparing unrelated medicines.

---

## 18. Data Aggregation & Representation

After creating comparison groups, the data was aggregated to understand price variation within each group.

The following statistics were calculated:

- Number of products
- Minimum price
- Maximum price
- Average price

### Aggregated Representation

| Comparison Group | Product Count | Minimum Price | Maximum Price | Average Price |
|---|---:|---:|---:|---:|
| Comparison Group | Calculated | Calculated | Calculated | Calculated |

The aggregated representation provides a summary of the products belonging to each comparison group.

This helps identify differences in listed prices among comparable medicine products.

---

## 19. Pandas Operations

Pandas was extensively used for data loading, cleaning, transformation, grouping and analysis.

### Main Pandas Operations Used

| Operation | Purpose |
|---|---|
| `pd.read_csv()` | Load the dataset |
| `df.head()` | View the first records |
| `df.info()` | Inspect data types and structure |
| `df.shape` | Check number of rows and columns |
| `df.columns` | View column names |
| `df.isnull().sum()` | Check missing values |
| `df.duplicated()` | Check duplicate records |
| `value_counts()` | Count categorical values |
| `sort_values()` | Sort records |
| `groupby()` | Group records for aggregation |
| Boolean filtering | Filter required records |
| Column assignment | Create derived columns |

These operations form the main data-processing workflow of the project.

---

## 20. Grouping, Sorting, Aggregation & Filtering

Grouping was used to organize medicines according to their comparison groups.

The project used grouping operations to calculate:

- Product count
- Minimum price
- Maximum price
- Average price

### Sorting

Sorting was used to identify:

- Highest price differences
- Lowest price differences
- Highest percentage differences
- Lowest percentage differences

### Filtering

Filtering was used to separate:

- Potential Generic candidates
- Potential Branded products
- Products with lower prices
- Products with higher prices
- Products with approximately equal prices

### Aggregation

Aggregation was used to summarize prices within each comparison group.

These operations helped convert the raw pharmaceutical dataset into meaningful analytical results.

---

## 21. Potential Generic-Name Identification

The dataset does not contain an official generic/branded classification field.

Therefore, the project uses a **project-defined analytical method** to identify **Potential Generic** medicine candidates.

### Identification Method

The medicine name is cleaned by:

- Converting the name to lowercase
- Removing strength values and units
- Removing common dosage-form words
- Removing unnecessary spaces

The cleaned medicine name is then compared with the cleaned `primary_ingredient`.

If the cleaned medicine name matches the primary ingredient, the product is classified as:

**Potential Generic**

Otherwise, it is classified as:

**Potential Branded**

### Classification Principle

The classification is based on the relationship between:

**Medicine Name ↔ Primary Ingredient**

It is **not** based solely on:

- Manufacturer
- Price

### Important Note

The terms **Potential Generic** and **Potential Branded** are **project-defined analytical categories**.

They should not be interpreted as official regulatory classifications of medicines.

The categories are used only for the purpose of this project's data analysis and price comparison.

---

## 22. Statistical Analysis

Statistical analysis was performed to understand price differences among comparable medicines.

The analysis considered:

- Number of Potential Generic candidates
- Number of Potential Branded products
- Number of comparison groups
- Minimum price
- Maximum price
- Average price
- Price difference
- Percentage price difference

The analysis also identified:

- Potential Generic candidates priced below the comparison average
- Potential Generic candidates priced above the comparison average
- Cases where prices were approximately equal

This analysis helps identify the extent of price variation among products with comparable characteristics.

---

## 23. Price Comparison Method

The price comparison was performed after identifying Potential Generic candidates and their corresponding comparison groups.

For each **Potential Generic** candidate:

1. Its `comparison_group` was identified.
2. Other products belonging to the same comparison group were identified.
3. The candidate itself was excluded from the comparison set.
4. The average listed price of the other products was calculated.
5. The candidate's listed price was compared with this average.

### Comparison Criteria

The products being compared have the same:

- Primary ingredient
- Primary strength
- Dosage form

The project uses the **average listed price of other products in the same comparison group** as the reference price.

---

## 24. Price Difference

The price difference is calculated using:

**Price Difference = Average Price of Other Products − Potential Generic Price**

### Interpretation

If:

**Price Difference > 0**

the Potential Generic candidate has a lower listed price than the average price of the other products in the same comparison group.

If:

**Price Difference < 0**

the Potential Generic candidate has a higher listed price than the comparison average.

If the difference is approximately zero, the prices are approximately equal.

Therefore, the project does not automatically treat every price difference as a saving.

---

## 25. Percentage Price Difference

The percentage price difference is calculated using the average price of other products as the reference.

### Formula

**Percentage Price Difference = ((Average Other Price − Candidate Price) / Average Other Price) × 100**

### Example

Suppose:

- Average price of other products = ₹100
- Potential Generic price = ₹70

Then:

**Price Difference = ₹100 − ₹70 = ₹30**

**Percentage Price Difference = (₹30 / ₹100) × 100 = 30%**

Therefore, the Potential Generic candidate's listed price is **30% lower than the comparison average**.

### Interpretation

- **Positive percentage:** Potential Generic candidate is priced below the comparison average.
- **Negative percentage:** Potential Generic candidate is priced above the comparison average.
- **Approximately 0%:** Prices are approximately equal.

A negative percentage should therefore be interpreted as the candidate being **higher priced than the comparison average**, rather than as a negative saving.

---

## Important Methodological Note

The price analysis is based on the **listed product price available in the dataset**.

The current project does not normalize prices according to pack size. Therefore, the results should be interpreted as comparisons of the listed product/pack prices available in the dataset.

The Potential Generic and Potential Branded categories are project-defined analytical classifications and should not be considered official medical or regulatory classifications.

This project is intended for **academic and data-analysis purposes** and does not provide medical, pharmaceutical or regulatory certification.

## Initial Dataset Columns

