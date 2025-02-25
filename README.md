# Bank Fraud Anomaly Detection

This project demonstrates an unsupervised anomaly detection approach on bank transaction data to flag potential fraudulent activity. By combining multiple detection methods and using an ensemble “at least two votes” strategy, the project increases confidence in identifying suspicious transactions.

## Project Overview
This repository applies anomaly detection techniques—including Isolation Forest, KMeans-based detection, and DBSCAN—to bank transactions. An ensemble approach is used to flag transactions as anomalous if at least two methods agree, helping to reduce false positives and better highlight potential fraud.

## Methodology
### Data Preprocessing:
The data is cleaned and processed by removing irrelevant columns (e.g., TransactionID), handling missing values, and engineering features such as time differences between transactions and unique IP counts per account.

### Anomaly Detection:
Three methods are applied:
Isolation Forest  
KMeans-based detection (using distance from cluster centroids)  
DBSCAN (density-based clustering)

### Ensemble Approach:
A transaction is flagged as anomalous if at least two of the three methods identify it as such.

## Results
### Anomaly Overlap:
The project compares anomalies flagged by each method and analyzes overlaps using summary statistics and visualizations (e.g., PCA scatter plots, Venn diagrams).

### Insights:
Transactions flagged by all three methods tend to have more extreme values in key features, indicating a higher likelihood of fraud.

## Usage
1. Clone the Repository :
   git clone https://github.com/kealankuar/bank-fraud-anomaly-detection.git
   cd bank-fraud-anomaly-detection
2. pip install -r requirements.txt
3. Run the notebooks in Jupyter Notebook or JupyterLab or any other suitable IDE

## Future Improvements
Parameter Tuning: Further adjust model parameters (e.g., DBSCAN’s eps, KMeans cluster count) for optimal performance.  
Feature Expansion: Explore additional features and alternative dimensionality reduction methods.  
Validation: Incorporate domain expertise or historical fraud data for validation of the detected anomalies.  

## Dataset
The dataset is sourced from Kaggle and contains various features such as transaction amounts, dates, IP addresses, device IDs, and more.
Dataset Credit: https://www.kaggle.com/datasets/valakhorasani/bank-transaction-dataset-for-fraud-detection/data
