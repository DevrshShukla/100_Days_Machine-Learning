# 📊 Exploratory Data Analysis (EDA) – Basic Questions Checklist

This guide answers the **most important questions you should ask before doing data analysis or machine learning**. It is written in **easy-to-understand terms** and is perfect for **GitHub, interviews, and projects**.

---

## 1️⃣ How big is the data?

### 🔍 What does this mean?

You need to know:

* How many **rows** (records) are there?
* How many **columns** (features) are there?

### 🧠 Why is it important?

* Helps decide which algorithms to use
* Large datasets need more memory and time

### 🧪 Code Example

```python
df.shape
```

### ✅ Output Example

```text
(891, 12)
```

➡️ 891 rows and 12 columns

---

## 2️⃣ How does the data look like?

### 🔍 What does this mean?

You want to **see the actual data values** to understand what kind of information is stored.

### 🧠 Why is it important?

* Detects weird or incorrect values
* Helps understand column meaning

### 🧪 Code Example

```python
df.head()
```

or

```python
df.sample(5)
```

---

## 3️⃣ All information about columns?

### 🔍 What does this mean?

You want to know:

* Column names
* Data types (number, text, etc.)
* Non-null values

### 🧠 Why is it important?

* ML models work only with numbers
* Helps detect wrong data types

### 🧪 Code Example

```python
df.info()
```

---

## 4️⃣ Any missing values?

### 🔍 What does this mean?

Check if some cells have **null / NaN values**.

### 🧠 Why is it important?

* Missing values can break models
* They must be filled or removed

### 🧪 Code Example

```python
df.isnull().sum()
```

### 🧠 Example Output

```text
Age      177
Cabin    687
```

➡️ These columns need cleaning

---

## 5️⃣ How does the data look mathematically?

### 🔍 What does this mean?

Get **statistical summary** of numerical columns.

### 🧠 Why is it important?

* Understand data distribution
* Detect outliers
* Compare mean vs median

### 🧪 Code Example

```python
df.describe()
```

### 📊 Metrics Explained Simply

* **mean** → average value
* **std** → spread of data
* **min / max** → range

---

## 6️⃣ Are there duplicate values?

### 🔍 What does this mean?

Check if the same row appears multiple times.

### 🧠 Why is it important?

* Duplicates can bias results
* ML models may overfit

### 🧪 Code Example

```python
df.duplicated().sum()
```

### 🧹 Remove duplicates

```python
df = df.drop_duplicates()
```

---

## 7️⃣ How is the correlation between columns?

### 🔍 What does this mean?

Correlation shows **how strongly two numerical columns are related**.

### 🧠 Why is it important?

* Helps in feature selection
* Detects multicollinearity

### 🧪 Code Example

```python
df.corr()
```