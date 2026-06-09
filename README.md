# 🔐 Password Strength Prediction using Machine Learning

A Machine Learning and NLP project that predicts whether a password is **Weak (0)**, **Medium (1)**, or **Strong (2)** using character-level TF-IDF features.

## 📊 Dataset

* 670K+ passwords
* Features:

  * `password` → Password text
  * `strength` → Password strength label (0, 1, 2)

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Scikit-Learn
* TF-IDF Vectorizer
* Logistic Regression
* Linear SVM (LinearSVC)
* Gradient Boosting Classifier

## ⚙️ Feature Engineering

```python
def character(password):
    return [char for char in password]

vec = TfidfVectorizer(tokenizer=character)
X = vec.fit_transform(passwords)
```

**Feature Matrix Shape:** `(669639, 153)`

## 🤖 Model Performance

| Model                        | Accuracy |
| ---------------------------- | -------- |
| Logistic Regression          | 81.86%   |
| Linear SVM                   | 80.90%   |
| Gradient Boosting Classifier | 91.34%   |

🏆 **Best Model:** Gradient Boosting Classifier

## 🚀 Run

```bash
pip install -r requirements.txt
python train.py
```

## 💡 Example

```text
Input:
tanishqa#$__672903

Output:
Strong Password (2)
```

## 📌 Future Improvements

* XGBoost / LightGBM
* Hyperparameter Tuning
* Streamlit Deployment
* Deep Learning Models

⭐ If you found this project useful, consider giving it a star.
