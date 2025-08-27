# Algerian Forest Fires Prediction

## Project Description

This project provides a comprehensive analysis and machine learning approach to predict forest fires in Algeria. It uses meteorological and FWI (Fire Weather Index) data from two distinct regions, Bejaia and Sidi Bel-abbes, collected between June and September 2012. The project's goal is to perform a detailed exploratory data analysis (EDA) and develop robust regression and classification models to predict the occurrence of forest fires.

---

## Table of Contents

- [Dataset Overview](#Dataset-Overview)
- [Exploratory Data Analysis (EDA)](https://www.google.com/search?q=%23exploratory-data-analysis-eda)
- [Machine Learning Models](https://www.google.com/search?q=%23machine-learning-models)
- [Project Structure](https://www.google.com/search?q=%23project-structure)
- [Dependencies](https://www.google.com/search?q=%23dependencies)
- [Usage](https://www.google.com/search?q=%23usage)

---

## Dataset Overview

The dataset, sourced from Kaggle, contains 244 instances (122 for each region) and 12 attributes. Key features include:

- **Date**: Day, month, and year (2012).
- **Temperature (Temp)**: Maximum daily temperature in Celsius.
- **Relative Humidity (RH)**: Daily humidity percentage.
- **Wind Speed (Ws)**: Daily wind speed in km/h.
- **Rain**: Total daily rainfall in mm.
- **FWI Components**: A set of components from the Fire Weather Index system (`FFMC`, `DMC`, `DC`, `ISI`, `BUI`, `FWI`).
- **Classes**: The target variable, which is a categorical label indicating `'fire'` or `'not fire'`.

The dataset has been pre-processed to handle missing values and prepare it for analysis and modeling.

---

## Exploratory Data Analysis (EDA)

The `Algerian_forest_fires_EDA.ipynb` notebook provides a detailed analysis of the dataset. The key steps and findings include:

1. **Data Cleaning**: The initial dataset contains text headers and inconsistent data types, which were cleaned to ensure numerical values were correctly interpreted.
2. **Missing Value Handling**: The dataset was checked for missing values, and appropriate strategies were used to handle any discrepancies.
3. **Visualizations**: Visualizations were created to understand the distribution of features and the relationship between variables.
4. **Key Findings**:
    - The highest number of forest fires occurred in **August and September** for both regions.
    - The **Bejaia region** showed a slightly higher fire count compared to the Sidi Bel-abbes region.
    - Meteorological factors like temperature, humidity, and rainfall show distinct patterns for fire and non-fire days.

---

## Machine Learning Models

The `Ridge_Lasso_ElasticNet_Model.ipynb` notebook focuses on building and evaluating regression models.

- **Objective**: The primary goal is to predict the **Fire Weather Index (FWI)**, which is a key indicator of fire potential. The models also aim to classify instances into `'fire'` or `'not fire'`.
- **Models Used**:
    - **Ridge Regression**: A linear regression model with L2 regularization to prevent overfitting by penalizing large coefficients.
    - **Lasso Regression**: A linear regression model with L1 regularization that can perform feature selection by shrinking some coefficients to zero.
    - **ElasticNet Regression**: A hybrid model that combines L1 and L2 regularization, making it effective for handling correlated features.
- **Pre-processing for Modeling**: The cleaned dataset from the EDA phase was used. Categorical variables, such as `Classes`, were encoded into numerical format. Unnecessary columns like `day`, `month`, and `year` were dropped for model training.

---

## Project Structure

- `Algerian_forest_fires_dataset_UPDATE.csv`: The raw, initial dataset.
- `Algerian_forest_fires_cleaned_dataset.csv`: The cleaned and pre-processed dataset, ready for model training.
- `Algerian_forest_fires_EDA.ipynb`: Jupyter Notebook with the EDA process, data cleaning, and visualizations.
- `Ridge_Lasso_ElasticNet_Model.ipynb`: Jupyter Notebook with the machine learning model building, training, and evaluation.

---

## Dependencies

This project requires Python 3.x and the following libraries. You can install them using `pip`:

```python
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## Usage

1. Clone the repository to your local machine.
2. Ensure you have the required dependencies installed.
3. Open the Jupyter Notebooks in your preferred environment (e.g., Jupyter, VS Code).
4. Run the cells in **`Algerian_forest_fires_EDA.ipynb`** first to perform data cleaning and analysis.
5. Then, run the cells in **`Ridge_Lasso_ElasticNet_Model.ipynb`** to train and evaluate the machine learning models.

---

## Contributing

Contributions are welcome! If you have any suggestions or improvements, please feel free to open an issue or submit a pull request.
