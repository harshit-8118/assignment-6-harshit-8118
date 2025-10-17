# DA5401 Assignment 6: Imputation via Regression for Missing Data 

**Student Name:** Harshit Shukla  
**Roll Number:** DA25S003  

  - -  -

## 1. Objective

This assignment challenges you to apply linear and non  -linear regression to impute missing values in a dataset. The effectiveness of your imputation methods will be measured indirectly by assessing the performance of a subsequent classification task, comparing the regression -based approach against simpler imputation strategies.

  - -  -

## 2. Methodology

The analysis was conducted in three main parts:
## PART A: Data Preprocessing and Imputation
* ### Load and prepare data
  - load, visualisation and prepare data 
  - one hot encoding for categorical columns
  - Artifically Missing cells at Random
  - Distribution visualization original vs missing
* ### Imputation Strategy 1:  (baseline)
  - filled missing values with medians
  - kde plots to see distribution of median imputed data, missing and original
  - demonstrated mean imputation
  - visulization through kde and box plots
  - Comparision between mean and median imputation
* ### Imputation strategy 2: Regression (Linear)
  - Linearly imputed on `BILL_AMT1` filling other missing cols with medians
  - Distribution comparision of `BILL_AMT1` with `Regression imputed`, `original`, and `missing`.
  - Actual vs predicted `BILL_AMT1` visualization.

* ### Imputation Strategy 3: Regression Imputation (Non -Linear)
  - `BILL_AMT1` column is imputed with KNN regressor filling other missing cols with medians.
  -   - Distribution comparision of `BILL_AMT1` with `KNN Reg imputed`, `original`, and `missing`.
  - Actual vs predicted `BILL_AMT1` visualization.

## Part B: Model Training and Performance Assessment 
* ### Data split & Standardization
  - train and test split for all five datasets, `Dataset_A`, `Dataset_B`, `Dataset_C`, `Dataset_D`, `Original`
  - train:test :: 3:1
  - standaridized the corresponding train and test dataset

* ### Model Evaluation
  - model is trained over training set of five datasets and tested on corresponding test sets.
  - moderate class imbalance in `Default` is removed using `smote`.
  - classification report and confusion matrix is generated.

## PART C: Comparative Analysis
* ### Results comparision
  - created summary table comparing performance metrics of five models:
  - Model A (Median Imputation) 
  - Model B (Linear Regression Imputation) 
  - Model C (Non-Linear Regression Imputation) 
  - Model D (Listwise Deletion)
  - Model E (original)

* ### Efficacy Discussion
  - Analyze and discuss the effectiveness of each imputation method.


### 3. File Structure
```
.
├── main.ipynb      # The Jupyter Notebook with code
└── README.md               # This documentation file.
```