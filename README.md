#  Generic vs Branded Medicine Price Comparison

A data analysis project that identifies **Potential Generic** and **Potential Branded** medicine products and compares their listed prices within comparable medicine groups.

---

##   Project Overview

The **Generic vs Branded Medicine Price Comparison** project is a data analysis project focused on comparing the listed prices of potential generic-name medicines with other comparable medicine products.

The project uses pharmaceutical product data and applies:

- Data loading
- Data filtering
- Data extraction
- Data cleaning
- Data transformation
- Data grouping
- Data aggregation
- Statistical analysis
- Data visualization
- Results interpretation

The comparison is performed using:

- **Primary Ingredient**
- **Primary Strength**
- **Dosage Form**
- **Listed Price**

A project-defined analytical method is used to identify **Potential Generic** and **Potential Branded** products based on the relationship between the medicine name and its primary ingredient.

> **Important:** The terms **Potential Generic** and **Potential Branded** are project-defined analytical categories. They are not official regulatory classifications.

---

#   Problem Statement

Medicines with the same or comparable active ingredients can have different listed prices depending on the product and manufacturer.

However, identifying meaningful price differences requires comparing products that have comparable characteristics rather than comparing unrelated medicines.

### Problem Statement

> To analyze pharmaceutical products and identify potential generic-name medicines, group comparable medicines using primary ingredient, strength, and dosage form, and compare their listed prices with other products in the same comparison group.

The project aims to provide a data-driven view of observed medicine price differences within comparable product groups.

---

#   Objectives

The main objectives of this project are:

- To load and inspect the pharmaceutical product dataset using Python and Pandas.
- To acquire and filter relevant medicine records for analysis.
- To extract the important attributes required for medicine comparison.
- To validate and clean the pharmaceutical dataset.
- To handle missing values, duplicate records, invalid prices, and inconsistent values.
- To standardize medicine names, ingredients, strengths, manufacturers, and dosage forms.
- To create comparison groups using primary ingredient, primary strength, and dosage form.
- To identify **Potential Generic** medicine candidates using a project-defined name-to-ingredient matching approach.
- To classify the remaining products as **Potential Branded** for project-level analysis.
- To calculate average prices within comparable medicine groups.
- To compare the listed price of Potential Generic candidates with the average listed price of other products in the same comparison group.
- To calculate price differences and percentage price differences.
- To visualize the results using appropriate charts.
- To interpret the observed price differences.
- To document the methodology, findings, limitations, and future scope.

---

#   Scope and Significance

## Scope

The project focuses on analyzing pharmaceutical product data available in the selected dataset.

The analysis includes:

- Pharmaceutical product information
- Medicine names
- Manufacturers
- Listed prices
- Primary ingredients
- Primary strengths
- Dosage forms
- Comparison groups
- Potential Generic identification
- Price comparison
- Data visualization
- Results interpretation

Products are grouped using:

**Primary Ingredient + Primary Strength + Dosage Form**

This helps ensure that price comparisons are performed among products with comparable characteristics.

## Significance

The project demonstrates how data analysis techniques can be applied to pharmaceutical product data to identify and understand price variation.

The analysis can help:

- Identify potential generic-name products in the dataset.
- Identify comparable medicine products.
- Observe differences in listed prices.
- Quantify price differences using percentage calculations.
- Present price variation using visualizations.
- Demonstrate the practical use of Python and Pandas in a real-world dataset.

> **Academic Scope:** This project is intended for academic data-analysis purposes. It does not provide medical advice, pharmaceutical certification, or official regulatory classification.

---

#  5. Dataset

## Dataset Name

**Indian Pharmaceutical Products Dataset**

## Dataset Source

The dataset was acquired from **Kaggle** and contains information about pharmaceutical products available in the Indian pharmaceutical market.

**Source:** Indian Pharmaceutical Products Dataset – Kaggle

## Dataset Description

The dataset contains pharmaceutical product information such as:

- Product ID
- Medicine/Product name
- Manufacturer
- Listed price
- Dosage form
- Pack size
- Active ingredients
- Primary ingredient
- Primary strength
- Therapeutic class
- Packaging information

## Initial Dataset Size

| Dataset Property | Value |
|---|---:|
| **Records** | **253,973** |
| **Columns** | **15** |

## Dataset Columns

| Column | Description |
|---|---|
| `product_id` | Unique identifier of the medicine product |
| `brand_name` | Name of the medicine/product |
| `manufacturer` | Manufacturer or pharmaceutical company |
| `price_inr` | Listed price in Indian Rupees |
| `is_discontinued` | Indicates whether the product is discontinued |
| `dosage_form` | Form of the medicine |
| `pack_size` | Quantity or size of the medicine pack |
| `pack_unit` | Unit associated with the pack size |
| `num_active_ingredients` | Number of active ingredients |
| `primary_ingredient` | Main or primary ingredient |
| `primary_strength` | Strength of the primary ingredient |
| `active_ingredients` | Active ingredients present in the product |
| `therapeutic_class` | Therapeutic category of the medicine |
| `packaging_raw` | Original packaging information |
| `manufacturer_raw` | Original manufacturer information |

## Dataset Processing

During the data processing stage, records with invalid or zero prices were removed.

After filtering invalid price records, the dataset contained:

**253,969 records**

Further validation and cleaning were performed before creating the final comparison-ready dataset.

---

#   Project Workflow

The project follows the **8-stage data analysis pipeline** required for the DAE project.


Data Loading & Reading
          ↓
Data Acquisition & Filtering
          ↓
Data Extraction
          ↓
Data Validation & Cleaning
          ↓
Data Aggregation & Representation
          ↓
Data Analysis
          ↓
Data Visualization
          ↓
Results & Interpretation

##  Data Loading & Reading

The pharmaceutical dataset is loaded into Python using Pandas.

The dataset is initially inspected to understand:

- Number of records
- Number of columns
- Column names
- Data types
- Missing values
- Unique values
- Overall structure

---

##  Data Acquisition & Filtering

The dataset is acquired from the selected source and filtered to retain records relevant to the medicine price comparison.

Invalid or zero-price records are removed because they cannot be used for meaningful price comparison.

---

##  Data Extraction

Relevant attributes are extracted from the original dataset.

Important fields include:

- Product ID
- Medicine name
- Manufacturer
- Price
- Dosage form
- Pack size
- Primary ingredient
- Primary strength
- Active ingredients
- Therapeutic class

---

##  Data Validation & Cleaning

The extracted data is validated and cleaned.

The process includes:

- Missing-value checking
- Duplicate Product ID checking
- Invalid price checking
- Strength validation
- Ingredient validation
- Dosage-form consistency checking
- Standardization of important text fields

### Final Comparison-Ready Dataset

After validation and cleaning, the comparison-ready dataset contained:

| Property | Value |
|---|---:|
| **Records** | **225,731** |
| **Columns** | **18** |
| **Comparison Groups** | **4,344** |
| **Missing Prices** | **0** |
| **Unknown Strengths** | **0** |
| **Duplicate Product IDs** | **0** |

---

##  Data Aggregation & Representation

Products are grouped using:

**Primary Ingredient + Primary Strength + Dosage Form**

For each comparison group, the following price statistics are calculated:

- Product count
- Minimum price
- Maximum price
- Average price

These aggregated values help identify price variation among comparable products.

---

##  Data Analysis

The analysis includes:

- Potential Generic identification
- Potential Branded classification
- Comparison-group analysis
- Price comparison
- Price difference calculation
- Percentage price difference calculation

Potential Generic candidates are identified using a project-defined method that compares the cleaned medicine name with the primary ingredient.

---

##  Data Visualization

The analysis results are represented using charts such as:

- Potential Generic vs Potential Branded distribution
- Potential Generic Price vs Average Comparison Price
- Medicine Price Distribution
- Price Distribution Comparison
- Percentage Price Difference
- Comparison Group Analysis

---

##  Results & Interpretation

The final stage presents:

- Major analytical findings
- Price differences
- Percentage differences
- Important observations
- Conclusions
- Limitations
- Future scope

The results are interpreted based on the listed prices available in the dataset.

---

#  Project Visualizations

The visual outputs generated during the project are maintained separately in the `Images` folder.

### Potential Generic vs Potential Branded

![Potential Generic vs Potential Branded](Images/potential_generic_vs_branded.png)

### Potential Generic Price vs Average Comparison Price

![Potential Generic Price vs Average Comparison Price](Images/generic_price_vs_average.png)

### Medicine Price Distribution

![Medicine Price Distribution](Images/medicine_price_distribution.png)

### Price Distribution Comparison

![Price Distribution Comparison](Images/price_distribution_comparison.png)

### Percentage Price Difference

![Percentage Price Difference](Images/percentage_price_difference.png)

### Comparison Group Analysis

![Comparison Group Analysis](Images/comparison_group_analysis.png)

> **Note:** The image filenames in the `Images` folder must exactly match the filenames used in this README.

---

#  Important Dataset Attributes

The dataset contains information about pharmaceutical products available in the Indian pharmaceutical market.

## Important Attributes

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

## Main Attributes Used for Comparison

The major attributes used in medicine comparison are:

- `brand_name`
- `price_inr`
- `primary_ingredient`
- `primary_strength`
- `dosage_form`
- `manufacturer`

---

#  Data Loading & Inspection

The pharmaceutical dataset was loaded into Python using the **Pandas** library.

The dataset was read using `pd.read_csv()` and inspected before performing further processing.

## Initial Dataset Information

- **Records:** 253,973
- **Columns:** 15

## Inspection Performed

The following operations were performed:

- Checking the dataset shape
- Viewing the first few records
- Checking column names
- Checking data types
- Checking missing values
- Examining unique values
- Understanding the overall dataset structure

The inspection helped identify the important attributes required for further processing and analysis.

---

#  Data Acquisition & Filtering

The dataset used for this project is the **Indian Pharmaceutical Products Dataset**.

The dataset was acquired from Kaggle and processed in the project environment.

## Dataset Source

**Indian Pharmaceutical Products Dataset – Kaggle**

## Filtering Performed

The dataset was filtered to retain records useful for medicine price comparison.

The main filtering criteria included:

- Valid medicine product records
- Valid price information
- Relevant ingredient information
- Relevant strength information
- Relevant dosage-form information

Records with invalid or zero prices were removed because they cannot be used for meaningful price comparison.

After filtering invalid price records, the dataset contained:

**253,969 records**

---

#  Data Extraction

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

Selecting relevant attributes reduced the complexity of the dataset and made subsequent validation, transformation and analysis easier.

---

#  Data Validation & Cleaning

Data validation was performed to check whether the dataset was suitable for further analysis.

The following validation checks were performed:

- Checking missing values
- Checking duplicate Product IDs
- Checking invalid prices
- Checking unknown or missing strengths
- Checking important ingredient information
- Checking dosage-form consistency
- Checking the structure of comparison groups

## Final Comparison-Ready Dataset

| Validation Property | Result |
|---|---:|
| Records | **225,731** |
| Columns | **18** |
| Comparison Groups | **4,344** |
| Missing Prices | **0** |
| Unknown Strengths | **0** |
| Duplicate Product IDs | **0** |

These validation checks helped ensure that the data used for analysis was consistent with the project requirements.

---

#  Missing-Value Handling

Missing values were identified using Pandas operations such as:

```python
isnull()
sum()
