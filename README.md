# Real Estate Price Prediction for Bangalore Houses

## Project Overview

This project aims to develop a machine learning model to predict real estate prices for houses in Bangalore. The model is designed to assist buyers, sellers, and real estate agents in estimating property values based on various features. 

## Technical Approach

The core algorithms used in this project are advanced regression techniques, specifically Gradient Boosting and Random Forest, known for their robustness in prediction tasks. The project was implemented using Python, leveraging machine learning and statistical libraries such as scikit-learn, along with extensive Exploratory Data Analysis (EDA).

## Steps Taken

### 1. Data Preprocessing and Analysis

- **Dropping Irrelevant Columns:** Removed columns that do not contribute to the prediction of house prices.
- **Handling Missing Values:** Null values were either dropped or filled using median or mean values depending on the context.
- **Standardizing the Bedroom Column:** Converted inconsistent formats like "4 bedroom" and "4BHK" to a uniform format.
- **Filtering Anomalous Data:**
  - Removed data where the number of bedrooms was unusually high (e.g., 30 or 40) compared to the total square footage.
  - Standardized square footage ranges by taking the average when given as a range (e.g., 1200 - 1330 sqft).
  - Handled different units of area, converting them to a consistent measurement (square feet).

### 2. Feature Engineering and Dimensionality Reduction

- **Price per Square Foot:** Created a new feature to represent the price per square foot.
- **Location Simplification:** 
  - With over 1300 unique locations, one-hot encoding was not feasible.
  - Locations appearing less than 10 times were grouped into an "Other" category.
- **Principal Component Analysis (PCA):** Considered for dimensionality reduction to reduce the complexity of the dataset.

### 3. Outlier Removal

- **IQR Method:** The Interquartile Range (IQR) was initially considered for outlier removal.
- **Domain Knowledge Application:**
  - Removed data points where one bedroom was less than 150 sqft, as this is unrealistic.
  - Identified and removed properties with abnormally low prices, which were not possible in Bangalore’s real estate market.
  - Used descriptive statistics and histograms to identify and visualize outliers, ensuring the dataset was well-suited for model training.
  - Removed properties with an unrealistic number of bathrooms compared to bedrooms.

## Results

The model achieved strong predictive performance, with Gradient Boosting and Random Forest demonstrating robustness and accuracy in estimating real estate prices.

## Conclusion

This project successfully developed a machine learning model capable of predicting house prices in Bangalore with a high degree of accuracy. By leveraging domain knowledge, careful preprocessing, feature engineering, and outlier removal, the model was able to provide valuable insights into property valuation.

## Future Work

- **Further Model Optimization:** Explore other techniques.
- **Enhanced Feature Engineering:** Incorporate additional data such as proximity to amenities or historical price trends.
- **Deployment:** Integrate the model into a web application for real-time prediction.

---

