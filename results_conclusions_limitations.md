# Results, Conclusions and Limitations

## 1. Results

The project analyzed pharmaceutical products to compare the listed prices of products having comparable characteristics.

The comparison was based on:

- Primary ingredient
- Primary strength
- Dosage form
- Listed price

### Final Dataset Results

The final comparison-ready dataset contained:

- **225,731 records**
- **18 columns**
- **4,344 comparison groups**
- **0 missing prices**
- **0 unknown strengths**
- **0 duplicate Product IDs**

### Potential Generic Identification

The dataset does not contain an official generic or branded classification.

Therefore, a project-defined name-based method was used to identify **Potential Generic** candidates.

The cleaned medicine name was compared with the cleaned primary ingredient.

If the cleaned medicine name matched the primary ingredient, the product was classified as:

**Potential Generic**

Otherwise, it was classified as:

**Potential Branded**

These are project-defined analytical categories and should not be considered official regulatory classifications.

### Price Comparison Results

Each Potential Generic candidate was compared with the average listed price of other products in the same comparison group.

The comparison group was created using:

**Primary Ingredient + Primary Strength + Dosage Form**

The analysis identified cases where Potential Generic candidates had:

- Lower prices than the comparison average
- Higher prices than the comparison average
- Approximately equal prices

This demonstrates that price differences exist among comparable pharmaceutical products, but the differences are not uniform across all products.

---

## 2. Price Difference

The price difference was calculated using:

**Price Difference = Average Price of Other Products − Potential Generic Price**

### Interpretation

- A **positive** price difference means the Potential Generic candidate has a lower listed price than the comparison average.
- A **negative** price difference means the Potential Generic candidate has a higher listed price than the comparison average.
- A value close to **zero** means the prices are approximately equal.

Therefore, the project does not automatically treat every price difference as a saving.

---

## 3. Percentage Price Difference

The percentage price difference was calculated using:

**Percentage Price Difference = ((Average Other Price − Candidate Price) / Average Other Price) × 100**

### Interpretation

- **Positive percentage:** Candidate price is below the comparison average.
- **Negative percentage:** Candidate price is above the comparison average.
- **Approximately 0%:** Prices are approximately equal.

This provides a relative measure of the observed price difference.

---

## 4. Visualization Results

The project used multiple visualizations to understand medicine prices and price differences.

The main visualizations included:

1. Potential Generic vs Potential Branded distribution
2. Potential Generic Price vs Average Comparison Price
3. Medicine Price Distribution
4. Price Distribution Comparison using Box Plot
5. Percentage Price Difference
6. Comparison-group price analysis

These visualizations helped identify price variation and differences among comparable pharmaceutical products.

---

# 5. Conclusion

The project demonstrates a data-driven approach for comparing listed prices of pharmaceutical products with comparable characteristics.

Medicines were grouped according to:

- Primary ingredient
- Primary strength
- Dosage form

A project-defined name-based method was then used to identify Potential Generic candidates.

The identified candidates were compared with the average listed price of other products in the same comparison group.

The analysis showed that price differences exist among comparable pharmaceutical products. Some Potential Generic candidates had lower listed prices than the comparison average, while some had higher prices.

Therefore, the project demonstrates that pharmaceutical product prices can vary even when products have comparable primary ingredients, strengths and dosage forms.

The project provides a structured analytical approach for studying observed price differences in the available pharmaceutical dataset.

---

# 6. Limitations

## 6.1 No Official Generic/Branded Label

The dataset does not provide an official generic or branded classification.

Therefore, the project uses a project-defined name-based method to identify Potential Generic candidates.

This classification should not be considered an official regulatory classification.

## 6.2 Pack-Size Normalization

The current analysis compares listed product prices available in the dataset.

Prices are not normalized according to pack size.

Therefore, differences in pack quantity may affect direct price comparisons.

## 6.3 Dataset Dependency

The results depend on the quality, completeness and accuracy of the available dataset.

Missing, incorrect or outdated information can affect the analysis.

## 6.4 Primary Ingredient-Based Grouping

Comparison groups are created using primary ingredient, primary strength and dosage form.

Products may contain additional active ingredients or other characteristics that are not fully represented by these three attributes.

## 6.5 Listed Price

The analysis uses the listed product price available in the dataset.

Actual market prices may vary depending on factors such as location, seller, discounts and other conditions.

## 6.6 Analytical Classification

Potential Generic and Potential Branded are project-defined analytical categories.

They should not be interpreted as official medical or regulatory classifications.

## 6.7 Academic Scope

This project is a data-analysis project.

It does not evaluate:

- Medical effectiveness
- Clinical outcomes
- Safety
- Therapeutic equivalence
- Prescribing decisions
- Medical suitability

---

# 7. Future Scope

The project can be extended in the future by:

- Adding official generic/branded classification data
- Normalizing prices by pack size or quantity
- Including multiple active ingredients in comparison criteria
- Adding historical price data
- Comparing prices across different locations
- Adding more pharmaceutical datasets
- Developing an interactive dashboard
- Improving generic-name identification using Natural Language Processing techniques
- Performing more detailed statistical analysis

---

# 8. Final Project Outcome

The project demonstrates a complete data-analysis workflow involving:

- Data loading
- Data acquisition and filtering
- Data extraction
- Data validation and cleaning
- Data transformation
- Feature engineering
- Comparison-group creation
- Data aggregation
- Statistical analysis
- Price comparison
- Data visualization
- Results interpretation

The project provides a structured approach for studying observed price differences among comparable pharmaceutical products.

---

## Academic Disclaimer

This project is developed for academic and data-analysis purposes.

The Potential Generic and Potential Branded classifications are project-defined analytical categories and are not official regulatory classifications.

The project does not provide medical advice, pharmaceutical certification, therapeutic-equivalence assessment or recommendations for medicine selection.
