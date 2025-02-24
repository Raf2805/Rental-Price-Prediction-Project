# Rental-Price-Prediction-Project


## Overview

This project aims to predict the monthly rental prices of properties using a variety of engineered features and regression models. We leverage numerical, categorical, and geographic data to build and compare multiple models, including Linear Regression, Ridge Regression, and Random Forest. Based on extensive evaluation metrics, the Random Forest model was selected as our final model for its superior performance.

## Project Structure

- **Data Loading and Cleaning:**  
  The dataset, `rentfaster.csv`, is loaded and cleaned by converting key variables to numeric types, extracting meaningful features, and handling missing values.

- **Feature Engineering:**  
  We create several new features to enhance model performance:
  - **Price per Square Foot:** Calculated as $$\\frac{price}{sq\\_feet}$$ to normalize property prices by their size.
  - **Total Rooms:** The sum of bedrooms and bathrooms, computed as $$beds + baths$$.
  - **Bath-to-Bed Ratio:** The ratio of bathrooms to bedrooms, defined as $$\\frac{baths}{beds}$$ (with appropriate handling when beds equals 0).
  - **Pet Friendly Indicator:** A binary feature derived by combining the pet policies for cats and dogs.
  - **Distance to Calgary:** Calculated using the latitude and longitude of the property, this feature quantifies the property's proximity to Calgary.

- **Model Development and Evaluation:**  
  The following models are built and compared:
  - **Linear Regression**
  - **Ridge Regression**
  - **Random Forest Regressor**
  
  A 5-fold cross-validation strategy is used, and additional evaluation metrics (MAE, MAPE, RMSE) are computed to assess model performance.

- **Final Model Selection:**  
  Based on higher R² scores and lower error metrics, the Random Forest model was chosen due to:
  - Its ability to capture complex, nonlinear relationships.
  - Lower Mean Absolute Error, Mean Absolute Percentage Error, and Root Mean Squared Error.
  - Consistent performance across cross-validation folds.

- **Prediction Demonstration:**  
  A sample property prediction is demonstrated with a detailed explanation of the inputs and resulting prediction, showcasing the practical utility of the model.

## How to Run the Project

1. **Dependencies:**  
   Ensure that you have the following Python libraries installed:
   - `pandas`
   - `numpy`
   - `scikit-learn`
   - `seaborn`
   - `matplotlib`

2. **Data:**  
   Place the dataset `rentfaster.csv` in the project directory.

3. **Execution:**  
   - Open the Jupyter Notebook provided.
   - Run the cells sequentially, starting with data loading, followed by cleaning, feature engineering, model training, evaluation, and prediction.

4. **Results and Analysis:**  
   Review the outputs directly in the notebook:
   - Data cleaning steps are justified and explained.
   - Model comparison outputs, including cross-validation scores and extended metrics.
   - A thorough justification for choosing the Random Forest model is provided.



## Conclusion

This project demonstrates an end-to-end machine learning workflow for rental price prediction. By incorporating systematic data cleaning, robust feature engineering, and comprehensive model evaluations, we provide a reliable and interpretable solution for predicting rental prices.
