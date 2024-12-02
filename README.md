# Anomaly Detection in Stock Market Data Using Unsupervised Machine Learning

## Project Description
This project focuses on detecting anomalies in financial market data using unsupervised machine learning techniques. By identifying unusual trading patterns, the system aims to uncover potential market manipulation, fraudulent activities, or significant economic events. The analysis is conducted on historical stock market data to evaluate the effectiveness of multiple unsupervised learning models.

## Project Objectives
- **Develop** and compare unsupervised machine learning models to detect anomalies in stock market data.
- **Validate** anomalies using statistical methods and correlate them with historical market events.
- **Enhance** insights into market behavior through robust visualizations and analysis.

## Folder Structure

- **data/**: Contains all data files.
  - **raw/**: Original dataset files (e.g., `data.csv`).
  - **processed/**: Cleaned and preprocessed dataset files for model input (e.g., `cleaned_data.csv`).
- **notebooks/**: Jupyter notebooks for data exploration and model development.
  - `exploratory_data_analysis.ipynb`: Notebook for dataset exploration and feature engineering.
  - `model_training.ipynb`: Notebook for model training, evaluation, and results visualization.
- **reports/figures/**: Visualizations generated during analysis, including:
  - Anomaly detection results.
  - PCA plots of anomalies vs. normal data.
  - Kernel Density Estimation (KDE) plots for feature distributions.
  - Temporal distribution of anomalies and correlations with historical events.
- **README.md**: Overview and instructions for the project.

## Data Source

The dataset contains stock market data collected from [nasdaq.com](https://www.nasdaq.com) through web scraping. It includes daily stock prices, trading volumes, and related metrics for leading companies.

- **Dataset Details**:
  - **Total Rows**: 25,161.
  - **Time Span**: 2013–2023.
  - **Companies Included**: Apple, Starbucks, Microsoft, Cisco Systems, Qualcomm, Meta, Amazon.com, Tesla, Advanced Micro Devices, and Netflix.
  - **Features**:
    - Stock prices and trading volumes.
    - Adjusted Close Change, Volume Change, Price Range, and Daily Price Change.

## Implemented Models

1. **Isolation Forest (IF)**:
   - Detects anomalies by isolating data points with unique characteristics.
   - Effective for identifying global outliers.

2. **Local Outlier Factor (LOF)**:
   - Identifies anomalies based on density variations among neighboring points.

3. **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)**:
   - Clusters data points and labels noise as anomalies.
   - Parameters tuned using the k-distance graph.

4. **Ensemble Model**:
   - Combines results from Isolation Forest, LOF, and DBSCAN to enhance robustness.

## Visualizations

- **PCA Plots**:
  - Highlights the separation of anomalies from normal data.
- **KDE Plots**:
  - Visualizes feature distributions for anomalies vs. normal data.
- **Yearly and Monthly Anomalies**:
  - Tracks the temporal distribution of anomalies.
- **Anomalies on Duplicate Dates**:
  - Links detected anomalies to specific historical market events.

## Key Findings

- **Anomalies Detected**:
  - Isolation Forest and LOF: 252 anomalies each.
  - DBSCAN: 461 anomalies.
  - Ensemble Model: 277 anomalies (agreement of at least two models).
- **Historical Event Correlation**:
  - March 13, 2020: Anomalies in seven companies correspond to the declaration of a U.S. national emergency due to COVID-19 and Federal Reserve interventions.
- **Feature Analysis**:
  - Price Range showed significant deviations, confirmed by statistical tests and a large effect size (Cohen’s d = 1.18).

## Dependencies and Requirements

- **Python Version**: Python 3.x
- **Dependencies**: Listed in `requirements.txt`. Install them using:
  ```bash
  pip install -r requirements.txt
