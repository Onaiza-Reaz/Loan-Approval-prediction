# Loan-Approval-prediction


This project involves building a machine learning model to predict loan approval based on various financial and personal attributes of loan applicants. The dataset used in this project contains various features such as education, employment status, income, and asset values. The goal is to determine whether an applicant's loan will be approved or not.

**Steps Involved**

**1. Importing Libraries**
We begin by importing essential libraries such as pandas, numpy, matplotlib, seaborn, and sklearn. These libraries are used for data manipulation, visualization, and building machine learning models.

**2. Loading Dataset**
The dataset is loaded into a pandas DataFrame for further processing and analysis.

**3. Data Cleaning**
Data cleaning involves several steps:

1: Handling missing values: Numerical columns have missing values filled using the mean of the column, and categorical columns have missing values filled using the forward fill method.

2: Correcting data types: Certain columns are converted to categorical data types.

3: Addressing inconsistent or erroneous data entries: Binary columns are standardized to have consistent 'Yes' or 'No' values.

4: Standardizing formats: Monetary values are converted to integers, and some other columns are ensured to be of integer type.

5: Applying label encoding: Categorical columns such as 'education', 'self_employed', and 'loan_status' are label encoded for model training.

**4. Exploratory Data Analysis (EDA)**

EDA is performed to understand the dataset better:

1: Generating descriptive statistics: This provides an overview of the dataset's distribution

2: Creating visualizations: Histograms for numerical columns, bar charts for categorical columns, and box plots for numerical columns are generated to visualize the data distribution and identify patterns.

3: Creating a correlation matrix: A heatmap of the correlation matrix is created to visualize the relationships between numerical features.

**5. Outlier Detection and Removal**

Outliers are detected and handled using the Interquartile Range (IQR) method:

Outliers are identified based on the IQR and can either be removed or capped.

This step helps in improving the model performance by handling extreme values that could skew the results.

**6. Manual Data Splitting**

The cleaned dataset is manually split into training and testing sets with an 80/20 split ratio. This allows for evaluating the model's performance on unseen data.

**7. Model Training**

A K-Nearest Neighbors (KNN) model is trained on the training set. The KNN model is chosen for its simplicity and effectiveness in classification tasks.

**8. Model Evaluation**

The trained KNN model is evaluated using various metrics:

Accuracy: The proportion of correctly predicted instances out of the total instances.

Precision: The proportion of true positive predictions out of all positive predictions.

Recall: The proportion of true positive predictions out of all actual positives.

F1 Score: The harmonic mean of precision and recall, providing a single measure of model performance.

Confusion Matrix: A matrix showing the actual versus predicted classifications, helping to visualize the performance of the model.

ROC-AUC: The Area Under the Receiver Operating Characteristic Curve, providing an aggregate measure of performance across all classification thresholds.

**9. Cross-Validation**

Cross-validation is implemented to assess the performance of the KNN model more robustly:

Cross-validation scores for accuracy, precision, recall, and F1 score are calculated and averaged.

This step helps in understanding the model's performance stability across different subsets of the data.

**Results and Findings**

The KNN model's accuracy on the test set is reported.

Precision, recall, F1 score, and ROC-AUC are calculated to provide a comprehensive evaluation of the model's performance.

Cross-validation results are compared to the manual split results to assess the model's consistency.
