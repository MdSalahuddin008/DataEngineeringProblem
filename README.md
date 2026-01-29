### Approach Summary

Part A – Web Scraping:
IndiaMART is a dynamically rendered website without public APIs.
Selenium was used to handle JavaScript-loaded content.
Due to inconsistent DOM structures, supplier name and price were extracted using
class-based selectors, while location was heuristically extracted from visible card text.

Part B – Data Cleaning:
Rows with missing supplier names were removed as supplier identity is critical.
Prices were converted to numeric and missing prices were filled using mean imputation
to avoid losing records.
A new 'area' feature was engineered by splitting location strings (Bengaluru – Area).

Exploratory Data Analysis:
Visualizations were created to analyze supplier distribution, area-wise product density,
average price trends, and category-wise pricing.
