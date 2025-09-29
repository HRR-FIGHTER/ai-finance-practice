# Practice Project – Stock Price Prediction with LSTM + FinBERT Sentiment

**Author:** Hamid Reza Ranjbar

⚠️ **Disclaimer:** This is a practice/test project for learning purposes only. Not investment advice.

---

## 📌 Overview

This project experiments with predicting S&P 500 stock prices using:

* **Historical Closing Price (CP)**
* **Daily sentiment scores** generated from financial news headlines using **FinBERT (Hugging Face)**

The goal is to test whether sentiment signals improve short-term LSTM predictions compared to using prices alone.

---

## 📂 Repository Structure

```
lstm-sentiment-test/
├── README.md
├── requirements.txt
├── .gitignore
├── LICENSE
├── practice_lstm_sentiment.ipynb   # main notebook (Colab export)
├── sample_data.csv                 # small optional sample
└── data/                           # place Kaggle dataset here (ignored by git)
```

---

## 📊 Dataset

Dataset used: [S&P 500 with Financial News Headlines (2008–2024)](https://www.kaggle.com/datasets/dyutidasmahaptra/s-and-p-500-with-financial-news-headlines-20082024#)

* Download from Kaggle and place the CSV in the `data/` folder.
* A small sample (`sample_data.csv`) is provided for testing.

---

## 🔧 How to Run

1. Clone the repo and install dependencies:

```bash
git clone https://github.com/<your-username>/lstm-sentiment-test.git
cd lstm-sentiment-test
pip install -r requirements.txt
```

2. Download dataset from Kaggle (see link above) → save into `data/`.

3. Open and run the notebook:

```bash
jupyter notebook practice_lstm_sentiment.ipynb
```

(or upload to Google Colab).

---

## 🧠 Sentiment Analysis

This project uses Hugging Face’s [FinBERT](https://huggingface.co/yiyanghkust/finbert-tone) for financial sentiment:

* Headlines → Positive / Negative / Neutral labels
* Converted to numeric score (e.g., +1, –1, 0) and averaged per day

---

## 🚀 Next Steps

* Add direct comparison: price-only LSTM vs. price+sentiment LSTM
* Try transformer-based time series models
* Extend evaluation to multiple stocks

---

## 📜 License

MIT License
