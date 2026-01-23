# Ordinal Encoding in Machine Learning (Basic → Advanced)

## 1. What is Ordinal Encoding?

**Ordinal Encoding** is a technique used to convert **categorical (text) data** into **numbers**,  
**only when the categories have a natural order or ranking**.

📌 Simple meaning:  
If categories can be arranged from **low → high**, we replace them with numbers that keep this order.

---

## 2. Why Ordinal Encoding is Needed?

Machine Learning models:
- ❌ Cannot understand text
- ✅ Understand numbers

But converting text to numbers must be done **carefully**.

Ordinal Encoding is useful because:
- It keeps **ranking information**
- It uses **less memory** than One-Hot Encoding
- It helps models understand **progression or levels**

---

## 3. Very Simple Real-World Example

### Example: Movie Ratings

| Rating Text | Meaning |
|------------|--------|
| Bad        | Worst |
| Average    | Okay |
| Good       | Better |
| Excellent  | Best |

Ordinal Encoding:

| Rating | Encoded Value |
|------|--------------|
| Bad | 1 |
| Average | 2 |
| Good | 3 |
| Excellent | 4 |

✅ Order is preserved  
⚠️ Numbers show ranking, **not exact distance**

---

## 4. When Should You Use Ordinal Encoding?

### ✅ Use Ordinal Encoding When:
- Categories have **clear order**
- Ranking matters

**Examples:**
- Education level (School < College < Degree)
- Customer satisfaction (Low < Medium < High)
- Clothing size (S < M < L < XL)
- Product quality (Poor < Average < Good)

---

### ❌ Do NOT Use Ordinal Encoding When:
- No natural order exists

**Examples:**
- City names
- Colors
- Country names
- Product IDs

👉 In these cases, use **One-Hot Encoding**

---

## Ordinal Encoding Using Scikit-Learn
**categories ensures the correct order is used**

```python
from sklearn.preprocessing import OrdinalEncoder
import pandas as pd

df = pd.DataFrame({
    "Quality": ["Low", "Medium", "High", "Medium"]
})

encoder = OrdinalEncoder(
    categories=[["Low", "Medium", "High"]]
)

df["Quality_Encoded"] = encoder.fit_transform(df[["Quality"]])
print(df)
```
---
## Advanced Example: Multiple Ordinal Columns

```python
data = {
    "Education": ["Graduate", "Secondary", "Post-Graduate"],
    "Satisfaction": ["High", "Low", "Medium"]
}

df = pd.DataFrame(data)

encoder = OrdinalEncoder(
    categories=[
        ["Primary", "Secondary", "Graduate", "Post-Graduate"],
        ["Low", "Medium", "High"]
    ]
)

encoded_data = encoder.fit_transform(df)
encoded_df = pd.DataFrame(encoded_data, columns=df.columns)
print(encoded_df)
```
---
## Real-World Case Study

### Customer Feedback System

**Feedback Levels:**

- Very Bad

- Bad

- Neutral

- Good

- Excellent