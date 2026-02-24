House Sales in King County, USA: Machine Learning Prediction Project
Overview
This project predicts house prices in King County, USA (including Seattle) using historical sales data. It applies machine learning techniques like linear regression, polynomial features, and Ridge regression to model factors influencing prices (e.g., bedrooms, square footage, location). The goal is to build and evaluate models for accurate price estimation, demonstrating data analysis and ML skills.
Objectives

Import and explore the King County house sales dataset.
Perform data wrangling (e.g., handle missing values, drop irrelevant columns).
Conduct Exploratory Data Analysis (EDA) with visualizations (e.g., boxplots, scatter plots, heatmaps).
Develop and fit regression models (simple linear, multiple linear, polynomial, Ridge).
Evaluate models using metrics like R² score and refine via cross-validation/pipelines.

Data Sources

CSV File: kc_house_data.csv (loaded via URL in the notebook).
Key Columns: id, date, price (target), bedrooms, bathrooms, sqft_living, sqft_lot, floors, waterfront, view, condition, grade, yr_built, yr_renovated, zipcode, lat, long.
Dataset Size: ~21,000 entries from 2014-2015 sales.

Methodology
The project is implemented in a single Jupyter notebook: House_Sales_in_King_Count_USA(2).ipynb.

Module 1: Importing Data:
Loaded data using Pandas; displayed head, described stats, and checked types.

Module 2: Data Wrangling:
Dropped irrelevant columns (id, Unnamed: 0).
Handled missing values in 'bedrooms' and 'bathrooms' (replaced with means).
Converted 'floors' to integer.

Module 3: Exploratory Data Analysis:
Boxplots for price by waterfront/view.
Regression plots for sqft_living vs. price.
Correlation heatmaps to identify features (e.g., high correlation with sqft_living, bathrooms).

Module 4: Model Development:
Simple Linear Regression: sqft_living vs. price (R² ~0.49).
Multiple Linear Regression: Using features like floors, waterfront, lat, etc. (R² ~0.65).
Polynomial Regression: Transformed features (degree 2); improved R² (~0.75).
Visualized predictions with distribution plots.

Module 5: Model Evaluation and Refinement:
Used pipelines for scaling/polynomial transforms.
Ridge Regression with alpha optimization (R² ~0.66).
Cross-validation for robust scoring; tested on holdout set.


Results

Key Insights: Price strongly correlates with living space, location (lat/long), and views. Waterfront homes are pricier.
Model Performance:
Linear: R² = 0.49-0.65.
Polynomial (degree 2): R² = 0.75 (best performer).
Ridge: R² = 0.66 (with regularization to prevent overfitting).

Visuals: Regression lines, residual plots, and distribution comparisons show model fit.

Technologies Used

Python Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn (LinearRegression, PolynomialFeatures, Ridge, Pipeline, cross_val_score).
Tools: Jupyter Notebooks.

How to Run the Project

Clone the repository: git clone <your-github-repo-url>.
Install dependencies: pip install -r requirements.txt (include: pandas, numpy, matplotlib, seaborn, scikit-learn).
Run the notebook: Open in Jupyter (jupyter notebook) and execute cells sequentially.
Data Download: The notebook fetches data via URL; ensure internet access.

Limitations and Future Work

Data is from 2014-2015; update with recent sales for better relevance.
Incorporate advanced models (e.g., Random Forest, XGBoost) or external data (e.g., economic indicators).
Deploy as a web app (e.g., using Streamlit) for interactive price predictions.

References

IBM Data Analysis with Python Course (Coursera).
Dataset: King County House Sales (public domain).
