## 1️⃣ Title: Bivariate and Multivariate Analysis

### Markdown Cell

```md
## Bivariated and Multivariated Analysis
```

### Explanation

This notebook focuses on **Exploratory Data Analysis (EDA)** techniques where:

* **Bivariate Analysis** → relationship between **two variables**
* **Multivariate Analysis** → relationship between **three or more variables**

These analyses help understand patterns, trends, and dependencies in data before building ML models.

---

## 3️⃣ Importing Libraries

### Code Cell

```python
import numpy as np
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
```

### Explanation

| Library    | Purpose                    |
| ---------- | -------------------------- |
| NumPy      | Numerical operations       |
| Pandas     | Data handling & analysis   |
| Seaborn    | Statistical visualizations |
| Matplotlib | Plot customization         |

Seaborn is built on top of Matplotlib and simplifies complex plots.

---

## 4️⃣ Loading Datasets

### Code Cell

```python
titanic = pd.read_csv('train.csv')
tips = sns.load_dataset('tips')
flights = sns.load_dataset('flights')
iris = sns.load_dataset('iris')
```

### Explanation

Multiple datasets are loaded to demonstrate different EDA techniques:

| Dataset | Purpose                               |
| ------- | ------------------------------------- |
| Titanic | Survival & demographics               |
| Tips    | Restaurant bills & tips               |
| Flights | Time-series passenger data            |
| Iris    | Classic ML dataset for classification |

Using different datasets helps understand how plots vary with data types.

---

## 5️⃣ Dataset Preview

### Code Cells

```python
titanic.sample(5)
tips.sample(5)
```

### Explanation

* `sample(5)` randomly displays rows
* Helps inspect column names, data types, and values
* Crucial before selecting visualization techniques

---

## 6️⃣ Scatter Plot (Numerical vs Numerical)

### Concept Used

**Bivariate Analysis**

### Purpose

Used to analyze the relationship between **two numerical variables**.

### Example Insight

In Titanic or Tips dataset:

* Total bill vs Tip amount
* Age vs Fare

If points show an upward trend → positive correlation.

---

## 7️⃣ Bar Plot (Categorical vs Numerical)

### Concept Used

**Bivariate Analysis**

### Purpose

* Shows average or total numerical values per category

### Example

* Average fare per passenger class
* Average tip by day

Bar height represents aggregated statistics like mean or sum.

---

## 8️⃣ Box Plot (Categorical vs Numerical)

### Concept Used

**Bivariate Analysis**

### Purpose

* Shows data distribution
* Identifies outliers
* Compares spread across categories

### Example

* Fare distribution by passenger class

Box plot components:

* Median
* Quartiles
* Whiskers
* Outliers

---

## 9️⃣ Heatmap (Categorical vs Categorical)

### Concept Used

**Bivariate / Multivariate Analysis**

### Explanation

Heatmaps visualize frequency or correlation using colors.

### Example

```python
pd.crosstab(titanic['Pclass'], titanic['Survived'])
```

Darker colors → higher values

Used to understand relationships between categories.

---

## 🔟 Cluster Map

### Markdown Cell

```md
### 6. Cluster Map
**[ Categorical - Categorical ]**
```

### Code Cell

```python
sns.clustermap(x, annot=True, fmt='d')
```

### Explanation

* Extends heatmaps
* Automatically clusters rows and columns
* Useful for pattern discovery

Real-world use:

* Customer segmentation
* Market basket analysis

---

## 1️⃣1️⃣ Pair Plot

### Markdown Cell

```md
### 7. Pair Plot
**[ Numerical - Numerical ]**
```

### Code Cell

```python
sns.pairplot(iris, hue='species')
```

### Explanation

* **Multivariate Analysis tool**
* Plots every numerical feature against others
* Color (`hue`) separates categories

Used to:

* Identify feature separability
* Detect correlations
* Check class overlap

Very useful before classification models.

---

## 1️⃣2️⃣ Line Plot (Time Series)

### Code Cell

```python
new = flights.groupby('month').sum().reset_index()
sns.lineplot(x='month', y='passengers', data=new)
```

### Explanation

* Groups passengers by month
* Line plot shows trend over time

Used for:

* Time-series analysis
* Trend detection
* Seasonal behavior

Example:
✈️ Increase in passengers during holiday months

---

## ✅ Key Takeaways

* Bivariate analysis helps understand **pairwise relationships**
* Multivariate analysis reveals **complex interactions**
* Visual EDA is essential before ML modeling

---

## 📌 Real-World Importance

| Field      | Use                        |
| ---------- | -------------------------- |
| Healthcare | Disease risk analysis      |
| Finance    | Credit scoring             |
| Retail     | Sales & demand forecasting |
| ML         | Feature selection          |

---