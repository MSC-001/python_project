# Crop Yield Prediction Project

This project focuses on analyzing a dataset of crop yields to understand the factors that influence them and to build a predictive model. The entire process, from data cleaning to model building, is documented in the `project_code.ipynb` notebook.

## Datasets

Two datasets are used in this project:

- `crop_yield[MissingValues&Duplicates].csv`: The raw dataset containing missing values and duplicate entries.
- `crop_yield[Cleaned].csv`: A cleaned version of the raw dataset, generated after the data cleaning process.

## Methodology

The project follows a structured approach to analyze the data and build a predictive model:

### 1. Data Loading and Exploration

- The raw dataset is loaded into a pandas DataFrame.
- Initial exploration is performed to understand the data's structure, including its shape, columns, and data types.

### 2. Data Cleaning

- **Missing Values**: The dataset is checked for missing values, which are then handled by dropping the respective rows.
- **Duplicates**: Duplicate rows are identified and removed to ensure data integrity.
- The cleaned data is saved as `crop_yield[Cleaned].csv`.

### 3. Outlier Detection and Handling

- Outliers in the numerical columns are detected using the Interquartile Range (IQR) method.
- These outliers are then removed to improve the accuracy and robustness of the model.

### 4. Exploratory Data Analysis (EDA)

- **Univariate Analysis**: The distribution of the target variable, `Crop Yield (kg per hectare)`, is analyzed.
- **Bivariate Analysis**: The relationship between `rainfall` and `Crop Yield` is explored.
- **Multivariate Analysis**: A correlation matrix is used to examine the relationships between different numerical features like Nitrogen (N), Phosphorus (P), and Potassium (K) levels, and crop yield.

### 5. Predictive Modeling

- A **Random Forest Regressor** is used to build a model that predicts crop yield.
- The data is split into training and testing sets to evaluate the model's performance.
- The model is trained on the training data and then used to make predictions on the test data.

## Results

- The Random Forest model achieved an **R² score of approximately 0.93**, indicating that it can explain a large portion of the variance in crop yield.
- The most important features for predicting crop yield were found to be `temperature`, `K` (Potassium), and `humidity`.

## How to Run

To replicate this analysis, you can run the `project_code.ipynb` notebook in a Jupyter environment. Ensure you have the required dependencies installed.

## Dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn
