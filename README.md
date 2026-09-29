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


---

#  5. Dataset

## Dataset Name

**Indian Pharmaceutical Products Dataset**

## Dataset Source

The dataset was acquired from **Kaggle** and contains information about pharmaceutical products available in the Indian pharmaceutical market.

**Source:** Indian Pharmaceutical Products Dataset – Kaggle
https://www.kaggle.com/datasets/rishgeeky/indian-pharmaceutical-products


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

#  Duplicate Validation

Duplicate validation was performed to ensure that the same product was not unintentionally represented multiple times.

The `product_id` field was used as the main identifier for checking duplicate products.

## Duplicate Checks

The following checks were performed:

- Identification of duplicate Product IDs
- Counting duplicate records
- Validating Product ID uniqueness after cleaning

The final comparison-ready dataset contained:

**0 duplicate Product IDs**

This helped ensure that products were represented correctly during the analysis.

---

#  Data Cleaning and Filtering

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

#  Data Transformation

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

#  Feature Engineering

Feature engineering was used to create additional analytical attributes from the existing dataset.

The project created derived features to support medicine comparison.

## Important Engineered Features

- Cleaned medicine-name representation
- Cleaned ingredient representation
- Cleaned strength representation
- Cleaned dosage-form representation
- `comparison_group`
- `medicine_type`
- Price difference
- Percentage price difference

These features were created during the project to support classification, grouping, and price analysis.

---

#  Comparison Group Creation

A comparison group was created to identify medicines with comparable characteristics.

The project defines a comparison group using:

**Primary Ingredient + Primary Strength + Dosage Form**

The standardized values were combined to create the `comparison_group`.

#  Pandas Operations

Pandas was extensively used for data loading, cleaning, transformation, grouping, and analysis.

## Main Pandas Operations Used

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

#  Grouping, Sorting, Aggregation & Filtering

Grouping was used to organize medicines according to their comparison groups.

The project used grouping operations to calculate:

- Product count
- Minimum price
- Maximum price
- Average price

## Sorting

Sorting was used to identify:

- Highest price differences
- Lowest price differences
- Highest percentage differences
- Lowest percentage differences

## Filtering

Filtering was used to separate:

- Potential Generic candidates
- Potential Branded products
- Products with lower prices
- Products with higher prices
- Products with approximately equal prices

## Aggregation

Aggregation was used to summarize prices within each comparison group.

These operations helped convert the raw pharmaceutical dataset into meaningful analytical results.

---

#  Potential Generic-Name Identification

The dataset does not contain an official generic/branded classification field.

Therefore, the project uses a **project-defined analytical method** to identify **Potential Generic** medicine candidates.

## Identification Method

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

## Classification Principle -- primary ingredient
#  Potential Generic-Name Identification

The dataset does not contain an official generic/branded classification field.

Therefore, the project uses a **project-defined analytical method** to identify **Potential Generic** medicine candidates.

## Identification Method

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

## Classification Principle

The classification is based on the relationship between:

**Medicine Name ↔ Primary Ingredient**

It is **not** based solely on:

- Manufacturer
- Price

> **Important:** The terms **Potential Generic** and **Potential Branded** are project-defined analytical categories. They should not be interpreted as official regulatory classifications of medicines.

The categories are used only for the purpose of this project's data analysis and price comparison.

---

#  Statistical Analysis

Statistical analysis was performed to understand price differences among comparable medicines.

## Metrics Considered

The analysis considered:

- Number of Potential Generic candidates
- Number of Potential Branded products
- Number of comparison groups
- Minimum price
- Maximum price
- Average price
- Price difference
- Percentage price difference

## Analysis Performed

The analysis also identified:

- Potential Generic candidates priced below the comparison average
- Potential Generic candidates priced above the comparison average
- Cases where prices were approximately equal

This analysis helps identify the extent of price variation among products with comparable characteristics.

---

#  Price Comparison Method

The price comparison was performed after identifying Potential Generic candidates and their corresponding comparison groups.

## Comparison Process

For each **Potential Generic** candidate:

1. Its `comparison_group` was identified.
2. Other products belonging to the same comparison group were identified.
3. The candidate itself was excluded from the comparison set.
4. The average listed price of the other products was calculated.
5. The candidate's listed price was compared with this average.

## Comparison Criteria

The products being compared have the same:

- **Primary ingredient**
- **Primary strength**
- **Dosage form**

The project uses the **average listed price of other products in the same comparison group** as the reference price.

---

#  Price Difference

The price difference is calculated using the following formula:

## Formula

**Price Difference = Average Price of Other Products − Potential Generic Price**

## Interpretation

### If Price Difference > 0

The Potential Generic candidate has a **lower listed price** than the average price of the other products in the same comparison group.

### If Price Difference < 0

The Potential Generic candidate has a **higher listed price** than the comparison average.

### If Price Difference ≈ 0

The prices are approximately equal.

Therefore, the project does not automatically treat every price difference as a saving.

---

#  Percentage Price Difference

The percentage price difference is calculated using the average price of other products as the reference.

## Formula

**Percentage Price Difference**

**= ((Average Other Price − Candidate Price) / Average Other Price) × 100**

## Example

Suppose:

- **Average price of other products = ₹100**
- **Potential Generic price = ₹70**

### Step 1: Calculate Price Difference

**Price Difference = ₹100 − ₹70**

**= ₹30**

### Step 2: Calculate Percentage Price Difference

**Percentage Price Difference = (₹30 / ₹100) × 100**

**= 30%**

Therefore, the Potential Generic candidate's listed price is **30% lower than the comparison average**.

## Interpretation

| Percentage | Interpretation |
|---|---|
| **Positive %** | Potential Generic candidate is priced below the comparison average |
| **Negative %** | Potential Generic candidate is priced above the comparison average |
| **Approximately 0%** | Prices are approximately equal |

A negative percentage should therefore be interpreted as the candidate being **higher priced than the comparison average**, rather than as a negative saving.

---



The classification is based on the relationship between:
