# Used Car Price Prediction

## Project Overview

This project focuses on predicting the prices of used cars listed on Craigslist across the United States. Leveraging a comprehensive dataset scraped from Craigslist, the project includes data preprocessing, exploratory data analysis (EDA), and the development of a predictive model using a Random Forest Regressor.

## Dataset

### About the Dataset

Craigslist is the world's largest collection of used vehicles for sale, yet compiling all entries into a single dataset poses significant challenges. To address this, a scraper was developed initially for a school project and later expanded to create a comprehensive dataset. This dataset includes every used vehicle entry within the United States on Craigslist, scraped periodically to ensure up-to-date information.

**Key Features of the Dataset:**
- **Price:** Listing price of the vehicle.
- **Condition:** Overall condition of the vehicle (e.g., new, like new, good).
- **Manufacturer & Model:** Brand and specific model of the vehicle.
- **Odometer:** Mileage of the vehicle.
- **Location:** Latitude and longitude coordinates.
- **Additional Attributes:** Includes 18 other categories such as fuel type, transmission, drive type, etc.

### Dataset Link

Access the dataset on [Kaggle](https://www.kaggle.com/datasets/austinreese/craigslist-carstrucks-data/data).

## Notebooks

### 1. Data Preprocessing & Cleaning

`Data_Preprocessing_Cleaning.ipynb`

**Overview:**
- **Data Loading:** Importing the raw dataset.
- **Data Cleaning:**
  - Handling missing values
  - Removing duplicates
  - Correcting data types
- **Drop Redundant Columns:** Removing columns that do not contribute to the prediction task.
- **Filter by Year:** Keeping entries of vehicles manufactured after 1990 to ensure relevance and data quality.
- **Remove Outliers:** Eliminating extreme values in `price` and `odometer` to reduce noise and improve model performance.
- **Predictive Imputation for Manufacturer:** Using a Random Forest Classifier to predict and impute missing `manufacturer` values.
- **Saving Cleaned Data:** Exporting the cleaned dataset for subsequent analysis.

### 2. Exploratory Data Analysis & Predictive Modeling

`EDA_and_Predictive_Modeling.ipynb`

**Overview:**
- **Exploratory Data Analysis (EDA):** Visualizing and understanding the distribution of variables and relationships between them.
- **Correlation Analysis:** Identifying key predictors of car prices.
- **Model Training:** Developing a Random Forest Regressor to predict car prices.
- **Model Evaluation:** Assessing model performance using RMSE and R² metrics.
- **Feature Importance:** Determining the most influential features in the prediction model.

## Key Features

- **Year:** Manufacturing year of the vehicle.
- **Odometer:** Mileage on the vehicle.
- **Cylinders:** Number of engine cylinders.
- **Fuel:** Type of fuel the vehicle uses.
- **Model:** Specific model of the vehicle.
- **Drive:** Drive type (e.g., FWD, RWD, AWD).
- **Manufacturer:** Brand of the vehicle.

## Model Performance

**Random Forest Regressor:**
- **RMSE:** \$5,362.24
- **R² Score:** 0.8699

**Top 7 Important Features:**
1. **Year**
2. **Odometer**
3. **Cylinders**
4. **Fuel**
5. **Model**
6. **Drive**
7. **Manufacturer**

**Analysis:**
The Random Forest model demonstrates strong predictive capabilities with an R² score of **0.8699**, indicating that approximately **86.99%** of the variance in used car prices is explained by the model. The RMSE of **\$5,362.24** suggests that the model's predictions are, on average, off by this amount. The top features align with industry insights, emphasizing the importance of a vehicle's age, mileage, engine specifications, and brand in determining its price.
