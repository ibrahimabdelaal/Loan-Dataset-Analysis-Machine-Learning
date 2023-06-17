# Loan-Dataset-Analysis-Machine-Learning

This repository contains code and documentation for analyzing loan-related information to assess loan applications. The goal is to identify which pieces of information have a strong relationship with the total loan amount and loan duration, enabling the bank to make better loan decisions.

# Motivation

Understanding the loan-related data can lead to better decision-making in various aspects. By analyzing this data, we can improve our loan assessment process, target specific clients for marketing purposes, and allocate resources more effectively. The insights gained from understanding this data can provide significant benefits to the bank.

# Dataset Description

The dataset consists of a row dataset with 11 columns, each containing specific information about customers and their loans. Here are the key columns:

Total O/S: Total loan amount

TENOR_@Booking: Duration in months for the loan

Loan Term: Duration in years

Booking Date: Date when the loan data is entered

Maturity Date: Date when the final loan payment is due

DPD: Days past dues, indicating missed repayments and their durations

DOB: Date of Birth of the client

Age of the client

Gender of the client

Customer Segment: Classification of the customer based on employment type

# Approach and Methodology

The analysis follows a systematic approach and methodology:

Preprocessing:

1- Data cleaning: Handling null and duplicate values by dropping them (since the number of NaN values is minimal).

2- Encoding categorical variables: Transforming categorical variables, such as gender and customer segmentation, into numerical representations. Additionally, using Unix timestamps to represent dates in the dataset.
Data Visualization:

3- Exploring the relationship between different attributes and loan duration/total loan amount using various visualization techniques:
Heatmaps, histograms, and count plots

4- PCA (Principal Component Analysis) for multivariate visualization

Through data analysis and visualization, we gain insights into attribute relationships and the distribution of data.

# Data Analysis Results:

Heatmap findings:

Loan term shows a strong correlation with tenor_@Booking and maturity date.
Total amount is most correlated with customer segmentation.
Gender has the least correlation with other attributes.
TENOR_@Booking has the lowest correlation with other attributes.
Age at maturity correlates strongly with age.
Other findings:

The majority of clients fall within the age range of 29 to 48.

Males represent 83.97% of the dataset, while females represent 16.03%.

# PCA Analysis:

Performing PCA analysis on the dataset to examine attribute relationships and generate principal components.
![image](https://github.com/ibrahimabdelaal/Loan-Dataset-Analysis-Machine-Learning/assets/49596777/09ecd924-0b85-4239-a859-32ec3b2f6cf4)


Results show that gender and DOB attributes are less important, while the first principal component provides information about age, age at maturity, and date of birth.
# K-means Clustering:

Employing K-means clustering using the first two principal components.

Utilizing the elbow method to determine an optimal value for k (the number of clusters) based on the variance explained.

Fitting the model with different k values (3, 4, 6, and 7).

Hierarchical Clustering:

![image](https://github.com/ibrahimabdelaal/Loan-Dataset-Analysis-Machine-Learning/assets/49596777/0cad1469-ee4e-46e6-8f97-789bdb4572a1)

Using the dendrogram visualization to suggest values for k (the number of clusters).

Dendrogram suggests values of 3, 4, and possibly 6.
![image](https://github.com/ibrahimabdelaal/Loan-Dataset-Analysis-Machine-Learning/assets/49596777/91c37689-5c6d-433d-b028-9e20ccd6f833)

# Evaluation of Different Models:

* Evaluating the models using silhouette scores, which measure the quality of clustering results.

Silhouette scores for data with 2 principal components:

K=3: 0.373

K=4: 0.348

K=7: 0.353

Based on the above scores, clustering the data into 3 clusters provides the best result.

Libraries Used
The following libraries were used for this analysis:


# Conclusion 
Classification model: Building a model to classify each loan application into one of the identified clusters.
Regression models: Developing regression models based on attribute correlations, such as predicting loan term.
Predicting loan amounts: Creating a model to predict the total loan amount, with the requirement of additional attributes such as income.
This analysis provides valuable insights that can enhance loan assessment processes and enable more accurate decision-making.
