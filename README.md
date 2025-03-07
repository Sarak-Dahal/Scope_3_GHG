# Scope 3 Greenhouse Gas Emissions Prediction
This repository contains the code, datasets, and trained models for predicting Scope 3 Greenhouse Gas (GHG) emissions using machine learning techniques. Scope 3 emissions are indirect emissions that occur across a company's value chain, accounting for 75-90% of total corporate emissions. This project aims to provide organizations with tools to better estimate and understand their Scope 3 emissions.

## Key Features
1. Data Sources
Carbon Disclosure Project (CDP): Reported emissions data from over 5,800 organizations (2013–2023).

Financial Modeling Prep APIs: Financial metrics like revenue, market capitalization, and industry classifications.

Combined these datasets to link financial performance with environmental impact.

2. Libraries Used
pandas: Data manipulation and analysis.

scikit-learn: Machine learning algorithms and preprocessing.

XGBoost: Gradient boosting framework for high-performance modeling.

Plotly: Interactive data visualization.

3. Exploratory Data Analysis (EDA)
Visualizations include:

Scope 3 Emissions by Industry
This bar chart shows the total Scope 3 emissions contributed by different industries:

Manufacturing is the largest contributor, with over 150 billion units of emissions.

Other significant contributors include Services, Retail, and Food & Agriculture industries.

Industries like Apparel, Biotech & Pharma, and Hospitality have relatively lower emissions.

Scope 3 Emissions by Sector
This bar chart provides a granular view of Scope 3 emissions by specific sectors:

Electrical & Electronic Equipment is the highest-emitting sector.

Thermal Power Generation is another major contributor.

Highlighting emission hotspots within sectors helps prioritize reduction efforts.

4. Model Creation
I created individual models for each of the 17 Scope 3 emission categories using XGBoost. Key steps include:

Target encoding for categorical variables like Primary Activity and Region.

Feature selection to reduce multicollinearity.

Imputation for missing values (e.g., linear regression for Employee_Count).

Hyperparameter tuning using GridSearchCV.

5. Pickle Files
To ensure modularity and flexibility:

Trained models and encoders were saved as pickle files.

Separate pickle files were created for each emission type, enabling easy loading and reuse without retraining.

6. Feature Importance
Feature importance analysis revealed:

Revenue as the most significant predictor of Scope 3 emissions.

Other important features include industry sector, number of employees, and geographic region.
