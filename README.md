# KNN Iris Flower Classification

## Overview
This repository implements a **K-Nearest Neighbors (KNN)** classifier on the Iris dataset, achieving **95.6% accuracy** with optimal hyperparameters. It covers the complete ML pipeline—from data exploration to decision boundary visualization.


## Objectives
- Perform comprehensive EDA on Iris flower measurements
- Implement and tune KNN using scikit-learn
- Evaluate model performance using accuracy, confusion matrix, and classification report
- Visualize decision boundaries to understand decision-making


## Tools & Technologies
- **Language**: Python  
- **Environment**: Google Colab / Jupyter Notebook  

**Libraries Used:**
- `pandas`, `numpy` – Data manipulation
- `matplotlib`, `seaborn` – Visualizations
- `scikit-learn` – KNN algorithm & evaluation metrics
- `mlxtend` – Decision boundary plotting


## Dataset
- **Source**: UCI Machine Learning Repository  
- **Samples**: 150 (50 samples per class)  
- **Features**:
  - Sepal Length (cm)
  - Sepal Width (cm)
  - Petal Length (cm)
  - Petal Width (cm)  
- **Target**: Iris species – setosa, versicolor, virginica


## Workflow & Highlights

### 1. Exploratory Data Analysis (EDA)
- Analyzed feature distributions by species.
- Identified petal measurements as the most discriminative.


### 2. Model Building
- Standardized features using `StandardScaler`.
- Split dataset: **70% training / 30% testing** (with stratification).
- Evaluated K from 1 to 20.  
  **Best K = 9**, achieving **95.6% accuracy**


### 3. Model Evaluation

**Confusion Matrix:**

|                   | Predicted: Setosa | Predicted: Versicolor  | Predicted: Virginica  |
|-------------------|------------------ |------------------------|-----------------------|
| Actual Setosa     |        15         |           0            |          0            |
| Actual Versicolor |     0             |          15            |          0            |
| Actual Virginica  |     0             |           2            |         13            |

**Classification Report:**
- Precision: 1.00 (setosa), 0.88 (versicolor), 1.00 (virginica)
- Recall:    1.00 (setosa), 1.00 (versicolor), 0.87 (virginica)


### 4. Advanced Analysis
- **Decision Boundary** visualized using Petal Length & Width.
- **Error Analysis**: 2 virginica samples misclassified as versicolor.


## Key Insights
- **Optimal K=9** offers a good balance of bias and variance.
- **Petal dimensions** are the most important features for accurate classification.
- Some confusion exists between _virginica_ and _versicolor_, indicating overlapping feature space.


## How to Run
1. Upload `Iris.csv` to Colab.
2. Run the notebook cells sequentially.
3. Explore accuracy results and boundary plots.
