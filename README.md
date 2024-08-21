# California Housing Prices

## Project Description
This project aims to predict the median house values in California using various machine learning models. The dataset contains information about census blocks in California, including features such as longitude, latitude, median age, total rooms, bedrooms, population, households, median income, and ocean proximity.

The key goals of this project are:
1. Predict the median house values using different models.
2. Explore the relationship between ocean proximity and home values.

## Dataset
The dataset used in this project is the [California House Prices](https://www.kaggle.com/datasets/camnugent/california-housing-prices) dataset, which is based on the 1990 census data.

## Features
The dataset includes the following features:
- `longitude`: Longitude coordinate
- `latitude`: Latitude coordinate
- `median_age`: Median age of the houses in the census block
- `total_rooms`: Total number of rooms in the census block
- `total_bedrooms`: Total number of bedrooms in the census block
- `population`: Total population in the census block
- `households`: Total number of households in the census block
- `median_income`: Median income of the households in the census block
- `median_house_value`: Median house value of the houses in the census block
- `ocean_proximity`: Categorical feature indicating the proximity to the ocean

## Data Cleaning
The dataset was cleaned by:
1. Dropping all null values.
2. Eliminating outliers for the `population` feature.
3. 

## Exploratory Data Analysis
1. Analyzed the distribution of the `median_house_value` feature using histograms.
2. Investigated the relationship between `median_house_value` and `median_income` for different `ocean_proximity` categories using scatter plots and correlation analysis.
3. Examined the distribution of `median_income` across the California coordinates using a KMeans clustering analysis.

## Modeling
1. Developed a Multiple Linear Regression model with `median_income` and `ocean_proximity` as the selected features.
2. Implemented a KNN Regressor model to predict the `median_house_value` using `median_income` and `ocean_proximity`.
3. Performed a Simple Logistic Regression using the `near_ocean` boolean feature to predict the probability of a house being near the ocean.

## Model Evaluation
### KNN Regressor Model
- **K = 145**
- **Total number of samples: 20,640**
- **Training set R²: 0.532**
- **Testing set R²: 0.513**
- The scatter plot of predicted vs. true values for the `near_ocean = 1` boolean feature shows a relatively positive, strong, and linear relationship.

### Logistic Regression Model
- The Logistic Regression model predicts the probability of a house being near the ocean, rather than the actual house value.
- The classification matrices for the training and testing datasets show the model's precision, recall, and F1 score.
- The plot of the odds (Probability of a house being near the ocean vs. percentile) reveals that more expensive houses are up to 7.3 times more likely to be near the beach than cheaper homes.

## Conclusion
The project successfully explored the relationship between ocean proximity and home values in California, and developed predictive models to estimate the median house values. The KNN Regressor model demonstrated a strong positive correlation between median income and median house value, with the model achieving a reasonable R-squared score on both the training and testing sets. The Logistic Regression model provided insights into the probability of a house being near the ocean, revealing that more expensive homes are significantly more likely to be located near the beach.

## Repository Contents
- `california_housing_project.ipynb`: Jupyter Notebook containing extensive project experimentation, analysis, and most plots mentioned and not mentioned in the README.md file
- `data`: Directory containing the California House Prices dataset.
- `README.md`: This README file.

## Project Contributors
- Ryan Cullen
- Aidan Murray
- Yash Bhatt
- Madeline Dodson
