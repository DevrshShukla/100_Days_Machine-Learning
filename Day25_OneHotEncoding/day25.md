# One-Hot Encoding in Machine Learning (Basic → Advanced)

## 1. What is One-Hot Encoding?

**One-Hot Encoding** is a technique used to convert **categorical (text) data** into **numerical format** so that machine learning models can understand it.

📌 Simple meaning:  
Each category is converted into a **separate column**, and the value is:
- `1` → if the category is present
- `0` → if the category is not present

---

## 2. Why Do We Need One-Hot Encoding?

Machine Learning models:
- ❌ Cannot work with text like `"Red"`, `"Blue"`, `"Delhi"`
- ✅ Work only with numbers

But converting categories to numbers **directly** can create **wrong meaning**.

👉 One-Hot Encoding avoids this problem by **not giving any order or priority**.

---

## 3. Very Simple Real-World Example

### Example: Favorite Color

| Color |
|------|
| Red |
| Blue |
| Green |

After One-Hot Encoding:

| Red | Blue | Green |
|----|------|-------|
| 1 | 0 | 0 |
| 0 | 1 | 0 |
| 0 | 0 | 1 |

✅ No ranking  
✅ No bias  
✅ Model treats all colors equally

---

## 4. When Should You Use One-Hot Encoding?

### ✅ Use One-Hot Encoding When:
- Categories have **NO natural order**
- All categories are **independent**

**Examples:**
- City names (Delhi, Mumbai, Chennai)
- Colors (Red, Blue, Green)
- Gender (Male, Female)
- Product category (Electronics, Clothing, Food)

---

### ❌ Do NOT Use One-Hot Encoding When:
- Categories have a **clear order**

**Examples:**
- Low, Medium, High
- Education levels
- Ratings

👉 In these cases, use **Ordinal Encoding**

---

## 5. Basic Manual Example (Understanding Concept)

```python
import pandas as pd

df = pd.DataFrame({
    "City": ["Delhi", "Mumbai", "Delhi", "Chennai"]
})

encoded_df = pd.get_dummies(df, columns=["City"])
print(encoded_df)
```
---
## Output:
```
   City_Chennai  City_Delhi  City_Mumbai
0             0           1            0
1             0           0            1
2             0           1            0
3             1           0            0
```
---
## 6. One-Hot Encoding Using Scikit-Learn

```python
from sklearn.preprocessing import OneHotEncoder
import pandas as pd

df = pd.DataFrame({
    "Browser": ["Chrome", "Firefox", "Edge"]
})

encoder = OneHotEncoder(sparse=False)
encoded = encoder.fit_transform(df[["Browser"]])

encoded_df = pd.DataFrame(
    encoded,
    columns=encoder.get_feature_names_out()
)

print(encoded_df)
```
---
## 7. Handling Multiple Categorical Columns (Advanced)

```python
data = {
    "City": ["Delhi", "Mumbai", "Chennai"],
    "Device": ["Mobile", "Laptop", "Tablet"]
}

df = pd.DataFrame(data)

encoder = OneHotEncoder(sparse=False)
encoded = encoder.fit_transform(df)

encoded_df = pd.DataFrame(
    encoded,
    columns=encoder.get_feature_names_out()
)

print(encoded_df)
```

## 8. Real-World Case Study

### Online Shopping Website

### Feature: Payment Method <br>
#### Values:

- UPI

- Credit Card

- Debit Card

- Net Banking

- After One-Hot Encoding:

- Payment_UPI

- Payment_CreditCard

- Payment_DebitCard

- Payment_NetBanking

📌 Model treats all payment methods equally


