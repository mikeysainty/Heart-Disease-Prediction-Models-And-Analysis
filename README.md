# Heart Disease Prediction Models and Analysis
This repository contains a Jupyter notebook for predicting the likelihood of heart disease using various machine learning models. The dataset used in this project is the Behavioral Risk Factor Surveillance System (BRFSS) 2015 dataset. It includes various health-related attributes and is publicly available on Kaggle. The notebook demonstrates data preprocessing, exploratory data analysis, model development, evaluation, and model interpretation.

**Source:** [BRFSS 2015 Dataset on Kaggle](https://www.kaggle.com/datasets/cdc/behavioral-risk-factor-surveillance-system/data)

## Features
### Data Loading and Preprocessing
- **Loading the dataset:** Load the dataset from a CSV file.
- **Selecting specific features:** Select features related to heart disease from the 330 available variables in the dataset.
- **Handling missing values:** Handle any missing values and scale the features appropriately.

### Exploratory Data Analysis (EDA)
- **Summary statistics:** Generate summary statistics for the dataset.
- **Data visualization:** Create visualizations to understand the data distribution and relationships.
- **Correlation analysis:** Analyze correlations between different features.

### Model Development
- **Logistic Regression:** Implement and evaluate a Logistic Regression model.
- **Random Forest:** Implement and evaluate a Random Forest model.
- **Neural Network:** Implement and evaluate a Neural Network model.
- **Naive Bayes:** Implement and evaluate a Naive Bayes model.
- **Decision Tree:** Implement and evaluate a Decision Tree model.
- **Model evaluation:** Use accuracy, precision, recall, F1-score, and ROC AUC for model evaluation.

### Model Interpretation
- **Logistic Regression:** Coefficient analysis.
- **Random Forest and Decision Tree:** Feature importance scores.

## Dataset
The dataset includes over 330 features, but the notebook focuses on the following health-related attributes:
- **HeartDiseaseorAttack:** Binary classification indicating the presence (1) or absence (0) of heart disease or heart attack.
- **HighBP:** Binary classification indicating high blood pressure.
- **HighChol:** Binary classification indicating high cholesterol.
- **CholCheck:** Binary classification indicating if cholesterol check was performed.
- **BMI:** Body mass index (weight in kg / height in m²).
- **Smoker:** Binary classification indicating if the person has smoked 100 cigarettes in their lifetime.
- **Stroke:** Binary classification indicating if the person has had a stroke.
- **Diabetes:** Binary classification indicating if the person has diabetes.
- **PhysActivity:** Binary classification indicating if the person has engaged in physical activity.
- **Fruits:** Binary classification indicating if the person consumes fruit daily.
- **Veggies:** Binary classification indicating if the person consumes vegetables daily.
- **HvyAlcoholConsump:** Binary classification indicating heavy alcohol consumption.
- **AnyHealthcare:** Binary classification indicating if the person has any healthcare coverage.
- **NoDocDueCost:** Binary classification indicating if the person could not see a doctor due to cost.
- **GenHlth:** General health status (ordinal scale).
- **MentHlth:** Number of days with poor mental health.
- **PhysHlth:** Number of days with poor physical health.
- **DiffWalk:** Binary classification indicating difficulty walking.
- **Sex:** Binary classification indicating the sex of the person.
- **Age:** Age in years (grouped in 5-year increments).
- **Education:** Education level (ordinal scale).
- **Income:** Income level (ordinal scale).

## Results
The following table summarizes the performance metrics for each model:

| Model               | Accuracy | Precision (0) | Precision (1) | Recall (0) | Recall (1) | F1-score (0) | F1-score (1) | Macro Avg Precision | Macro Avg Recall | Macro Avg F1-score | Weighted Avg Precision | Weighted Avg Recall | Weighted Avg F1-score |
|---------------------|----------|---------------|---------------|------------|------------|--------------|--------------|----------------------|------------------|-------------------|------------------------|----------------------|----------------------|
| Logistic Regression | 0.9062   | 0.91          | 0.55          | 0.99       | 0.12       | 0.95         | 0.20         | 0.73                 | 0.56             | 0.57              | 0.88                   | 0.91                 | 0.88                 |
| Random Forest       | 0.9024   | 0.91          | 0.47          | 0.99       | 0.11       | 0.95         | 0.18         | 0.69                 | 0.55             | 0.56              | 0.87                   | 0.90                 | 0.87                 |
| Neural Network      | 0.9063   | 0.91          | 0.63          | 1.00       | 0.06       | 0.95         | 0.11         | 0.77                 | 0.53             | 0.53              | 0.88                   | 0.91                 | 0.87                 |
| Naive Bayes         | 0.8164   | 0.95          | 0.27          | 0.85       | 0.54       | 0.89         | 0.36         | 0.61                 | 0.69             | 0.63              | 0.88                   | 0.82                 | 0.84                 |
| Decision Tree       | 0.8497   | 0.92          | 0.25          | 0.91       | 0.28       | 0.92         | 0.26         | 0.59                 | 0.59             | 0.59              | 0.86                   | 0.85                 | 0.85                 |

## Summary
The results of the models show the following key points:
- **High Accuracy:** Logistic Regression and Neural Network models show the highest accuracy, indicating they are generally good at predicting the overall outcome.
- **Precision and Recall for Class 0 (No Heart Disease):** All models have high precision and recall for class 0, indicating they are very good at correctly identifying individuals without heart disease.
- **Struggling with Class 1 (Heart Disease):** Most models have lower precision and recall for class 1, indicating they struggle to correctly identify individuals with heart disease.
  - Logistic Regression and Random Forest models have moderate precision but very low recall for class 1.
  - Neural Network has higher precision for class 1 but still has very low recall.
  - Naive Bayes shows a more balanced approach with relatively higher recall for class 1 but lower precision.
- **Class Imbalance:** The significant class imbalance in the dataset (229,787 instances of no heart disease vs. 23,893 instances of heart disease) affects the models' ability to correctly identify heart disease cases compared to no heart disease cases.
- **F1-Scores:** F1-scores are generally higher for class 0 across all models, showing that they perform better at predicting no heart disease.

## Conclusion
The models are very good at correctly predicting the absence of heart disease (class 0) but struggle more with predicting the presence of heart disease (class 1). This indicates a need for further tuning and possibly exploring additional features or different modeling approaches to improve recall for heart disease cases.

## Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue for any bugs, feature requests, or improvements.
