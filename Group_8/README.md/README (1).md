# IT2011 Artificial Intelligence and Machine Learning Project

## Project Title
**Fitness Classification Using Machine Learning**

## Project Overview
This project applies data preprocessing, exploratory data analysis (EDA), feature engineering, machine learning model design, hyperparameter tuning, and model evaluation to a fitness-related dataset.

The objective is to predict the target variable **`is_fit`**, where the model classifies whether a person is fit or not fit based on the available input features.

The project is completed as a six-member group assignment. Each member is responsible for an individual preprocessing contribution and one individual machine learning model. The final group work combines the individual contributions into an integrated preprocessing pipeline and a six-model comparison.

---

## Dataset

### Dataset File
`fitness_dataset.csv`

### Target Variable
`is_fit`

### Main Features
- `age`
- `gender`
- `height_cm`
- `weight_kg`
- `heart_rate`
- `blood_pressure`
- `sleep_hours`
- `nutrition_quality`
- `activity_index`
- `smokes`
- `is_fit`

### Data Issues Handled
- Missing values in `sleep_hours`
- Mixed values in `smokes`
- Outliers in `weight_kg`
- Categorical encoding
- Feature engineering using BMI
- Standardization / scaling
- EDA visualizations

---

## Group Member Roles

### Preprocessing and EDA Responsibilities

| Member | Student | Assigned Task | Visualization |
|---|---|---|---|
| Member 1 | IT25101600 – Husain N.N | Missing values | Histogram of `sleep_hours` |
| Member 2 | IT25102434 – Navoda K.P.K | Mixed `smokes` data cleaning | Bar chart of smoking status |
| Member 3 | IT25103453 – De Silva S.T.S.M | Outlier handling | Boxplot of `weight_kg` |
| Member 4 | IT25101303 – Kumarasingha I.S.N.P | Categorical encoding | Countplot of `gender` vs `is_fit` |
| Member 5 | IT25103237 – Kavindi J.V.M | Feature engineering – BMI | Scatter plot of BMI vs `is_fit` |
| Member 6 | IT25100430 – Kariyawasam K.H.M.M | Standardization / scaling | Correlation heatmap |

### Machine Learning Model Responsibilities

| Member | Student | Assigned Model |
|---|---|---|
| Member 1 | IT25101600 – Husain N.N | Logistic Regression |
| Member 2 | IT25102434 – Navoda K.P.K | K-Nearest Neighbors (KNN) |
| Member 3 | IT25103453 – De Silva S.T.S.M | Support Vector Machine (SVM) |
| Member 4 | IT25101303 – Kumarasingha I.S.N.P | Decision Tree |
| Member 5 | IT25103237 – Kavindi J.V.M | Random Forest |
| Member 6 | IT25100430 – Kariyawasam K.H.M.M | Gradient Boosting |

---

## Repository Structure

```text
Group_ID/
│
├── README.md
│
├── data/
│   ├── raw/
│   │   └── fitness_dataset.csv
│   ├── external/
│   │   └── (external datasets, if used)
│   └── processed/
│       └── fitness_processed.csv
│
├── notebooks/
│   ├── IT25101600_Logistic_Regression.ipynb
│   ├── IT25102434_KNN.ipynb
│   ├── IT25103453_SVM.ipynb
│   ├── IT25101303_Decision_Tree.ipynb
│   ├── IT25103237_Random_Forest.ipynb
│   └── IT25100430_Gradient_Boosting.ipynb
│
├── group_pipeline.ipynb
├── group_model_pipeline.ipynb
│
└── results/
    ├── eda_visualizations/
    ├── model_visualizations/
    ├── logs/
    └── outputs/
```

---

## Preprocessing Workflow

1. Load the raw dataset.
2. Inspect the dataset structure and data types.
3. Identify missing values.
4. Handle missing `sleep_hours` values.
5. Clean mixed values in `smokes`.
6. Detect and handle outliers in `weight_kg`.
7. Encode categorical variables.
8. Create BMI as a new feature.
9. Standardize / scale features where required.
10. Perform EDA and generate visualizations.
11. Save the processed dataset for model training.

---

## Machine Learning Models

### 1. Logistic Regression
Main hyperparameter:
- `C`

### 2. K-Nearest Neighbors
Main hyperparameters:
- `n_neighbors`
- `weights`
- `p`

### 3. Support Vector Machine
Main hyperparameters:
- `C`
- `kernel`
- `gamma`

### 4. Decision Tree
Main hyperparameters:
- `max_depth`
- `min_samples_split`
- `criterion`

### 5. Random Forest
Main hyperparameters:
- `n_estimators`
- `max_depth`
- `min_samples_split`

### 6. Gradient Boosting
Main hyperparameters:
- `n_estimators`
- `learning_rate`
- `max_depth`

---

## Model Training and Evaluation

Each individual model notebook includes:

1. Import required libraries.
2. Load the dataset.
3. Prepare features and target.
4. Split the dataset into training and testing sets.
5. Build a baseline model.
6. Perform hyperparameter tuning using `GridSearchCV`.
7. Use stratified 5-fold cross-validation.
8. Select the best parameter combination.
9. Train the optimum model.
10. Generate predictions.
11. Evaluate model performance.

### Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion Matrix
- Classification Report

---

## Group Model Comparison

The final group model pipeline compares the optimum result from each of the six individual models.

The final comparison includes:
- Best hyperparameters
- Cross-validation F1-score
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Confusion matrix
- Limitations and observations

---

## How to Run the Project

### Requirements

```bash
pip install pandas numpy matplotlib scikit-learn joblib
```

### Step 1 – Place the Dataset

```text
data/raw/fitness_dataset.csv
```

### Step 2 – Run the Group Preprocessing Pipeline

Open:

```text
group_pipeline.ipynb
```

Run all cells in order.

### Step 3 – Run the Individual Model Notebooks

Open the required notebook from the `notebooks/` folder and run all cells.

Example:

```text
notebooks/IT25101600_Logistic_Regression.ipynb
```

### Step 4 – Run the Group Model Comparison

Open:

```text
group_model_pipeline.ipynb
```

Run all cells to compare the six optimum models.

### Step 5 – Check Results

Generated outputs should be available under:

```text
results/
```

---

## Results Folder

### EDA Visualizations
`results/eda_visualizations/`

### Model Visualizations
`results/model_visualizations/`

### Logs
`results/logs/`

### Outputs
`results/outputs/`

---

## Tools and Libraries

- Python
- Jupyter Notebook / Google Colab
- pandas
- NumPy
- Matplotlib
- scikit-learn
- joblib

---

## Ethical Considerations

The model is developed for academic purposes.

The group should consider:
- Possible bias in the dataset
- Representation of different groups
- Differences in performance across subgroups
- Limitations of using a simplified `is_fit` target
- Risk of treating model predictions as medical conclusions

This project should not be treated as a medical diagnostic system.

---

## Final Deliverables

- `README.md`
- Raw dataset
- Individual preprocessing contributions
- Integrated preprocessing pipeline
- Six individual model notebooks
- Integrated six-model comparison
- EDA visualizations
- Model evaluation outputs
- Final processed dataset
- Final group report

---

## Group Note

Each member should be prepared to explain:
- Their preprocessing contribution
- Their assigned machine learning model
- Why the model is suitable
- Hyperparameters used
- Tuning method
- Validation method
- Evaluation metrics
- Model performance
- Limitations and possible improvements
