
# Real-Time News Categorization & Sentiment Analysis Dashboard

A Streamlit-powered interactive dashboard for real-time news aggregation, automated categorization, and sentiment analysis using fine-tuned BERT transformer models. The application fetches global news, classifies articles into predefined categories, analyzes sentiment (Positive, Neutral, Negative), and provides insightful visualizations and filtering options.

---

## 🚀 Features

- **Live News Aggregation**  
  Fetches real-time headlines from multiple countries using NewsAPI.

- **Automated News Categorization**  
  Classifies articles into relevant categories using a fine-tuned BERT model.

- **Sentiment Analysis**  
  Evaluates sentiment (Positive, Neutral, Negative) using a separate BERT model.

- **Interactive Dashboard (Streamlit)**  
  - Filter by country, category, sentiment, and date  
  - View KPIs: total articles, sentiment counts, category distribution  
  - Dynamic visualizations: pie charts, bar graphs, time series  
  - Browse article details with metadata and source links  

---

## 🗂️ Project Structure

```plaintext
app.py                    # Main dashboard script
news_fetcher.py           # News retrieval and preprocessing
categorizer.py            # News category classification using BERT
sentiment_analyzer.py     # Sentiment classification using BERT
train_models.py           # Script for training BERT models
bert_news_cat/            # Saved category model and encoder
bert_sentiment/           # Saved sentiment model and encoder
news_data.json            # Raw news data
categorized_news.json     # Labeled news data
```

---

## 🧰 Getting Started

### Prerequisites

Ensure the following dependencies are installed:

- Python 3.8+
- [`streamlit`](https://streamlit.io/)
- [`transformers`](https://huggingface.co/transformers/)
- [`torch`](https://pytorch.org/)
- [`pandas`](https://pandas.pydata.org/)
- [`plotly`](https://plotly.com/python/)
- [`scikit-learn`](https://scikit-learn.org/)
- [`newsapi-python`](https://github.com/mattlisiv/newsapi-python)
- [`joblib`](https://joblib.readthedocs.io/)

### Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/moazhassan751/news-bert-categorization-sentiment-dashboard
   cd news-bert-categorization-sentiment-dashboard
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Configure NewsAPI Key:**

   Open `news_fetcher.py` and insert your [NewsAPI](https://newsapi.org/) key in the designated variable.

4. **(Optional) Retrain Models:**

   To retrain or fine-tune the BERT models on your own data:

   ```bash
   python train_models.py
   ```

---

## ▶️ Running the Application

To launch the Streamlit dashboard locally:

```bash
streamlit run app.py
```

The app will open in your default web browser.

---

## 📁 File Descriptions

| File/Folder            | Description                                        |
|------------------------|----------------------------------------------------|
| `app.py`               | Main Streamlit app file                            |
| `news_fetcher.py`      | Fetches and stores news articles                   |
| `categorizer.py`       | Categorizes articles using BERT                    |
| `sentiment_analyzer.py`| Performs sentiment analysis using BERT             |
| `train_models.py`      | For training or updating models                    |
| `bert_news_cat/`       | Fine-tuned category classification model + encoder |
| `bert_sentiment/`      | Fine-tuned sentiment model + encoder               |
| `news_data.json`       | Raw articles fetched from NewsAPI                  |
| `categorized_news.json`| Articles with category and sentiment labels        |

---

## 🔧 Customization Options

- **Add/Remove Countries:**  
  Modify the list in `news_fetcher.py` or `app.py`.

- **Change or Add Categories:**  
  Update the label mappings in `categorizer.py` and retrain if needed.

- **Improve Sentiment Accuracy:**  
  Fine-tune the sentiment BERT model on a larger or domain-specific dataset.

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!  
Feel free to fork this repo and submit a pull request.

---

## 🙌 Acknowledgements

- [NewsAPI](https://newsapi.org/) — Real-time news data
- [Hugging Face Transformers](https://huggingface.co/transformers/) — BERT models
- [Streamlit](https://streamlit.io/) — Dashboard framework
- [Plotly](https://plotly.com/python/) — Data visualization




