# Drug Recommendation Using Decision Tree Classifier

This repository contains a complete machine learning workflow designed to predict the most appropriate drug for a patient based on their clinical characteristics. The project demonstrates a clear and structured approach to data preprocessing, model training, evaluation, and interpretation using a Decision Tree Classifier.

---

## Project Overview

The goal of this project is to build a multiclass classification model capable of recommending one of five possible medications:

* Drug A
* Drug B
* Drug C
* Drug X
* Drug Y

Each patient in the dataset suffers from the same illness and responded to one of these medications during treatment. The model aims to learn the relationship between patient characteristics and drug outcomes to assist in future recommendations.

---

## Dataset Description

The dataset contains the following patient features:

* **Age**: Numeric variable.
* **Sex**: Categorical variable (F/M).
* **Blood Pressure (BP)**: Categorical variable (LOW, NORMAL, HIGH).
* **Cholesterol**: Categorical variable (NORMAL, HIGH).
* **Na_to_K**: Numeric variable representing the Sodium-to-Potassium ratio, a relevant biochemical indicator closely related to drug response.

**Target Variable**: The drug to which the patient responded.

This dataset is a standard example used to illustrate multiclass classification problems.

---

## Methodology

### 1. Data Preprocessing

* Encoding categorical features.
* Preparing feature matrix **X** and target vector **y**.

### 2. Model Training

A Decision Tree Classifier was trained using the entropy criterion for measuring information gain.

### 3. Cross-Validation

To ensure model stability and reduce the risk of overfitting, a 10-fold cross-validation strategy was applied. Mean accuracy was computed to evaluate general performance.

### 4. Feature Importance Analysis

The model provides insights into which clinical variables contribute most to the prediction. These importance scores help interpret how the decision rules are constructed.

### 5. Final Predictions

The trained model can be used to recommend an appropriate drug for new patients based on their clinical profile.

---

## Key Findings

* The model achieves strong performance across cross-validation folds, suggesting consistent and reliable predictions.
* The **Na_to_K** ratio is one of the most influential features in determining drug recommendation.
* Blood Pressure and Cholesterol categories also contribute significantly to the decision-making process.
* The Decision Tree structure allows full transparency and interpretability of each prediction.

---

## Conclusions

* The Decision Tree classifier successfully distinguishes between all drug categories in the dataset.
* Cross-validation confirms that the model generalizes well and is not overfitting.
* The dataset is well-structured for interpretability, making Decision Trees an appropriate choice for this type of problem.
* The importance of the Sodium-to-Potassium ratio highlights the clinical relevance of biochemical markers in treatment selection.

---

## How to Run the Project

1. Clone the repository:

```bash
git clone <your-repository-url>
```

2. Install project dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook
```

4. Run the cells to reproduce training, evaluation, and predictions.

---

## Repository Structure

```
├── data/                 # Dataset (if included)
├── notebook.ipynb        # Main analysis and model development
├── figures/              # Visualizations and plots
├── requirements.txt      # Python dependencies
└── README.md             # Project documentation
```

---

## Technologies Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Jupyter Notebook

---

## Author

**Iván Felipe Osorio – Data Scientist**
