# linear-Regression-from-scratch
Energy Consumption Prediction using Linear Regression
This project is a practical implementation of Linear Regression algorithms built completely from scratch (without relying on high-level machine learning libraries like Scikit-Learn). The goal is to predict "Energy Consumption" based on various environmental and structural factors using the Gradient Descent optimization algorithm.

📌 Project Overview
The script reads data from assignment1dataset.csv, preprocesses it, and trains both Simple Linear Regression and Multiple Linear Regression models. Furthermore, the project conducts hyperparameter tuning by testing different Learning Rates and Epochs to achieve optimal model performance, evaluating the results using Mean Squared Error (MSE).

🛠️ Requirements and Dependencies
To run this code, you will need a Python environment with the following libraries installed:

pandas: For reading and manipulating the dataset.

numpy: For numerical operations and matrix calculations.

matplotlib: For plotting graphs and visualizing the results.

📊 Dataset Details
The models use the following independent variables (Features) to make predictions:

Square Footage

Number of Occupants

Appliances Used

Average Temperature

Target Variable: Energy Consumption

🧠 Evaluated Models
The experiment is divided into 6 different models to compare their performance:

M1: Simple Linear Regression using (Square Footage) only.

M2: Simple Linear Regression using (Number of Occupants) only.

M3: Simple Linear Regression using (Appliances Used) only.

M4: Simple Linear Regression using (Average Temperature) only.

M5: Multiple Linear Regression using All 4 Features.

M6: Multiple Linear Regression using (Square Footage, Number of Occupants).

⚙️ Methodology
Data Normalization: Z-score normalization is applied to standardize the data (Mean = 0, Standard Deviation = 1). This ensures that the Gradient Descent algorithm converges faster and remains stable.

Custom Algorithm: A custom linear_regression function is built to manually update weights (m) and bias (c) iteratively.

Hyperparameter Tuning:

Phase 1: Fixing the epochs at 5000 and testing various learning rates: [0.00001, 0.0001, 0.001, 0.01, 0.05, 0.1].

Phase 2: Fixing the learning rate at the best performing value (0.01) and testing different epoch counts: [10, 100, 1000, 10000, 50000].

📈 Results and Conclusion
Based on the generated plots and MSE calculations, the project concludes the following:

Best Learning Rate: 0.01

Best Epochs: 1000

Best Single Feature: The script dynamically identifies and prints the best individual feature that yields the lowest error in the simple regression models.

Best Overall Model: M5 (which incorporates all four features) achieves the lowest Mean Squared Error (MSE), making it the most accurate model for predicting energy consumption.

🚀 How to Run
Ensure the dataset file assignment1dataset.csv is placed in the same directory as the Python script.

Run the script in your local Python environment or on Google Colab.

The script will train the models, print the MSE values for each trial to the console, and generate two sets of subplots demonstrating the relationship between (MSE vs. Learning Rate) and (MSE vs. Epochs).
