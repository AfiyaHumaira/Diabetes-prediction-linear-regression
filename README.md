
# 🩺 Diabetes Prediction using Linear Regression

This project uses **Linear Regression** to predict whether a patient is diabetic (Outcome = 1) or not (Outcome = 0) based on various medical features.

---

## 📁 Dataset

- Source: `diabetes.csv`
- Contains 768 records with 8 features and 1 label (`Outcome`).

| Feature               | Description                           |
|------------------------|---------------------------------------|
| Pregnancies           | Number of times pregnant              |
| Glucose               | Plasma glucose concentration          |
| BloodPressure         | Diastolic blood pressure              |
| SkinThickness         | Triceps skin fold thickness           |
| Insulin               | 2-Hour serum insulin                  |
| BMI                   | Body mass index                       |
| DiabetesPedigreeFunction | Diabetes pedigree function        |
| Age                   | Age in years                          |
| Outcome               | 1 = diabetic, 0 = not diabetic        |

---

## 🧪 Preprocessing Steps

1. **Replace 0 values** in:  
   `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, and `BMI` with the **column median**.

2. **Replace first row's glucose** with the **maximum** glucose value from the dataset.

3. For all rows with the **minimum age**, replace their glucose values with the **minimum** glucose value.

---

## 🧠 Model Used

- **Linear Regression** from `sklearn.linear_model`
- Prediction output was **rounded** to 0 or 1 to perform binary classification.

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Confusion Matrix**
- **Precision**
- **Recall**
- **F1-Score**

Sample Output:
```text
Accuracy: 0.76
Precision: 0.79
Recall: 0.74
F1 Score: 0.76
Confusion Matrix:
[[85, 15],
 [13, 57]]


▶️ Running Process
✅ Option 1: Google Colab

    Open Google Colab

    Upload:

        diabetes.csv

        or open the shared notebook: diabetes-linear-regression.ipynb

    Run all cells step by step:

        Preprocessing the dataset

        Splitting into training/test sets

        Training the Linear Regression model

        Rounding predictions to 0 or 1

        Evaluating model performance

✅ Option 2: Local Jupyter Notebook

    Clone the repository:

git clone https://github.com/yourusername/diabetes-prediction-linear-regression.git
cd diabetes-prediction-linear-regression

Install requirements:

pip install pandas numpy scikit-learn

Run the notebook:

jupyter notebook diabetes-linear-regression.ipynb
