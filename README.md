# Project Evaluation Analysis – World Bank IEG Data

This repository was developed as part of a professional interview exercise to explore and model the relationship between **Monitoring and Evaluation (M&E) Quality** and **Outcome Ratings** for World Bank projects, using data from the **Independent Evaluation Group (IEG)**. The analysis focuses on projects within the **Human Development Practice Group** approved between **2015 and 2025**.

---

## 📁 Repository Structure

### `1_Data/`
This folder contains the core data and supporting files:
- **IEG Excel Dataset**: Downloaded from IEG’s website under the [Data > WB Project Ratings](https://ieg.worldbankgroup.org/data) section.
- **Shapefiles**: Used to generate the interactive global map.
- **Pickle files**: Output from optimized machine learning models.

---

### `2_Codes/`
Contains three Python notebooks that progressively explore, model, and interpret the relationship between project outcomes and evaluation quality.

#### `1_Data_Analysis.ipynb`
**Question addressed:**  
> _How do Outcome Ratings vary by region?_

This notebook:
- Filters the dataset to include only Human Development projects approved between 2015 and 2025.
- Performs descriptive statistics and visualizations to analyze regional patterns.
- Generates an **interactive choropleth map** showing average outcome scores by country.
- Presents regional distributions using **boxplots** and **bar charts**.

#### `2_Models.ipynb`
**Question addressed:**  
> _What is the relationship between Monitoring and Evaluation (M&E) Quality and Outcome Ratings?_

This notebook includes:
1. **Statistical models**, following [Raimondo (2016)]([https://ieg.worldbankgroup.org/data](https://documents1.worldbank.org/curated/en/180811468197076970/pdf/WPS7726.pdf)):
   - **Ordinary Least Squares (OLS)**
   - **Ordered Logit Regression**
   - **Propensity Score Matching (PSM)** to estimate the Average Treatment Effect (ATT)

2. **Machine Learning models**:
   - Predicts outcome ratings using Random Forests and LightGBM.
   - Computes feature importance to understand the role of M&E Quality.

3. **Text mining extension**:
   - Extracts full-text evaluations from PDFs.
   - Implements **sentiment analysis** on M&E sections (Design, Implementation, Utilization).
   - Uses sentiment scores as predictors in ML models.

#### `3_NLP_Model.ipynb`
This notebook expands the analysis by:
- Using **natural language processing (NLP)** to predict Outcome Ratings directly from evaluation text.
- Extracting and analyzing specific sections of the text:
  - M&E Design
  - M&E Implementation
  - M&E Utilization
  - Overall Outcome section
- Implementing and tuning models (Ordinal Logit, Random Forest, LightGBM) using **Optuna**.
- Identifying and visualizing the most predictive **words and phrases** across models and sections.

---

### `3_Outputs/`
This folder contains:
- Plots.
- An **interactive world map** of outcome scores.
- Feature importance graphs and final model outputs.

## 👤 Author

Prepared by **Diego Parra** (dparraalvarez@worldbank.org). Feel free to reach out for questions or collaboration opportunities.
