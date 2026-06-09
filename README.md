# 🔐 Password Strength Prediction using Machine Learning

A Machine Learning project that predicts whether a password is **Weak (0)**, **Medium (1)**, or **Strong (2)** using NLP and classification algorithms.

## 📊 Dataset

- **670K+ passwords**
- Features:
  - `password` → Password text
  - `strength` → Password strength label (0, 1, 2)

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- TF-IDF Vectorizer
- Logistic Regression
- Gradient Boosting Classifier

## ⚙️ Feature Engineering

Passwords are converted into character-level TF-IDF vectors:

```python
vec = TfidfVectorizer(tokenizer=character)
x = vec.fit_transform(passwords)
```

Feature Matrix Shape:

```text
(669639, 153)
```

## 🤖 Models & Results

| Model | Accuracy |
|---------|----------|
| Logistic Regression | 81.86% |
| Gradient Boosting | 91.34% |

🏆 **Best Model:** Gradient Boosting Classifier

## 🚀 Usage

```bash
python train.py
```

Example:

```text
Input: tanishqa#$__672903
Output: Strong Password (2)
```

## 📌 Future Improvements

- XGBoost / LightGBM
- Hyperparameter Tuning
- Streamlit Web App Deployment
