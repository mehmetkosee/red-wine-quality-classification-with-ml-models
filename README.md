# Red Wine Quality Classification using Machine Learning 🍷

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Library](https://img.shields.io/badge/Library-Scikit--Learn%20%7C%20Pandas%20%7C%20Seaborn-orange)
![License](https://img.shields.io/badge/License-MIT-green)

This project aims to predict the quality of red wine ("Good" or "Bad") based on physicochemical properties using various Machine Learning algorithms. The dataset contains 12 variables, including acidity, sugar, pH, and alcohol levels.

The original quality score (0-10) was transformed into a **binary classification problem**:
* **Good Wine (1):** Quality score $\ge$ 7
* **Bad Wine (0):** Quality score < 7

## Dataset
* **Source:** Red Wine Quality Dataset (Cortez et al., 2009)
* **Instances:** 1599
* **Features:** Fixed acidity, volatile acidity, citric acid, residual sugar, chlorides, free sulfur dioxide, total sulfur dioxide, density, pH, sulphates, alcohol.
* **Target:** Quality (converted to binary).

## 🛠️ Data Preprocessing & Methodology
1.  **EDA (Exploratory Data Analysis):** Analyzed correlations via Heatmap.
    * *Insight:* Alcohol and sulphates have the highest positive correlation with quality, while volatile acidity has a negative correlation.
2.  **Target Transformation:** Converted quality scores into binary classes.
3.  **Scaling:** Applied `StandardScaler` to normalize feature values for better model performance.
4.  **Modeling:** Implemented three classifiers:
    * Logistic Regression
    * Decision Tree Classifier
    * Random Forest Classifier
5.  **Optimization:** Used `GridSearchCV` to tune hyperparameters for the Random Forest model.

## 📊 Model Performance
The models were evaluated based on accuracy on the test set (20% split).

| Model | Accuracy Score |
|-------|----------------|
| Logistic Regression | 86.56% |
| Decision Tree | 88.75% |
| **Random Forest (Best Model)** | **90.31%** |

*The Confusion Matrix shows that the Random Forest model has high precision in distinguishing between good and bad wines.*

## 🚀 Installation & Usage

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/YOUR_USERNAME/red-wine-quality-classification-with-ml-models.git](https://github.com/YOUR_USERNAME/red-wine-quality-classification-with-ml-models.git)
    ```
2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Run the notebook:**
    Open `red-wine-quality-classification-with-ml-models.ipynb` in Jupyter Notebook or VS Code and run all cells.
