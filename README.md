## **Project Overview**

This project involves developing an Artificial Neural Network (ANN) model to predict the density and excess molar volume (VE) of a monoethanolamine-methanol binary mixture based on temperature and an additional feature. The dataset includes measurements of density and excess molar volume at various temperatures. The objective is to build a predictive model that can estimate these properties accurately. The project encompasses data preprocessing, exploratory data analysis (EDA), model development, and evaluation, with results saved for further analysis.

---

## **Introduction**

Monoethanolamine (MEA) and methanol (MeOH) are used in various industrial applications, including gas treatment. Understanding the physicochemical properties of their mixtures, such as density and excess molar volume, is crucial for optimizing processes. This project focuses on predicting these properties using machine learning techniques, specifically an Artificial Neural Network (ANN). By leveraging temperature and a feature 'x1', the goal is to provide accurate predictions of density and excess molar volume, which are essential for designing and improving industrial processes.

---

## **Dataset Description**

The dataset used in this project consists of measurements related to the monoethanolamine-methanol binary mixture. It includes the following columns:

- **Temperature (T)**: The temperature at which measurements were taken, in Kelvin.
- **Feature x1**: An additional feature relevant to the mixture.
- **Density (d)**: The density of the mixture, measured in g/cm³.
- **Excess Molar Volume (VE)**: The excess molar volume of the mixture, measured in cm³/mol.

The data is provided in an Excel file (`density16.xlsx`), which includes various temperature and composition scenarios.

---

## **Data Preprocessing**

1. **Loading Data**: The dataset is loaded from an Excel file using Pandas.
2. **Feature Engineering**:
   - A constant temperature feature `T` is added.
   - The `VE` and `density` columns are cleaned and transformed for consistency.
3. **Scaling**:
   - The features `x1` and `T` are standardized.
   - The target variables (density and excess molar volume) are also standardized to ensure better model performance.

---

## **Exploratory Data Analysis (EDA)**

EDA is performed to understand the dataset and visualize relationships:

1. **Descriptive Statistics**: Calculate summary statistics to understand data distribution.
2. **Visualization**:
   - **Temperature vs. Density and VE**: Scatter plots to observe how density and excess molar volume vary with temperature.
   - **Distribution Plots**: Histograms to view the distribution of density and excess molar volume.

---

## **Model**

1. **Model Architecture**:
   - **Input Layer**: Takes scaled features `x1` and `T`.
   - **Hidden Layers**: Multiple dense layers with ReLU activation functions.
   - **Output Layer**: Predicts density and excess molar volume.

2. **Loss Function**:
   - Custom RMSE (Root Mean Squared Error) loss function is used to train the model.

3. **Training**:
   - The model is trained with scaled data for 200 epochs with a batch size of 64.
   - A validation split is used to monitor overfitting.

---

## **Evaluation**

1. **Predictions**:
   - The model’s predictions are scaled back to the original range using inverse transformation.
   
2. **Error Metrics**:
   - **Mean Absolute Percentage Error (MAPE)**: Calculated for both density and excess molar volume to evaluate model accuracy.

3. **Results**:
   - A comparison of actual vs. predicted values is saved in an Excel file for review.
   - Training and validation RMSE are visualized in plots to understand model performance over epochs.

---

## **Results**

1. **Comparison DataFrame**: Contains actual and predicted values for density and excess molar volume.
2. **Plots**:
   - **Training and Validation RMSE Plot**: Shows the convergence of the model and performance over epochs.

![download (3)](https://github.com/user-attachments/assets/0c3732c6-c62f-46eb-ad90-a90d134a4754)

![download (4)](https://github.com/user-attachments/assets/d76d0222-9aa4-4272-af64-9380b211544b)

![download (5)](https://github.com/user-attachments/assets/3e7bc5ba-8720-4a8b-a86d-9cc2e8c40401)

3. **Saved Results**:
   - Comparison results are saved to an Excel file (`comparison_results.xlsx`).

---

## **Usage**

1. **Dependencies**: Ensure you have the necessary libraries installed: Pandas, NumPy, TensorFlow, scikit-learn, Matplotlib.
2. **Running the Project**:
   - Load the dataset.
   - Perform data preprocessing.
   - Train the model and evaluate results.
   - Visualize performance metrics.
