# **Credit Card Fraud Detection using SEMMA Methodology**

## **Project Overview**
The objective of this project is to demonstrate the use of the SEMMA methodology (Sample, Explore, Modify, Model, Assess) on a real-world dataset to build an effective credit card fraud detection system. The dataset used is a publicly available credit card transaction dataset, which includes both legitimate and fraudulent transactions. This project aims to identify patterns that can help in distinguishing between fraudulent and non-fraudulent activities.

The project involves detailed steps to preprocess the data, explore key features, build a classification model, and evaluate the model's effectiveness using various performance metrics.

## **SEMMA Methodology**
The SEMMA (Sample, Explore, Modify, Model, Assess) methodology provides a structured approach for data mining projects, ensuring a systematic flow from data collection to model evaluation. Below is a brief description of how each phase is applied in this project:

### **1. Sample**
- Extracted a 10% sample from the original dataset to reduce computational load while preserving the distribution of legitimate and fraudulent transactions.
- Ensured that the sample maintained the same class proportions as the original dataset for accurate representation.

### **2. Explore**
- Conducted Exploratory Data Analysis (EDA) to visualize the distribution of fraudulent vs. non-fraudulent transactions.
- Analyzed correlations between various features using a heatmap to identify patterns and potential feature interactions.
- Plotted the distribution of the target class to understand class imbalance and its impact on modeling.

### **3. Modify**
- Scaled features such as `Amount` and `Time` to normalize the data using `StandardScaler`.
- Engineered new features such as `scaled_amount` to capture the significance of transaction amounts.
- Applied stratified sampling to split the data into training and testing sets, maintaining class balance.

### **4. Model**
- Implemented a Random Forest Classifier to classify transactions as either fraudulent or legitimate.
- Tuned the model using Grid Search to optimize hyperparameters and improve accuracy.
- Evaluated the model using classification metrics like Precision, Recall, and F1-Score.

### **5. Assess**
- Evaluated the model using a confusion matrix and ROC curve to analyze the trade-off between True Positives and False Positives.
- Achieved a high F1-Score of 0.91 and an AUC score of 0.96, indicating strong model performance in identifying fraudulent transactions.
- Visualized the results using a confusion matrix heatmap and ROC curve to demonstrate the model’s predictive power.

## **Dataset Information**
The dataset used for this project is the [Credit Card Fraud Detection Dataset](https://www.kaggle.com/mlg-ulb/creditcardfraud) from Kaggle. It contains a total of 284,807 transactions with 31 features, including:

- **Time**: Seconds elapsed between this transaction and the first transaction in the dataset.
- **V1 to V28**: Principal components obtained via PCA.
- **Amount**: Transaction amount.
- **Class**: Target variable (0 = Legitimate, 1 = Fraudulent).

## **Medium Article**
https://medium.com/@syedanidakhader/unmasking-fraud-leveraging-the-semma-methodology-for-credit-card-fraud-detection-dd48bff36483
