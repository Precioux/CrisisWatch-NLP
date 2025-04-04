
# 🧠 CrisisWatch-NLP

> Crisis Detection using NLP, Sentiment Analysis & Geospatial Mapping

**CrisisWatch-NLP** is a social media analysis tool. The goal is to build a pipeline that detects, analyzes, and visualizes crisis-related discussions (e.g., suicidality, mental health distress, substance use) from Reddit using advanced NLP techniques and geospatial tools.

---

## 📌 Objectives

- 🔍 Extract crisis-related posts from Reddit based on keyword filters and location cues
- 💬 Analyze sentiment using VADER
- 🧠 Assess crisis risk levels using BERT-based semantic similarity
- 🗺️ Visualize regional distress patterns on an interactive map

---

## ✅ Tasks Completed

### 📥 Task 1: Social Media Data Extraction & Preprocessing

- Collected posts via Reddit’s `praw` API from mental health subreddits
- Filtered posts using a keyword list (e.g., “i want to die”, “relapse”)
- Cleaned text using `nltk` (stopwords, punctuation, emojis removed)
- Output: `raw_reddit_posts.csv`, `cleaned_reddit_posts.csv`

---

### 💬 Task 2: Sentiment & Crisis Risk Classification

- Applied **VADER** sentiment scoring (Positive, Neutral, Negative)
- Embedded post text and high-risk phrases using **BERT** (`sentence-transformers`)
- Calculated semantic similarity to label risk levels:
  - 🟥 High-Risk
  - 🟧 Moderate Concern
  - 🟩 Low Concern
- Output: `reddit_bert_risk_labeled.csv`, distribution plots

---

### 🌍 Task 3: Crisis Geolocation & Mapping

- Extracted city/state names using **spaCy NER (GPE labels)**
- Geocoded locations with `geopy.Nominatim`
- Created interactive **Folium heatmap** of distress discussions
- Displayed **Top 5 crisis-prone locations**
- Output: `crisis_heatmap.html`

---

## 🛠️ Tech Stack

| Component       | Tool / Library                      |
|----------------|--------------------------------------|
| Data Source     | Reddit via `praw`                   |
| NLP             | `nltk`, `spaCy`, `sentence-transformers` |
| Sentiment       | `vaderSentiment`                    |
| Embeddings      | BERT (`all-MiniLM-L6-v2`)           |
| Geocoding       | `geopy`                             |
| Mapping         | `folium`                            |
| Visualization   | `matplotlib`, `seaborn`             |
| Environment     | Google Colab                        |

---

## ▶️ How to Run

1. Open the notebook in **Google Colab**
2. Run code cells step-by-step:
   - Extract posts
   - Clean text
   - Run sentiment & BERT classification
   - Extract and map locations
3. Download outputs:
   - CSV files
   - `crisis_heatmap.html`

---

## 📁 Project Structure

```
/crisiswatch-nlp/
├── raw_reddit_posts.csv
├── cleaned_reddit_posts.csv
├── reddit_bert_risk_labeled.csv
├── crisis_heatmap.html
├── README.md
└── [Colab Notebook].ipynb
```

