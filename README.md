# 🚢 Titanic Survival Predictor using Logistic Regression

This project uses logistic regression to predict passenger survival on the Titanic based on various features such as age, fare, passenger class, and more. The model is built using Python, pandas, and scikit-learn, and includes exploratory data analysis, preprocessing, model training, evaluation, and comparison with Random Forest.

---

## 📁 Dataset

- Source: [Kaggle Titanic Dataset](https://www.kaggle.com/competitions/titanic/data)
- Columns used:
  - `Pclass` (Passenger class)
  - `Sex` (encoded)
  - `Age` (filled with mean)
  - `SibSp`, `Parch` (family aboard)
  - `Fare` (filled with median)
  - `Embarked` (encoded)

---

## 🧪 Preprocessing Steps

- Visualized and filled missing values (`Age`, `Fare`).
- Dropped high-cardinality or irrelevant columns (`Cabin`, `Name`, `Ticket`, `PassengerId`).
- Encoded categorical columns (`Sex`, `Embarked`) using one-hot encoding.
- Standardized `Pclass` and `Fare` using `StandardScaler`.
- Dropped any remaining missing data.

---

## ⚙️ Model Training

### Logistic Regression

- Split into training and test sets (`70/30`).
- Trained with `LogisticRegression()` from `sklearn`.

### Random Forest (for comparison)

- Trained `RandomForestClassifier` with different `n_estimators` using `cross_val_score`.
- Plotted accuracy vs. number of trees.

---

## 📊 Evaluation

### Logistic Regression Performance:

precision recall f1-score support

0 0.82 0.91 0.86 163
1 0.84 0.68 0.75 104

accuracy 0.82 267

- **Confusion Matrix**:
  [[149 14]
[ 33 71]]

- **Interpretation**:
- Good precision and accuracy.
- Slightly lower recall for class `1` (survived), indicating some survivors were misclassified.

---

## 📈 Visualization

- Heatmaps for missing values and correlations.
- Pairplot and barplots for class distributions.
- Accuracy vs. estimator count plot for Random Forest tuning.

---

## 📦 Libraries Used

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `sklearn` (LogisticRegression, RandomForestClassifier, StandardScaler, metrics)

---

## 🚀 Future Work

- Improve recall by tuning threshold or using class weights.
- Try more advanced models (XGBoost, SVM).
- Deploy model as a web app using Streamlit or Flask.

---

## 🧠 Author

**Milkiyas Weldesenbet Gebrehiwet**  
Passionate about building data-driven and automated systems.

## 📜 License

MIT License - use and modify freely.
