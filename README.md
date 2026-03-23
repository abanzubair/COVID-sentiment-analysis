# 🦠 COVID-19 Tweet Sentiment Analyzer

A machine learning project that classifies COVID-19 related tweets into **Positive**, **Negative**, or **Neutral** sentiments using NLP and Logistic Regression.

## 📊 Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | **91%** |
| Macro F1-Score | 0.90 |

| Class | Precision | Recall | F1 |
|-------|-----------|--------|----|
| Negative | 0.95 | 0.81 | 0.88 |
| Neutral | 0.87 | 0.99 | 0.93 |
| Positive | 0.95 | 0.87 | 0.91 |

## 🛠️ Tech Stack

- **Python 3.13**
- **pandas**, **numpy** — data handling
- **scikit-learn** — TF-IDF vectorization, Logistic Regression
- **VADER (NLTK)** — initial sentiment scoring
- **WordCloud**, **matplotlib** — visualization
- **Gradio** — interactive web UI

## 📁 Project Structure

```
├── covid.ipynb        # Main notebook
├── nlptask.csv        # Dataset (COVID tweets)
└── README.md
```

## 🚀 Getting Started

### 1. Clone the repo
```bash
git clone https://github.com/yourusername/covid-sentiment-analyzer.git
cd covid-sentiment-analyzer
```

### 2. Install dependencies
```bash
pip install pandas numpy scikit-learn matplotlib wordcloud gradio nltk
```

### 3. Run the notebook
```bash
jupyter notebook covid.ipynb
```

### 4. Launch the UI
Run the last cell in the notebook — opens a Gradio interface at `http://127.0.0.1:7860`

## 🔍 How It Works

1. **Data Cleaning** — removes RTs, URLs, special characters, lowercases text
2. **Feature Extraction** — TF-IDF vectorizer converts cleaned tweets to numerical features
3. **Model** — Logistic Regression trained on 80/20 train-test split
4. **Prediction** — classifies any input tweet as `pos`, `neg`, or `neu`

## 📷 Example Predictions

| Tweet | Prediction |
|-------|-----------|
| *"Vaccines are saving lives, finally seeing hope!"* | 😊 Positive |
| *"Another lockdown is destroying the economy"* | 😠 Negative |
| *"WHO releases new COVID-19 guidelines"* | 😐 Neutral |

## 📄 Dataset

The dataset (`nlptask.csv`) contains COVID-19 tweets from April 2021 with pre-labeled sentiments using VADER scores.

---

Made with ❤️ | Aban Zubair
