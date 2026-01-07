# 📊 Exploratory Data Analysis (EDA) – Univariate Analysis

## 📅 Day 18 – EDA Using Univariate Analysis

Exploratory Data Analysis (EDA) is the process of **understanding data before applying machine learning or statistics**.  
Univariate Analysis means **analyzing only ONE variable (column) at a time**.

---

## 🔹 Types of Data in Univariate Analysis

### 1️⃣ Categorical Data
Categorical data represents **categories or labels**.

### Examples:
- Gender (Male / Female)
- Department (HR, IT, Sales)
- Payment Mode (Cash, UPI, Card)

---

### 📌 A) Count Plot
A **Count Plot** shows **how many times each category appears**.

#### Purpose:
- To check **frequency of each category**
- To compare category distribution

#### Example:
```python
import seaborn as sns
sns.countplot(x='Gender', data=df)
```

### 📌 B) Pie Chart

#### A Pie Chart shows percentage distribution of categories.

#### Purpose:

- To understand proportion

- Easy visual comparison

#### Example:
```python
df['Gender'].value_counts().plot.pie(autopct='%1.1f%%')
```

---

### 2️⃣ Numerical Data

---

- Numerical data represents numbers.

#### Examples:

- Age

- Salary

- Marks

- Height

### 📊 Histogram

- A Histogram shows the distribution of numerical data.

### Purpose:

- Understand data spread

- Identify skewness

- Detect outliers

### Example:
```python
plt.hist(df['Age'])
plt.xlabel('Age')
plt.ylabel('Frequency')
```

### 📈 Distribution Plot (Distplot)

#### A Distribution Plot shows:

### 1. Histogram

- Probability Density Curve (PDF)

### Purpose:

- Understand data distribution

- Check normality
```python
sns.distplot(df['Salary'])
```

### 📦 Box Plot (Very Important)

#### A Box Plot visually shows:

- Minimum

- Maximum

- Median

- Quartiles

- Outliers

### 🧠 Understanding Box Plot Terms (Easy Explanation) <br>
### 📌 Quartiles

Quartiles divide data into 4 equal parts.

Term 	Meaning<br>
**Q1	25th percentile**<br>
**Q2	50th percentile (Median)**<br>
**Q3	75th percentile**<br><br>
### 📌 Inter Quartile Range (IQR)<br>
### IQR = Q3 − Q1<br>


It shows middle 50% of the data.

### 📌 Minimum & Maximum (Whiskers)
Minimum = Q1 − 1.5 × IQR <br>
Maximum = Q3 + 1.5 × IQR


- Values outside this range are Outliers.

### 📌 Outliers

### Outliers are extreme values that:

- Are very high or very low

- Can affect model performance

## Example:

- Salary = ₹10,000,000 when most salaries are ₹30,000–₹80,000

### 📊 Box Plot Example:
```python
plt.boxplot(df['Salary'])
plt.show()
```