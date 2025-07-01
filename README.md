# Summer-Analytics-Hackathon-2
The NHANES Age Classification project focuses on predicting whether an individual is a Senior (65+) or an Adult (under 65) based on various health and lifestyle metrics collected in the NHANES survey by the CDC. The dataset includes features like BMI, glucose levels, insulin levels, and physical activity indicators. 

# NHANES Age Classification

This project uses a subset of the National Health and Nutrition Examination Survey (NHANES) data to classify individuals into two age groups: **Adult (under 65)** and **Senior (65 and over)** based on a range of health and lifestyle indicators.

## 📂 Dataset

- `Train_Data.csv`: Contains 1,966 samples with 7 features and the target column `age_group`.
- `Test_Data.csv`: Contains 312 samples without the target column. Your task is to predict `age_group` for these entries.
- `Sample_Submission.csv`: Shows the required format for test set predictions (binary: 0 for Adult, 1 for Senior).

### Features

| Column    | Description |
|-----------|-------------|
| `SEQN`    | Unique identifier (dropped during processing) |
| `RIAGENDR`| Gender (1 = Male, 2 = Female) |
| `PAQ605`  | Engages in moderate/vigorous activity (1 = Yes, 2 = No) |
| `BMXBMI`  | Body Mass Index |
| `LBXGLU`  | Glucose level |
| `DIQ010`  | Diabetes questionnaire response |
| `LBXGLT`  | Glucose tolerance (oral) |
| `LBXIN`   | Insulin level |
| `age_group` | Target variable (0 = Adult, 1 = Senior) |

## 🧹 Preprocessing

- Handled missing values using median (for numeric) and mode (for categorical) imputation.
- Dropped the `SEQN` column as it does not contribute to predictions.
- Encoded the `age_group` column: `Adult` → `0`, `Senior` → `1`.

## 📊 EDA & Feature Engineering

- Performed visual analysis to understand distribution of classes and features.
- Explored correlations to identify key predictors of age group.
- Considered normalization/standardization where applicable.

## 🧠 Modeling

Several classification models can be tried:
- Logistic Regression
- Random Forest
- XGBoost
- Support Vector Machine

Evaluation Metric: **Accuracy** or **F1 Score**, depending on class balance.

## 📤 Submission

Prepare a file with the following format:
```csv
age_group
0
1
0
...
