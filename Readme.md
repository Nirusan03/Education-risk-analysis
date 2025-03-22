# Student Writing Risk Prediction

This repository contains all files related to the Machine Learning in Business Assessment. The goal of this project is to identify primary school students at risk of underperforming in writing by Year 3 using machine learning models.

---

## Project Overview

This project was conducted in collaboration with a fictional Australian learning analytics consultancy, **Data2Intel**, as part of a university coursework assessment. The dataset includes information on 2,000 students from over 40 schools, focusing on their demographics, literacy, and numeracy skills in early primary years (Year 1 and Year 2).

The ultimate goal is to help schools **predict and intervene early** with students who may be at risk of low writing performance by Year 3 (as indicated by NAPLAN results).

---

## Objectives
- Predict students at risk of underperforming in writing by Year 3.
- Explore and visualise key insights through EDA.
- Build and evaluate supervised machine learning models.
- Group students using clustering for early intervention strategies.
- Deliver both a technical report and a business report.

---

## Repository Structure

```
├── data/
│   └── LA4PSchools.csv                 # The main dataset (not included here for privacy)
│
├── Final_Model.ipynb                  # Combined notebook for all models
├── LogisticRegression.ipynb          # Logistic Regression model notebook
├── RandomForest.ipynb                # Random Forest model notebook
├── KMean.ipynb                        # K-Means clustering notebook
│
│
└── README.md                         # You are here
```

---

## Machine Learning Models Used

### 1. **Logistic Regression**
- Accuracy: ~74.9%
- Simple and interpretable baseline
- Hyperparameter tuning via GridSearchCV

### 2. **Random Forest Classifier** **Recommended Model**
- Accuracy: ~80.9%
- Best performance overall
- Handles imbalance using `class_weight='balanced'`
- Feature importance and permutation analysis used

### 3. **K-Means Clustering**
- Used for unsupervised grouping of students
- Optimal clusters determined using Elbow Method and Silhouette Score
- PCA used for dimensionality reduction and visualisation

---

## Dataset Description

The dataset `LA4PSchools.csv` includes:
- **Target Variable**: `Year3_Writing_At_Risk` (True/False)
- **Demographics**: Gender, Kinder Age, Disability, NCCD Funding
- **Family Background**: Number of siblings, parental education, occupation
- **School SES**: For Year 1 and Year 2
- **Assessments**:
  - Literacy: Burt, Clay, TextLevel, WritingVocab, HRSIW
  - Numeracy: Counting, Place Value, Addition/Subtraction, Multiplication/Division

> The dataset was pre-cleaned by the provider. Additional preprocessing such as encoding, scaling, outlier removal, and SMOTE were performed during the analysis.

---

## Instructions to Run the Project

> Dataset is not publicly shared here due to privacy restrictions. You must place `LA4PSchools.csv` in your working directory.

1. Clone the repository:
```bash
git clone https://github.com/Nirusan03/Education-risk-analysis.git
cd Education-risk-analysis
```

2. (Optional) Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
```

3. Install the required packages:
```bash
pip install -r requirements.txt  # create this file manually if needed
```

4. Open the notebooks:
- Run each of the following notebooks in order:
  - `LogisticRegression.ipynb`
  - `RandomForest.ipynb`
  - `KMean.ipynb`

Or use the combined `Final_Model.ipynb` to view everything in one place.

---

## Evaluation Metrics
- **Accuracy, Precision, Recall, F1-score**
- **ROC Curve and AUC (for LR)**
- **Confusion Matrix**
- **Feature Importance (RF)**
- **Silhouette Score for Clustering**

---

## Recommendations
- Deploy **Random Forest** for real-time prediction in educational systems.
- Use **K-Means clusters** for targeted support groups.
- Focus on students with low SES, poor early reading scores, and cognitive disabilities.
- Retrain the model periodically with new data for improved accuracy.

---

## Contact
For any queries, please reach out via [nirusan.hariharan350@gmail.com].
