# 📰 Reddit Crypto News Sentiment Analyzer

Analyze the latest crypto-related Reddit posts and their top comments using sentiment analysis (VADER) and visualize the results using Matplotlib and Seaborn.

---

## 📌 Project Overview

This project uses the **Reddit API (via `praw`)** to fetch recent posts from popular crypto subreddits like:

- r/CryptoCurrency  
- r/Bitcoin  
- r/Ethereum  
- r/Solana

It applies **VADER sentiment analysis** to both the post content and the top comments, and then visualizes sentiment trends using graphs like:

- Bar charts of sentiment categories
- Scatter plots: score vs sentiment
- Heatmaps: correlation of post metrics

---

## 🚀 Features

- 🔍 Pulls live posts & comments from Reddit using `praw`
- 🧠 Sentiment classification using NLTK's VADER
- 📊 Visualizations using Matplotlib & Seaborn
- 📁 Exports full dataset to CSV
- 📈 Custom visualizations like heatmaps and scatter plots

---

## 🖼️ Sample Visuals

### 🔴 Post Sentiment Classification
![Bar chart of sentiment classes](./assets/sentiment_bar.png)

### 🔵 Score vs Sentiment Scatter Plot
![Score vs Sentiment](./assets/scatter_plot.png)

### 🔥 Correlation Heatmap
![Correlation Heatmap](./assets/heatmap.png)

---

## 🧪 Tech Stack

| Tool           | Usage                            |
|----------------|----------------------------------|
| `praw`         | Reddit API wrapper                |
| `pandas`       | DataFrame operations              |
| `nltk`         | VADER sentiment analysis          |
| `matplotlib`   | Static plotting                   |
| `seaborn`      | Advanced plotting & heatmaps      |
| `streamlit` *(optional)* | Web-based dashboard    |

---

## 📁 Output Columns

The resulting CSV (`crypto_reddit_sentiment.csv`) contains:

| Column              | Description                                  |
|---------------------|----------------------------------------------|
| subreddit           | Name of subreddit                            |
| title               | Post title                                   |
| text                | Post body content                            |
| score               | Post upvotes                                 |
| url                 | Direct link to the post                      |
| num_comments        | Number of comments                           |
| created             | UTC timestamp                                |
| top_comments        | Top 10 comment bodies                        |
| post_sentiment      | VADER compound score of post                 |
| comment_sentiment   | VADER compound score of comments             |
| post_sentiment_label| Negative / Neutral / Positive classification |
| comment_sentiment_label| Same as above                             |
| comment_length      | Word count of top comments                   |

---

## 📦 Installation

```bash
# Create a virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install praw pandas matplotlib seaborn nltk
