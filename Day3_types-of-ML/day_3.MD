# 📘 Types of Machine Learning

Machine Learning (ML) is a subset of Artificial Intelligence (AI) that allows systems to **learn from data and improve automatically** without being explicitly programmed.

            🤖 Machine Learning
                     │
    ┌────────────────┼────────────────┐
    │                │                │
✅ Supervised 🔍 Unsupervised 🎮 Reinforcement
│ │ │
┌────┴────┐ ┌─────┼─────┐ │
│ │ │ │ │ │
📊Regression 🏷Classification 🧩Clustering 🔻Dimensionality 🔗Association 🎯Reward-based

Based on the learning approach, Machine Learning is mainly divided into **three categories**:

1. **Supervised Learning**
2. **Unsupervised Learning**
3. **Reinforcement Learning**

---

## 🧠 1. Supervised Learning

In **Supervised Learning**, the model is trained on **labeled data**.  
This means **both input and correct output are already known**.

📌 *Think of it like learning with a teacher.*

### 🔹 Types of Supervised Learning

#### ✅ a) Classification
- Output is **categorical** (classes or labels)

**Examples:**
- Email → *Spam / Not Spam*
- Image → *Cat / Dog*
- Student result → *Pass / Fail*

📍 **Real-life example:**  
Gmail classifying emails into *Primary*, *Spam*, or *Promotions*

---

#### ✅ b) Regression
- Output is **continuous (numeric value)**

**Examples:**
- Predicting **house price**
- Predicting **temperature**
- Predicting **salary**

📍 **Real-life example:**  
Predicting house price based on size, location, and number of rooms

---

## 🔍 2. Unsupervised Learning

In **Unsupervised Learning**, the data is **unlabeled**.  
The model finds **patterns or structures** on its own.

📌 *Think of it like learning without a teacher.*

### 🔹 Types of Unsupervised Learning

#### ✅ a) Clustering
- Groups similar data points together

**Examples:**
- Customer segmentation
- Grouping similar products
- Social media friend suggestions

📍 **Real-life example:**  
E-commerce websites grouping customers based on buying behavior

---

#### ✅ b) Dimensionality Reduction
- Reduces the number of features while keeping important information

**Examples:**
- Reducing image size
- Data visualization
- Faster model training

📍 **Real-life example:**  
Compressing large datasets for easier analysis

---

#### ✅ c) Association
- Finds relationships between items

**Examples:**
- Market basket analysis
- Recommendation systems

📍 **Real-life example:**  
“People who bought **milk** also bought **bread**”

---

## 🎮 3. Reinforcement Learning

In **Reinforcement Learning**, an **agent learns by trial and error**.  
The agent receives **rewards or penalties** based on actions.

📌 *Think of it like training a pet.*

### 🔹 Key Components
- **Agent** → Learner (AI)
- **Environment** → World where agent acts
- **Reward** → Feedback

### 🔹 Examples
- Game playing AI (Chess, PUBG bots)
- Self-driving cars
- Robot navigation

📍 **Real-life example:**  
Teaching a robot to walk — correct step → reward, wrong step → penalty

---

## 📊 Comparison Table

| Learning Type | Data Type | Output | Example |
|--------------|----------|--------|--------|
| Supervised | Labeled | Known | Spam detection |
| Unsupervised | Unlabeled | Unknown | Customer grouping |
| Reinforcement | Reward-based | Actions | Game AI |

---

## 🧾 Summary

- **Supervised Learning** → Learn with labeled data
- **Unsupervised Learning** → Learn patterns without labels
- **Reinforcement Learning** → Learn by rewards and penalties

This classification helps choose the **right ML approach** based on the problem and data available.

---

📌 *Part of the **100 Days of Machine Learning** series*
