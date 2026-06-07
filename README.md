# Property Price Prediction using Linear Regression

## Project Overview

This project aims to predict median house values in California districts using demographic, geographic, and housing-related features. The objective is to build and compare **Simple Linear Regression** and **Multiple Linear Regression** models to determine which approach provides better predictive performance while maintaining interpretability.

## Dataset Information

The dataset contains district-level housing information with the following features:

| Feature            | Description                   |
| ------------------ | ----------------------------- |
| longitude          | Longitude of the district     |
| latitude           | Latitude of the district      |
| housing_median_age | Median age of houses          |
| total_rooms        | Total number of rooms         |
| total_bedrooms     | Total number of bedrooms      |
| population         | Population of the district    |
| households         | Number of households          |
| median_income      | Median income of residents    |
| ocean_proximity    | Proximity to the ocean        |
| median_house_value | Target variable (house price) |

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

* Dataset inspection and summary statistics
* Missing value analysis
* Distribution analysis using histograms
* Correlation analysis using heatmaps
* Outlier detection using boxplots
* Feature relationship exploration using pairplots

### 2. Data Preprocessing

* Handled missing values in `total_bedrooms` using median imputation
* Encoded categorical feature `ocean_proximity` using one-hot encoding
* Split data into training and testing sets

### 3. Model Development

#### Simple Linear Regression

* Feature Used: `median_income`
* Target: `median_house_value`

#### Multiple Linear Regression

* Utilized all available predictor variables
* Included encoded ocean proximity features

### 4. Model Evaluation

The models were evaluated using:

* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)
* R² Score (Coefficient of Determination)

## Results

| Model                      | R² Score |
| -------------------------- | -------- |
| Simple Linear Regression   | 0.4589   |
| Multiple Linear Regression | 0.6254   |

### Key Findings

* Median income is the strongest individual predictor of house prices.
* Multiple Linear Regression significantly outperforms Simple Linear Regression.
* Geographic and ocean proximity features contribute meaningfully to prediction accuracy.
* The Multiple Linear Regression model explains approximately 62.5% of the variance in house prices.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook

## Installation

Clone the repository:

```bash
git clone [https://github.com/Manasveejain/Property-Price-Prediction]
```

Install dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

Run the Jupyter Notebook:

```bash
jupyter notebook
```

## Project Structure

```text
├── data/
│   └── housing.csv
├── notebooks/
│   └── Property Price Prediction.ipynb
├── images/
│   └── visualizations
├── README.md
```

## Conclusion

The project demonstrates how regression techniques can be applied to real-world housing data. While Simple Linear Regression provides an interpretable baseline model, Multiple Linear Regression delivers substantially better predictive performance and is selected as the final model for house price prediction.
