# Term Deposit Prediction

This project predicts whether a bank customer will subscribe to a **term deposit** based on marketing campaign data. It is a **binary classification problem** solved using **Logistic Regression**.

The objective is to help banks improve marketing efficiency by identifying potential subscribers in advance.

---

## Objective

- Predict customer subscription (`yes` / `no`)
- Handle class imbalance effectively
- Improve recall for potential subscribers
- Build an interpretable classification model

---

## Dataset

The dataset is derived from the **Bank Marketing Dataset**, which contains information from direct marketing campaigns of a bank.

### Target Variable
- `y`
  - `yes` → Customer subscribes to term deposit
  - `no` → Customer does not subscribe

### Important Note
The CSV file is **semicolon (`;`) separated**, not comma-separated.

---

## Features

The dataset includes:
- Customer demographics (age, job, education, marital status)
- Contact information (contact type, month, day)
- Campaign details (duration, number of contacts)
- Economic indicators

---

## Approach

1. Load the dataset using the correct delimiter
2. Encode categorical variables
3. Scale numerical features
4. Handle class imbalance using `class_weight`
5. Train Logistic Regression model
6. Tune decision threshold to improve recall
7. Evaluate using appropriate metrics

---

## Model

- **Logistic Regression**
  - Interpretable
  - Supports class weighting
  - Suitable for binary classification

---

## Evaluation Metrics

- Accuracy
- Precision
- Recall (primary focus)
- F1-score
- Confusion Matrix

Recall is prioritized because missing a potential subscriber is more costly than contacting a non-interested customer.

---

## How to Run

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Train Model
```python
model.fit(X_train, y_train)
```

### Make Predictions
```python
y_pred = model.predict(X_test)
```

---

## Repository Structure

```
Term-Deposit-Predict/
│
├── train.csv
├── test.csv
├── README.md
├── requirements.txt
└── notebooks / scripts
```

---

## Conclusion

This project demonstrates how Logistic Regression, combined with class weighting and threshold tuning, can effectively solve real-world marketing prediction problems.

---

## License

This project is open-source and intended for educational use.

