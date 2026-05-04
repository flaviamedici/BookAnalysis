# 📚 Text Analysis: *Miracle in the Andes*

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)
![License](https://img.shields.io/badge/License-Educational-lightgrey)
![Made With](https://img.shields.io/badge/Made%20with-Regex-orange)

---

## 🚀 Overview

This project performs **text analysis** on the book *Miracle in the Andes* using Python. It showcases how to:

* Process raw text data
* Extract patterns using regular expressions
* Analyze word frequency
* Derive insights from literary text

---

## ✨ Features

✅ Count total chapters
✅ Extract sentences containing specific keywords (`love`)
✅ Perform word frequency analysis
✅ Identify dominant themes through word usage

---

## 📂 Project Structure

```
.
├── miracle_in_the_andes.txt   # Input dataset
├── analysis.py                # Main analysis script
└── README.md                 # Documentation
```

---

## ⚙️ How It Works

### 📖 Load the Book

```python
with open("miracle_in_the_andes.txt", "r", encoding="utf-8") as file:
    book = file.read()
```

---

### 🔢 Chapter Detection

Uses regex to identify chapter headings:

```python
pattern = re.compile("Chapter [0-9]+")
chapters = re.findall(pattern, book)
```

📊 **Total Chapters:** `10`

---

### ❤️ Extract Sentences with "love"

```python
pattern = re.compile("[A-Z]{1}[^.]*[^a-zA-Z]love[^a-zA-Z]+[^.]*.")
findings = re.findall(pattern, book)
```

📊 **Occurrences:** `67 sentences`

---

### 📊 Word Frequency Analysis

```python
pattern = re.compile("[a-zA-Z]+")
words = re.findall(pattern, book.lower())
```

---

## 📈 Top 20 Most Frequent Words

```
the     ██████████████████████████████████████ 5346
and     ████████████████████ 2795
i       ███████████████████ 2729
to      █████████████████ 2400
of      ██████████████ 2060
a       ████████████ 1566
was     ███████████ 1430
in      ███████████ 1419
we      █████████ 1226
my      █████████ 1169
that    ████████ 1001
he      ████████ 946
had     ████████ 941
it      ███████ 800
for     ██████ 705
as      ██████ 700
but     ██████ 679
with    █████ 632
me      █████ 617
on      █████ 576
```

---

## 📊 Insights

### 🔍 Language Patterns

* Common stopwords dominate (expected in natural language)
* First-person narration is prominent (`I`, `we`, `my`)

### ❤️ Theme Detection

The frequent appearance of **"love" (83 times overall, 67 sentences)** highlights:

* Emotional resilience
* Family connection
* Survival motivation
* Spiritual reflection

---

## ▶️ How to Run

```bash
git clone <your-repo-url>
cd text-analysis-project
python analysis.py
```

---

## 📌 Future Improvements

* 🔍 Remove stopwords for cleaner insights
* 📊 Add visualizations (matplotlib / seaborn)
* ☁️ Generate word clouds
* 🧠 Apply NLP (NLTK, spaCy)
* 📈 Sentiment analysis by chapter

---

## 🖼️ Example Future Visualization

*(You can add this later with matplotlib)*

```
Word Frequency Distribution (Concept)

the  | ##############################
and  | ##################
i    | #################
love | #####
```

---

## 🤝 Contributing

Contributions are welcome!
Feel free to fork the repo and submit a pull request.

---

## 📜 License

This project is intended for **educational purposes only**.

---

## ⭐ If you found this useful

Give the repo a star ⭐ and share your improvements!



Jupyter lab

Install: 
```
py 3.14 -m pip install jupyterlab
```
Go to directory that Juyter is installed
```
py -m jupyterlab
```
Start notebook in certain directory
```
py -m jupyterlab --notebook-dir=<path/to/project/directory>
```
