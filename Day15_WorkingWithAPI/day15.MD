# 📌 Fetching Data From an API (100 Days of Machine Learning — Day 17)

**YouTube Link:** https://youtu.be/roTZJaxjnJc  
**Topic:** How to fetch data from an API and save it into a Pandas DataFrame  
**Skills Covered:** APIs, HTTP Requests, JSON & parsing, Python, Pandas  
**Difficulty Level:** Beginner – Intermediate  
**Interview Focus:** Practical data acquisition for ML pipelines

---

## 💡 1. What Is an API?

**API (Application Programming Interface)**  
An API is a **standard way for applications to communicate** with each other over the internet.  
In data science and ML, APIs let you **pull live structured data** (like JSON) from a database or platform.

🔎 Think of an API like an interface at a restaurant:  
- You (client) request a dish  
- The kitchen (server/API) sends it back in a format you can eat (JSON, XML etc.)

📊 Real-world examples:  
- 🇮🇳 Pulling movie data from TMDB (The Movie Database)  
- 💰 Fetching financial market prices  
- 📍 Getting weather info dynamically  
- 🚗 Real-time traffic data

---

## 🧠 2. How Does an API Work?

General flow:

1. **Send HTTP GET request**  
   You ask the API for specific data.
2. **Receive HTTP Response**  
   Server returns data (often JSON).
3. **Parse the JSON response**  
   Convert it into Python data structures.
4. **Store in DataFrame**  
   Use **Pandas** to tabulate and inspect.

---

## 🛠 3. Tools & Libraries

| Tool | Purpose |
|------|---------|
| `requests` | Send HTTP GET/POST requests |
| `json` | Parse JSON |
| `pandas` | Manipulate and store structured table data |

## 🧑‍💻 Real World Example
### 🚀 Building a Movie Analytics Table

### You can fetch:

- Movie titles

- Ratings

- Release dates

- Genre IDs

### Then:

- Visualize trending movies.

- Feed into recommendation systems.

- Build dashboards.

## ❗ Common Interview Questions
### ❓ Q: What’s the difference between web scraping and API?

- API

- Structured data

- Legal & faster

- Web Scraping

- Parse HTML

- Fragile / slower

### ❓ Q: What status code means success?

- 200 OK — request was successful.

### ❓ Q: What format do APIs return?

- Mostly JSON — easy to parse with Python.