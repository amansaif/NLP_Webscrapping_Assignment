# NLP_Webscrapping_Assignment# Web Scraping and Data Extraction using BeautifulSoup

NLP Lab practical — scrapes course details (name, rating, original price, discounted price, thumbnail image) from the [GeeksforGeeks Courses](https://www.geeksforgeeks.org/courses) page and stores the result in a structured CSV file.

## 📌 Overview

This notebook demonstrates the **Data Acquisition** stage of an NLP pipeline:

```
Data Acquisition → HTML Parsing → Data Extraction → Data Structuring → CSV Export
```

It uses `requests` to fetch the webpage and `BeautifulSoup` (with the `lxml` parser) to parse the HTML and pull out the required fields, which are then combined into a `pandas` DataFrame and exported to CSV.

## 🛠️ Tech Stack

- Python 3
- [Requests](https://docs.python-requests.org/) — fetch the webpage
- [BeautifulSoup4](https://www.crummy.com/software/BeautifulSoup/) + `lxml` — parse HTML
- [Pandas](https://pandas.pydata.org/) / NumPy — structure and handle data

## 📂 Files

| File | Description |
|---|---|
| `2401201145_Mohd_Aman.ipynb` | Main Jupyter notebook with the full scraping workflow |
| `GFG_COURSES.csv` | Output CSV generated after running the notebook |

## ⚙️ How to Run

1. Clone this repository
   ```bash
   git clone <repo-url>
   cd <repo-name>
   ```
2. Install the dependencies
   ```bash
   pip install pandas numpy requests beautifulsoup4 lxml
   ```
3. Open the notebook and run all cells
   ```bash
   jupyter notebook 2401201145_Mohd_Aman.ipynb
   ```
4. The scraped data will be saved as `GFG_COURSES.csv` in the same folder.

## 🔍 What the Notebook Does

1. Sends an HTTP GET request to the GeeksforGeeks Courses page (with a browser-like `User-Agent` header to avoid being blocked)
2. Parses the HTML response using BeautifulSoup + lxml
3. Extracts:
   - Course names (`<h4>` tags)
   - Course ratings (`<span class="urw-din">`)
   - Original & discounted prices (`<div class="courseListingPage_priceTags__PXTc9">`)
   - Course thumbnail image URLs (`<img alt="course thumbnail">`)
4. Combines everything into a single Pandas DataFrame
5. Exports the DataFrame to `GFG_COURSES.csv`

## ✅ Output

A CSV file with the following columns:

| Course Name | Course Rating | Original Price | Discount Price |
|---|---|---|---|

## 👤 Author

**Mohd Aman**
BCA (AI & Data Science), K.R. Mangalam University
Roll No: 2401201145
