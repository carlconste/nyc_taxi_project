# NYC Taxi Data Project

**By: Carl Conste**

This project uses data collected by the *New York City Taxi & Limousine Commission* about “Green” Taxis. Green Taxis, unlike yellow taxis, are taxis that are not permitted to pick up passengers inside of the densely populated areas of Manhattan. 

This project was sourced from StrataScratch and was originally based on a Capital One Data Science Project. The data used for this project is from 2015, however more recent data is available on the [NYC Taxi & Limousine Commission](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page) website. 

The goal of the project was to do an exploratory and predictive analysis of NYC Green Taxi trips from 2015, focusing on characteristics such as tipping behavior, trip characteristics, and geographic traffic patterns.

[View the full analysis here](https://github.com/carlconste/nyc_taxi_project/blob/main/nyc_taxi_analysis.ipynb).

## Key Findings
- **Tipping Behavior**: Tip percentages are concentrated around lower values, with a small number of extreme observations producing abnormally high percentages.
- **Non-linear Modeling**: XGBoost outperformed Linear Regression during cross-validation, suggesting that nonlinear relationships and interactions between trip characteristics are useful for predicting tip percentage.
- **Extreme Observations Affect Model Performance**: The optimized XGBoost model achieved strong performance on typical observations but produced substantially larger errors when evaluated on the test set containing extreme tip percentages.
- Brooklyn accounted for the largest share of borough-level taxi traffic, followed by Manhattan, Queens, the Bronx, and Staten Island.

## Borough Flows Visualization
One part of the project explores intra-vs-inter borough traffic flows and key characteristics through visualizations. An interactive visualization can be found here: [Interactive Borough Map](https://carlconste.github.io/nyc_taxi_project/visualization/borough_traffic_flow.html).
- Points on the map represent intra-borough trips
- Directional arrows represent inter-borough trips, color coded by each borough. 
- Line colors correspond to the *originating* borough.

Data for the GeoJSON files for the borough boundaries are sourced from the [NYC Department of City Planning](https://www.nyc.gov/content/planning/pages/resources/datasets/borough-boundaries).

##
**Tools Used**: Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly, Scikit-learn, XGBoost, GeoPandas