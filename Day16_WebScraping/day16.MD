# 📌 Web Scraping & Creating a Pandas DataFrame  
**YouTube Link:** https://youtu.be/8NOdgjC1988  
**Topic:** How to fetch data from a website using web scraping and store it in a Pandas DataFrame  
**Skills Covered:** Web Scraping, HTML Parsing, Requests, BeautifulSoup, Pandas  
**Difficulty Level:** Beginner – Intermediate  
**Interview Focus:** Data acquisition from websites, HTML parsing, working with structured data

---

## 🔍 1. What Is Web Scraping?

**Web Scraping** is the process of automatically extracting data from web pages shown in a browser.  
It’s useful when data is not available through an API or downloadable format and lives in plain HTML. :contentReference[oaicite:1]{index=1}

💡 **Analogy:** Think of a bot that reads all the tables on a website just like a human would — but much faster and without clicking manually.

📌 **Common Use Cases:**
- 📊 Scraping reviews from e-commerce sites  
- 🍽 Collecting recipes from food blogs  
- 🏙 Scraping hotel or travel data  
- 💼 Scraping job listings

---

## 🛠 2. Tools We Use

| **Library**      | **Purpose** |
|------------------|-------------|
| `requests`       | Download web page HTML |
| `BeautifulSoup`  | Parse HTML and extract specific elements |
| `pandas`         | Store and manipulate data in table format |

---

## 📘 3. List of Functions

| 🔢 | **Function / Property** | **Example**                                        | **Easy Definition (Simple Words)**                                                  |
| -- | ----------------------- | -------------------------------------------------- | ----------------------------------------------------------------------------------- |
| 1  | `BeautifulSoup()`       | `soup = BeautifulSoup(html, 'html.parser')`        | Converts raw HTML into a structured Python object so we can search and extract data |
| 2  | `find()`                | `soup.find('div', class_='price')`                 | Finds **only the first matching element**                                           |
| 3  | `find_all()`            | `soup.find_all('span', class_='tag-item')`         | Finds **all matching elements** and returns a list                                  |
| 4  | `select()`              | `soup.select('span.tag-item')`                     | Finds elements using **CSS selectors** (most flexible method)                       |
| 5  | `select_one()`          | `soup.select_one('div.price')`                     | CSS selector version of `find()` (returns first match)                              |
| 6  | `.text`                 | `tag.text`                                         | Extracts only the visible text from a tag                                           |
| 7  | `.get_text()`           | `tag.get_text(strip=True)`                         | Extracts clean text and removes extra spaces                                        |
| 8  | `.attrs`                | `tag.attrs`                                        | Returns **all attributes** of an HTML tag as a dictionary                           |
| 9  | `.get()`                | `tag.get('href')`                                  | Safely extracts a **specific attribute value**                                      |
| 10 | `find_next()`           | `tag.find_next('span')`                            | Finds the **next matching element** after the current one                           |
| 11 | `find_previous()`       | `tag.find_previous('div')`                         | Finds the **previous matching element** before the current one                      |
| 12 | `.parent`               | `tag.parent`                                       | Returns the **immediate parent tag**                                                |
| 13 | `.parents`              | `list(tag.parents)`                                | Returns **all parent tags** up to `<html>`                                          |
| 14 | `.children`             | `list(tag.children)`                               | Returns **direct child elements only**                                              |
| 15 | `.descendants`          | `list(tag.descendants)`                            | Returns **all nested children** (children + grandchildren)                          |
| 16 | `.prettify()`           | `print(soup.prettify())`                           | Formats HTML nicely for **easy debugging**                                          |
| 17 | `find_all(text=True)`   | `soup.find_all(text=True)`                         | Extracts **only text nodes** from the page                                          |
| 18 | `regex with find_all()` | `soup.find_all('div', class_=re.compile('price'))` | Finds elements using **partial or dynamic class names**                             |
| 19 | `decompose()`           | `tag.decompose()`                                  | Completely **removes a tag from HTML memory**                                       |
| 20 | `extract()`             | `removed = tag.extract()`                          | Removes tag but **keeps it stored for later use**                                   |

