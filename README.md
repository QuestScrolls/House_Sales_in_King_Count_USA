Automobile Sales Statistics Dashboard Capstone Project
Overview
This capstone project analyzes historical automobile sales data (1980-2023) to visualize trends, recession impacts, and statistics. It uses Python for data processing and visualization, creating interactive dashboards and maps to explore sales by year, vehicle type, unemployment rates, and geography. The project highlights skills in data wrangling, EDA, and interactive visualization.
Key focus: Identify how recessions affect sales, advertising expenditure, and vehicle types.
Objectives

Import and clean automobile sales data using Pandas.
Create visualizations with Matplotlib and Seaborn (e.g., line plots for sales trends, bar plots for vehicle types).
Build an interactive Folium map for geographical sales analysis during recessions.
Develop a Dash web app for dynamic reporting (e.g., yearly vs. recession statistics, with dropdowns and graphs).

Data Sources

CSV File: historical_automobile_sales.csv (loaded via URL in notebooks).
Key Columns: Date, Year, Month, Recession (binary flag), Automobile_Sales, Vehicle_Type, Unemployment_Rate, Advertising_Expenditure, City (for mapping).

Methodology
The project is divided into two Jupyter notebooks:

DV0101EN-Final-Assign-Part1.ipynb (Visualizations with Matplotlib, Seaborn, Folium):
Loaded and explored data.
Created line plots (e.g., yearly sales fluctuations during recessions).
Bar plots (e.g., average sales by vehicle type).
Pie charts (e.g., advertising expenditure share by vehicle type).
Geographical analysis: Folium choropleth map showing sales by city during recessions (using 'us-states.json' GeoJSON).
Saved plots as images (e.g., 'recession_sales_line.png') for peer review.

DV0101EN-Final-Assign-Part2.ipynb (Interactive Dash App):
Built a Dash web app with dropdowns for statistics type (Yearly/Recession) and year selection.
Callbacks to dynamically update graphs based on inputs.
Recession Report: Line chart for sales over years, bar chart for vehicle types, pie chart for ad expenditure, bar chart for unemployment effects.
Yearly Report: Line charts for total/ monthly sales, bar chart for average vehicles sold, pie chart for ad expenditure by vehicle.
Layout: Flexbox styling for grid-based chart display.
Run: python app.py (opens at http://127.0.0.1:8050/).


Results

Insights:
Sales drop significantly during recessions (e.g., 2008-2009 financial crisis).
Economy vehicles sell better during high unemployment; luxury vehicles correlate with higher ad spend.
Geographical patterns: Higher sales in urban areas like New York during non-recession periods.

Visuals: Interactive elements allow filtering; e.g., pie charts show ~40% ad spend on SUVs.
Challenges: Handled dynamic disabling of year dropdown for recession mode; ensured no data scenarios return empty graphs.

Technologies Used

Python Libraries: Pandas, NumPy, Matplotlib, Seaborn, Folium, Dash, Plotly Express, More-Itertools.
Tools: Jupyter Notebooks, GitHub for version control.

How to Run the Project

Clone the repository: git clone <your-github-repo-url>.
Install dependencies: pip install -r requirements.txt (include: pandas, dash, plotly, folium, matplotlib, seaborn, more-itertools).
Run notebooks: Open in Jupyter (jupyter notebook) and execute cells.
For Dash App: Run python DV0101EN-Final-Assign-Part2.ipynb (or export to .py) and access the dashboard in your browser.

Limitations and Future Work

Data is historical (up to 2023); integrate real-time APIs for updates.
Expand to predictive ML (e.g., forecast sales using Scikit-learn).
Deploy Dash app to Heroku for public access.

References

IBM Data Visualization with Python Course (Coursera).
Data Source: IBM Skills Network.
