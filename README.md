# Overview
This project aims to predict house prices in Bangalore using machine learning techniques. By analyzing real estate data, the model helps users estimate property prices based on features such as location, square footage, number of bedrooms, and bathrooms. The approach involves data preprocessing, feature engineering, model selection, training, evaluation, and deployment to ensure accurate and interpretable predictions.

## Methodology
1. Data Collection
    The dataset used is the Bengaluru House Prices dataset.
    Key attributes include area type, location, size, total square feet, number of bathrooms, and price.

2. Data Preprocessing
    Data Cleaning
    Removed unnecessary columns (area_type, society, balcony, availability).
    Handled missing values using dropna() to remove incomplete records.
    Feature Extraction
    Extracted BHK (number of bedrooms) from the size column.
    Converted non-numeric total_sqft values (e.g., ranges like 800 - 1000) into numerical form by averaging.
    Outlier Removal
    Eliminated properties with extremely small area per BHK (<300 sqft).
    Removed extreme price-per-square-foot outliers using mean and standard deviation filtering for each location.

3. Exploratory Data Analysis (EDA)
    Used scatter plots to visualize relationships between BHK, square footage, and price.
    Analyzed price-per-square-foot distributions using histograms.
    Identified trends and outliers for further data cleaning.

4. Feature Engineering
    Created a new feature: price_per_sqft for better price standardization.
    Simplified location categories by grouping rare locations into an "Other" category.
    Applied one-hot encoding to convert categorical features into numerical form.

5. Model Building
    Split the dataset into training and testing sets using train_test_split().
  Tested multiple models:
    Linear Regression
    Lasso Regression
    Decision Tree Regressor
    Used GridSearchCV for hyperparameter tuning and model selection.

6. Model Evaluation
    Measured model performance using:
    R-squared (R²) Score to assess fit quality.
    Cross-validation to ensure model robustness.

7. Prediction
    Developed a function to predict house prices based on:
    Location
    Square footage
    Number of bedrooms (BHK)
    Number of bathrooms

8. Model Deployment
    The final trained model was saved using Pickle for future use.
    A JSON file containing feature names was generated for seamless inference.
    Technologies Used
    Programming & Tools
    Python (Data processing & modeling)

#### Libraries:
    Pandas & NumPy (Data manipulation)
    Matplotlib & Seaborn (Data visualization)
    Scikit-learn (Machine learning algorithms)
    Pickle (Model persistence)

#### Installation & Usage:
    Prerequisites
    Python 3.12.6
    Jupyter Notebook (optional)

# Output

![WhatsApp Image 2025-03-30 at 15 11 14_28024b4c](https://github.com/user-attachments/assets/f7906824-c2c9-4776-9792-8afc5e98843c)

