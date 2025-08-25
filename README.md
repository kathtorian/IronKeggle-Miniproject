

# 🏡 Real Estate Price Analysis – Ironhack Kaggle Project
## Project Overview

This project is part of the **Ironhack Data Science & Machine Learning Bootcamp** and follows a Kaggle-style competition format. The dataset covers house sales in King County, Washington (including Seattle) between May 2014 and May 2015.

The primary objective is to **__analyze housing prices and identify the key factors that influence them__**, with a special focus on properties priced above $650,000. Beyond exploratory analysis, we also apply machine learning models to predict housing prices more accurately.

## 📂 Repository Structure
## 📂 Repository Structure

```bash
.
├── Mini_Project.ipynb                          # Jupyter notebook with full analysis and code
├── data/                                       # Raw and processed datasets
├── images/                                     # Visualizations exported from notebook
├── IronKeggle - Project Presentation.pdf       # Project presentation
└── README.md                                   # Project documentation
```


## 🎯 Objectives

- Perform **Exploratory Data Analysis** (EDA) to understand property characteristics.

- Engineer new, more meaningful features (e.g., house age, renovation flag, price per m²).

- **Identify key drivers** of housing prices (size, rooms, location, etc.).

- Handle missing values, duplicates, and outliers. Detect and handle outliers, missing values, and categorical variables.

- Build and tune **machine learning models for price prediction**. 

- Communicate insights through data visualization and clear reporting.

- Interpret and rank feature importance to highlight the most influential property characteristics.


## 📊 Analysis & Data Processing

#### Dataset Understanding

- Categorical vs. numerical feature classification.
- Converted yr_built → age and yr_renovated → renovated (binary).
- Converted date to datetime type for temporal analysis.

#### Feature Engineering

- Added age of the property.
- Created renovation flag.
- Built geolocation clusters using KMeans on latitude and longitude.
- Generated price per square meter for relative valuation.

#### Data Cleaning

- Removed outliers using IQR filtering.
- Handled categorical variables:
        - Ordinal → treated as ordered (e.g., condition, grade).
        - Nominal → one-hot encoded.
- Normalized continuous features with RobustScaler.
- Applied log transformation to target (price) to reduce skew.

#### Exploratory Insights

- Larger living area strongly correlates with higher price.

- Location (lat/long clusters) is a key driver of housing values.

- Renovated properties and higher-grade houses sell for a significant premium.

- Price distribution is right-skewed, requiring transformation.


## Modeling
- Baseline models tested.

- XGBoost Regressor with hyperparameter tuning via GridSearchCV (5-fold CV) provided the best balance of accuracy and generalization.

- Feature importance analysis showed:

        - Location (lat, long, and cluster feature) as the strongest driver.
        - Size (sqft_living, sqft_lot, sqft_living15) as major contributors.
        - Age, bathrooms, bedrooms, and grade also highly influential.
        - Renovation status positively impacts predicted price.

- Discussion of predictive power and limitations.


## 🔑 Key Insights
- **Location matters most**: longitude, latitude, and neighborhood clusters dominate the model.

- House size (living area, lot size, nearby house sizes) is a critical factor in pricing.

- Renovations & age influence property value significantly.

- Feature engineering (clusters, age, log-price) improved model robustness and reduced reliance on a single dominant feature.


## 🚀 Next Steps
- Add **external datasets** (schools, crime rate, amenities) for richer context.
- Experiment with ensemble methods (Stacking, LightGBM, CatBoost).
- Improve predictive models and try new ones.
- Deploy a streamlit app or dashboard for interactive price prediction.
- Perform geospatial visualization to highlight neighborhood trends.

## 🛠️ Tech Stack
Python 🐍
Pandas, NumPy
Matplotlib, Seaborn
Scikit-learn
XGBoost


## 👩‍💻 Author
Hi, I’m Katherine! 👋  
I’m currently completing the **Ironhack Data Science Bootcamp** and building projects in Machine Learning & Data Analysis.  
My long-term goal is to become a **Machine Learning Engineer** and specialize in real estate and financial applications of AI.  

📧 Contact me: pktorian@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/katherine-torian) | [GitHub](https://github.com/kathtorian)
