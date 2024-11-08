# Natural Language Processing: Stock News Sentiment Analysis and Summarization

## Project Summary
This project focuses on developing an AI-driven sentiment analysis system to evaluate and summarize stock-related news. Designed for a NASDAQ-listed company, the system processes historical daily news data alongside stock prices and trading volume to identify key events and predict potential market impacts. The goal is to enhance investment strategies by providing timely, sentiment-informed insights for financial analysts.

## Key Aspects of the Project
- **Business Context**: In the fast-paced financial industry, news can dramatically influence investor sentiment and stock prices. By leveraging sentiment analysis, this project aims to automate the interpretation of news articles to support more informed investment decisions.
- **Objective**: Create a sentiment analysis model to categorize news sentiment (positive, neutral, or negative) and use an LLM-based summarizer to highlight the top weekly events likely to impact stock prices.
- **Dataset**: Includes 349 news articles from early 2019, each labeled with sentiment (positive, neutral, or negative) and correlated with stock price and trading volume data for more accurate analysis.

## Statistical Analysis
- **Data Quality**: The dataset is clean, with no missing values or duplicates. However, sentiment labels are imbalanced, with a higher frequency of neutral sentiment.
- **Distribution Analysis**: Stock prices show right-skewed distributions, while trading volume and article length (in words) have low correlation with price and sentiment.
- **Bivariate Analysis**: Explored correlations among stock prices, sentiment, trading volume, and article length. Stock price variables are highly inter-correlated, suggesting potential redundancy.

## Data Processing and Model Building
1. **Data Preprocessing**:
   - Tokenization and text cleaning for news content.
   - Feature engineering for additional insights, such as article length.
2. **Model Development**:
   - Built sentiment classification models with embeddings like Word2Vec, GloVe, and Sentence Transformers.
   - Tuned models using Grid Search for optimal performance.

## Model Selection and Final Model
- **Evaluation**: Models were evaluated based on precision, recall, and F1-score.
- **Final Selection**: GloVe-based model showed high training performance but signs of overfitting, highlighting the challenge of sentiment prediction in finance.
- **LLM-Based Summarization**: Designed to return a JSON output summarizing top three weekly positive and negative news events based on likelihood of impacting stock prices.

## Summarization of Stock News using LLM
The LLM generates a weekly summary of key news events by analyzing and ranking headlines based on sentiment and potential impact. This helps identify the top positive and negative developments for analysts to consider in their decision-making.

## Takeaways from the Project
- **Data Challenges**: Financial news data is prone to label imbalance, necessitating careful handling in training models.
- **Model Limitations**: High correlation among stock price variables may require dimensionality reduction or alternative feature engineering.
- **LLM Utility**: Incorporating LLMs for news summarization proved valuable for distilling insights, but accuracy in sentiment categorization remains critical for reliable predictions.
