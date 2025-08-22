# Titanic Survival Prediction using Logistic Regression

This project builds a **Logistic Regression** model to predict passenger survival on the Titanic dataset.  
It is implemented in a **Jupyter Notebook** and follows a complete ML pipeline: **data preprocessing, model training, evaluation, and feature importance analysis.**

---

## 📂 Dataset
The dataset used is the **Titanic training set** from [Kaggle’s Titanic: Machine Learning from Disaster competition](https://www.kaggle.com/c/titanic).  

File required: `train[1].csv`  
- Place it in the project root directory before running the notebook.

**Features included:**
- `Pclass` – Passenger class (1 = 1st, 2 = 2nd, 3 = 3rd)  
- `Sex` – Gender  
- `Age` – Passenger’s age  
- `SibSp` – Number of siblings/spouses aboard  
- `Parch` – Number of parents/children aboard  
- `Fare` – Ticket fare  
- `Embarked` – Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)  
- `Survived` – Target variable (0 = Did not survive, 1 = Survived)

---

## ⚙️ Project Workflow

1. **Data Preprocessing**
   - Dropped irrelevant columns: `PassengerId`, `Name`, `Ticket`, `Cabin`
   - Filled missing `Age` with mean
   - Filled missing `Embarked` with mode
   - Converted categorical features (`Sex`, `Embarked`) into numeric using Label Encoding
   - Applied StandardScaler for feature scaling

2. **Model Building**
   - Algorithm: **Logistic Regression** (`sklearn.linear_model.LogisticRegression`)
   - Train/Test Split: **80% training, 20% testing**

3. **Model Evaluation**
   - Accuracy Score
   - Classification Report (Precision, Recall, F1-score)
   - Confusion Matrix

4. **Feature Importance**
   - Extracted model coefficients
   - Ranked features by absolute weight to identify survival factors

---

## 📊 Results

- Logistic Regression achieved a baseline accuracy of around **80%**.
- **Most influential survival factors:**
  - **Sex** → Female passengers had much higher survival probability.
  - **Pclass** → Higher-class passengers survived more often.
  - **Fare** → Higher ticket fare correlated with higher survival.

---

## 🚀 Steps to Run the Project

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <Titanic-Survival-Prediction>```

### 2. Set up the environment
Install dependencies
```bash
pip install -r requirements.txt

