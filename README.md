# smart-home-electricity-forecasting-lstm
## Deep learning project for household electricity consumption forecasting using LSTM networks
## Overview

This project focuses on forecasting household electricity consumption using Long Short-Term Memory (LSTM) networks on time-series power consumption data. The objective is to predict future electricity usage patterns using historical smart home energy consumption data.

The project applies deep learning techniques to analyze minute-level electricity readings and generate accurate short-term power consumption forecasts. Such forecasting systems can help improve energy management, reduce electricity wastage, and support smart grid optimization.

## Problem Statement

Accurate electricity consumption forecasting is important for efficient energy management in smart homes and smart grids. Traditional machine learning models often struggle to capture long-term temporal dependencies in sequential power consumption data.

This project uses LSTM neural networks, which are specifically designed for time-series forecasting, to predict future household electricity consumption based on historical usage patterns.

## Dataset
Dataset: Individual Household Electric Power Consumption Dataset
Source: UCI Machine Learning Repository / Kaggle
Records: Approximately 2,075,259 minute-level observations
Time Period: December 2006 – November 2010

## Features Used
Global_active_power (Target Variable)
Global_reactive_power
Voltage
Global_intensity
Sub_metering_1
Sub_metering_2
Sub_metering_3

## Data Preprocessing

The following preprocessing steps were performed before training the model:

Replaced missing values (?) with NaN
Converted numerical columns to float data types
Combined Date and Time columns into a DateTime index
Applied MinMaxScaler normalization
Created sliding window sequences for supervised learning
Split data into training and testing sets using time-based splitting

## Model Architecture

Multiple LSTM architectures were experimented with to improve forecasting performance.

## Baseline Model
LSTM(64)
Dense(1)
Improved Model
LSTM(64, return_sequences=True)
Dropout(0.2)
LSTM(64)
Dense(1)
Training Configuration
Optimizer: Adam
Loss Function: Mean Squared Error (MSE)
Evaluation Metrics
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
Training Parameters
Batch Size: 64
Epochs: 30
Train-Test Split: 80:20
Validation Split: 10%

## Results

The LSTM model successfully captured temporal electricity consumption patterns and produced accurate short-term forecasts.

## Key Findings
Longer input window sizes improved prediction accuracy
Stacked LSTM architecture performed better than the baseline model
Dropout regularization reduced overfitting
The model achieved strong forecasting performance based on MAE and RMSE evaluation metrics

## Technologies Used
Python
TensorFlow 
Pandas
NumPy
Matplotlib
Scikit-learn

## Applications
Smart home energy management
Electricity demand forecasting
Smart grid optimization
Energy consumption monitoring
Predictive analytics for IoT systems

## Future Improvements
Experiment with GRU and Transformer-based models
Hyperparameter optimization using GridSearch
Real-time forecasting dashboard using Streamlit
Multi-step future forecasting
Deployment using Flask API or cloud platforms
