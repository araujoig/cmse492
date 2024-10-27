# Anomaly Detection in Financial Trading Data

## Project Description
This project aims to develop an unsupervised machine learning model for detecting anomalous trading patterns within financial market data. By identifying unusual trading behaviors, we can spot potential market manipulation or fraudulent activities. The goal is to create a real-time system capable of flagging significant deviations from normal market activities.

## Project Objectives
- **Develop** a machine learning model to detect anomalous trading patterns in financial data.
- **Implement** an unsupervised learning system for real-time anomaly detection that flags potential irregularities for further investigation.

## Folder Structure

- **data/**: Contains all data files.
  - **raw/**: Raw data files (e.g., `data.csv`).
  - **processed/**: Processed and cleaned data files for model input (e.g., `cleaned_data.csv`).
- **notebooks/**: Jupyter notebooks for data exploration and model development.
  - `exploratory_data_analysis.ipynb`: Exploratory analysis of the data.
  - `model_training.ipynb`: Training and evaluation of the anomaly detection model.
- **reports/figures/**: Visualizations and figures generated during analysis.
  - Includes various plots, such as anomaly detection results and trading volume distributions.
- **src/**: Source code for data preprocessing and model building.
  - `data_preprocessing.py`: Preprocessing functions for data cleaning and transformation.
  - `anomaly_detection_model.py`: Code to build and evaluate the anomaly detection model.
- **README.md**: Project overview and setup instructions.
- **requirements.txt**: List of dependencies required to run the project.

## Dependencies and Requirements
- Python 3.x
- Required packages listed in `requirements.txt`. Install them by running:
  ```bash
  pip install -r requirements.txt
