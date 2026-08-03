# 📘 Week 3 - Day 2: Linear Regression — Training, Coefficients & Evaluation

I built and evaluated my first regression model today, moving from theory 
into practice. The focus was on understanding how coefficients shape 
predictions, how metrics quantify performance, and whether the model 
outperforms a simple baseline.

---

## 📚 Linear Regression

Linear regression fits the **best line** through data points to predict a 
continuous outcome. It minimizes the error between predicted and actual 
values using the **least squares method**.

> 🧑‍🏫 I think of it as drawing the line that best explains the relationship 
between my features and target.

---

## 🎯 Coefficients & Intercept

- 📈 **Coefficient (slope)** — how much the target changes when a feature 
increases by 1 unit  
- ⚖️ **Intercept (bias)** — the predicted value when all features are 0  

Together, they define the regression equation.  
In the Diabetes dataset, the largest coefficients were **s1 (-931.49)** and 
**s5 (+736.20)**, showing opposite effects on disease progression.

---

## 📊 Evaluation Metrics

| **Metric** | **Meaning** | **Goal** |
|:---:|:---|:---:|
| MAE | Average absolute error | Lower = better |
| RMSE | Penalizes large errors | Lower = better |
| R² | Fraction of variance explained | Closer to 1 = better |

On the test set, my model achieved:  
- **MAE**: 42.79  
- **RMSE**: 53.85  
- **R²**: 0.453  

---

## 🧪 Hands-On Lab

I applied linear regression on the **Diabetes dataset**:

- 📥 Loaded the dataset and split into train/test sets  
- ⚙️ Trained a `LinearRegression` model  
- 🔍 Inspected coefficients and intercept  
- 📊 Evaluated with MAE, RMSE, and R²  
- 🛡️ Compared against a baseline model (predicting the mean)  
- 📈 Visualized predictions vs. actual values  

---

## 🛡️ Step 4: Baseline Comparison

To check if my model is truly useful, I compared it against a baseline 
that simply predicts the mean of the training target (`y_train`).

python
{

baseline_pred = np.full_like(y_test, y_train.mean(), dtype=float)

baseline_rmse = np.sqrt(mean_squared_error(y_test, baseline_pred))
rmse = np.sqrt(mean_squared_error(y_test, predictions))

print("RMSE:", rmse)
print("Baseline RMSE:", baseline_rmse) 

}

---

## 📈 Results

- 🔹 **Model RMSE**: 53.85
- 🔹 **Baseline RMSE**: 73.22 

---

## 📝 Final Reflection

My model’s RMSE of 53.85 is substantially lower than the baseline’s
73.22, representing about a 26% reduction in error.
Its R² score of 0.453 indicates it explains roughly 45% of the
variance in disease progression.

By contrast, the baseline’s R² is essentially 0 (slightly negative) —
expected since it predicts the training mean rather than the test mean.
This confirms that my regression model has captured a real relationship
between the features and disease progression, rather than just noise. 

---

## 🛠️ Tools

- Python  
- Pandas  
- Scikit-learn  
- Matplotlib  
- Jupyter Notebook
