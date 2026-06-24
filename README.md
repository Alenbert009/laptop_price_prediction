# 💻 Laptop Price Prediction System

An end-to-end Machine Learning project that predicts the market price of a laptop based on its hardware specifications and brand. This project features a comprehensive Exploratory Data Analysis (EDA), extensive benchmarking of 10 different regression algorithms, and a user-friendly Streamlit web application for real-time predictions.

### 🌐 Live Demo
**Check out the live web application here:** [Laptop Price Prediction App](https://laptoppriceprediction-sujoy.streamlit.app/)

---

## 🎯 Project Overview

The laptop market is highly saturated with varying configurations, making it difficult for consumers to gauge fair pricing. This project solves that problem by leveraging machine learning to predict laptop prices based on key features like RAM, CPU, GPU, Weight, and Screen Resolution. 

The project rigorously evaluated multiple models to find the most accurate predictor, ultimately deploying an **XGBoost Regressor** to power the backend of the interactive web app.

---

## ✨ Key Highlights & Features

* **Comprehensive EDA:** Uncovered hidden trends in the data through detailed visualizations, including:
  * *Price vs. Operating System* trends.
  * *Weight vs. Density* and *Weight vs. Price* correlations.
  * The impact of premium features (Touchscreen, IPS panels) on overall cost.
* **Extensive Model Benchmarking:** Built, tuned, and compared 10 different machine learning algorithms to ensure maximum predictive accuracy.
* **Interactive UI:** A clean, intuitive Streamlit frontend allowing users to input custom configurations and instantly receive a predicted price in INR (₹).

---

## 🧠 Methodology & Machine Learning Pipeline

### 1. Data Analysis & Preprocessing
* Cleaned and formatted raw data (e.g., extracting numeric values from RAM and Memory columns).
* Engineered new features such as PPI (Pixels Per Inch) from Screen Resolution.
* Handled categorical variables (Brand, CPU Type, GPU Brand, OS) using techniques like One-Hot Encoding and Target Encoding.

### 2. Model Selection & Benchmarking
To find the best performing model, the following algorithms were tested:
* Linear Regression
* Ridge & Lasso Regression
* K-Nearest Neighbors (KNN)
* Decision Tree
* Support Vector Regressor (SVR)
* Random Forest
* Gradient Boosting & AdaBoost
* **XGBoost (Selected Champion Model)**

*XGBoost was chosen as the final model due to its superior capability in handling complex, non-linear relationships and delivering the lowest prediction error.*

### 3. Deployment
* Exported the trained XGBoost model and data transformation pipelines using `pickle`.
* Built an interactive frontend using `Streamlit` (`app.py`) to accept user inputs and display predictions dynamically.

---

## 📂 Repository Structure

```text
├── app.py                 # Streamlit application script for the frontend
├── laptop_price_eda.ipynb # Jupyter Notebook containing Data Cleaning, EDA, and Model Training
├── xgb_model.pkl          # Serialized XGBoost regression model
├── pipeline.pkl           # Serialized data preprocessing pipeline
├── requirements.txt       # Python dependencies required to run the project
└── README.md              # Project documentation
