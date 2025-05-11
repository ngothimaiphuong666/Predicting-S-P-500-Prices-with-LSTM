# Predicting-S-P-500-Prices-with-LSTM
This project is part of an extended exercise to explore time-series forecasting using deep learning. The goal is to predict the daily closing prices of the S&amp;P 500 index using an LSTM (Long Short-Term Memory) model built with PyTorch.
📂 Project Overview

Objective: Predict the next-day S&P 500 closing price using the last 5 days of historical prices.
Dataset: 10 years of S&P 500 daily data (2014–2024), including columns such as Date, Price, Open, High, Low, Vol., and Change %.
Tools & Frameworks: Python, PyTorch, Pandas, NumPy, Matplotlib
🧠 Model Development

Started with a basic nn.Linear model to test baseline performance:
MAE (Test): $190.10
RMSE (Test): $268.87
Improved the model significantly by switching to an LSTM:
MAE (Test): $131.75
RMSE (Test): $178.22
🛠️ Key Steps

Data Preprocessing
Loaded CSV file (S&P 500 Daily.csv)
Cleaned missing values, converted dates, and normalized prices
Created sliding windows of 5 days → 1 day prediction
Model Training
Built and trained a PyTorch-based LSTM model
Used MSE (Mean Squared Error) loss and Adam optimizer
Trained for 300+ epochs with decreasing loss
Evaluation
Evaluated on unseen test data
Plotted predicted vs actual prices
Observed solid trend capture with minor deviations
📊 Results

The model captures general trends of S&P 500 movements. While some volatility remains hard to predict, performance is significantly better than the linear model.

Final Test Results:

MAE: $131.75
RMSE: $178.22
📌 Future Improvements

Add technical indicators (e.g., Moving Averages, RSI)
Train on longer sequences (e.g., 10–20 days)
Experiment with stacked LSTM layers or GRU
Apply to other stock indices or ETFs
🚀 Getting Started

This project is built in Google Colab. To run it:

Upload your S&P 500 Daily.csv file
Run the provided code cells
Visualize predictions and model performance
🔗 Author

Developed by Ngo Thi Mai Phuong as part of an academic and professional upskilling journey in financial data science and AI.
