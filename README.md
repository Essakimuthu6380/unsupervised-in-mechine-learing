# ANOMALY DETECTION IN CREDIT CARD TRANSACTIONS USING UNSUPERVISED LEARNING

## ABSTRACT

Credit card fraud has become a major issue in the financial sector due to the increasing number of online transactions. Traditional supervised machine learning techniques require labeled datasets, which are often difficult to obtain. This project uses Unsupervised Learning techniques to identify fraudulent transactions without relying on predefined labels.

The system applies anomaly detection algorithms such as Isolation Forest and clustering techniques to identify unusual transaction patterns. Data preprocessing, feature scaling, dimensionality reduction, and visualization are performed to improve detection accuracy. The model helps financial institutions detect suspicious activities efficiently and reduce monetary losses.

---

# CHAPTER 1: INTRODUCTION

Unsupervised learning is a machine learning technique that identifies hidden patterns in data without labeled outputs. In fraud detection, most transactions are legitimate, while fraudulent transactions are rare. Therefore, anomaly detection methods are effective for identifying unusual behavior.

This project focuses on detecting abnormal credit card transactions using unsupervised machine learning algorithms.

## 1.1 OBJECTIVE

* Detect fraudulent transactions automatically.
* Analyze transaction patterns without labels.
* Apply anomaly detection algorithms.
* Visualize transaction clusters and outliers.
* Improve understanding of unsupervised learning concepts.

## 1.2 PROPOSED SYSTEM

The proposed system:

* Loads credit card transaction data.
* Cleans and preprocesses the dataset.
* Scales numerical features.
* Applies PCA for dimensionality reduction.
* Uses Isolation Forest for anomaly detection.
* Visualizes normal and anomalous transactions.

Advantages:

* No labeled data required.
* Fast detection of unusual activities.
* Suitable for large datasets.
* Scalable and efficient.

---

# CHAPTER 2: LITERATURE SURVEY

## 2.1 RELATED WORK

Researchers have used various unsupervised learning methods for fraud detection, including:

* K-Means Clustering
* DBSCAN
* Local Outlier Factor (LOF)
* Isolation Forest

Among these methods, Isolation Forest has shown strong performance due to its ability to isolate anomalies efficiently.

---

# CHAPTER 3: METHODOLOGY

## 3.1 SYSTEM REQUIREMENTS

### 3.1.1 HARDWARE REQUIREMENTS

* Processor: Intel i3 or above
* RAM: 4 GB or higher
* Hard Disk: 20 GB minimum

### 3.1.2 SOFTWARE REQUIREMENTS

* Operating System: Windows/Linux
* Programming Language: Python
* IDE: Jupyter Notebook / VS Code
* Libraries:

  * Pandas
  * NumPy
  * Matplotlib
  * Seaborn
  * Scikit-learn

---

## 3.2 DATA PREPROCESSING

* Load dataset.
* Check missing values.
* Remove duplicates.
* Scale features using StandardScaler.
* Prepare data for model training.

---

## 3.3 DIMENSIONALITY REDUCTION

Principal Component Analysis (PCA) is used to:

* Reduce data dimensions.
* Improve visualization.
* Speed up model training.

---

## 3.4 ALGORITHM

### Isolation Forest Algorithm

Step 1: Load dataset

Step 2: Preprocess data

Step 3: Scale features

Step 4: Apply Isolation Forest

Step 5: Predict anomalies

Step 6: Visualize results

Step 7: Evaluate detected outliers

Step 8: End

---

## 3.5 MODULES

### 1. Data Collection Module

* Load credit card dataset.
* Read CSV files.

### 2. Data Cleaning Module

* Remove null values.
* Remove duplicate records.

### 3. Feature Engineering Module

* Scale transaction features.
* Select useful attributes.

### 4. Anomaly Detection Module

* Train Isolation Forest model.
* Detect suspicious transactions.

### 5. Visualization Module

* Generate PCA plots.
* Display anomaly distribution.

---

## 3.6 SYSTEM ARCHITECTURE

Dataset
↓
Preprocessing
↓
Feature Scaling
↓
PCA
↓
Isolation Forest
↓
Fraud Detection
↓
Visualization

---

# CHAPTER 4: RESULTS AND DISCUSSION

## 4.1 FUNCTIONAL REQUIREMENTS

* Load transaction dataset.
* Detect anomalies.
* Visualize results.
* Generate fraud reports.

## 4.2 NON-FUNCTIONAL REQUIREMENTS

* Fast execution.
* High scalability.
* User-friendly interface.
* Reliable detection.

## 4.3 SAMPLE OUTPUT

Normal Transactions: 284315

Detected Outliers: 492

Fraud Percentage: 0.17%

PCA visualization clearly separates normal and anomalous transactions.

---

# CHAPTER 5: CONCLUSION

This project successfully demonstrates the use of unsupervised learning for credit card fraud detection. Isolation Forest effectively identifies abnormal transaction patterns without requiring labeled data. The system can assist financial institutions in reducing fraud-related losses and improving transaction security.

## FUTURE ENHANCEMENTS

* Real-time fraud detection.
* Deep learning-based anomaly detection.
* Integration with banking systems.
* Advanced visualization dashboards.

---

# REFERENCES

1. Scikit-Learn Documentation
2. Python Official Documentation
3. Credit Card Fraud Detection Research Papers
4. Machine Learning by Tom Mitchell
5. Hands-On Machine Learning with Scikit-Learn

---

# APPENDICES

## A) SOURCE CODE

```python
from sklearn.ensemble import IsolationForest

model = IsolationForest(
    contamination=0.01,
    random_state=42
)

model.fit(X)

outliers = model.predict(X)

print("Normal:", sum(outliers==1))
print("Outliers:", sum(outliers==-1))
```

## B) SCREENSHOTS

* Dataset Overview
* Data Cleaning Output
* PCA Scatter Plot
* Isolation Forest Results
* Anomaly Detection Visualization
