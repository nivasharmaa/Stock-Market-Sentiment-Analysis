# Stock-Market-Sentiment-Analysis

**Team Members:** Mansi Asher, Niva Sharma

## Project Overview

Stock prices are influenced by many factors, including news sentiment.  
Our goal is to investigate whether financial news sentiment correlates with — and can help predict — daily stock price movements for a chosen company over the past 1–2 years. This is framed as a supervised learning problem, using historical prices and sentiment scores to forecast market direction.

---

## Novelty & Importance

- **Why this matters:**  
  - News sentiment is a key driver of investor behavior.  
  - If a reliable link exists, it enables sentiment-driven trading strategies.  
- **Key research questions:**  
  1. How accurately can news sentiment predict daily stock changes?  
  2. What is the impact of positive vs. negative headlines?  
  3. Do some stocks react more strongly to news sentiment?  
- **Prior work:**  
  - Existing studies show mixed results depending on data sources, timeframes, and methods.  
  - Our contribution: apply the analysis to recent real-world data and a modern NLP pipeline.

---

## Data Collection

1. **Financial News:**  
   - Kaggle dataset of headlines tagged with sentiment (positive / neutral / negative).  
2. **Stock Prices:**  
   - Yahoo Finance API to fetch historical OHLCV data (open, high, low, close, volume).  

---

## Data Format & Preparation

- **News Data:**  
  - Text headlines + sentiment labels.  
  - Convert labels to numerical: +1 (positive), 0 (neutral), –1 (negative).  
- **Stock Data:**  
  - Daily time series with closing price and percentage change.  
- **Merging Strategy:**  
  - Aggregate daily sentiment scores (e.g. sum or average).  
  - Align with same-day price changes.

---

## Modeling Approach

- **Regression:**  
  - Linear Regression to predict % change in closing price.  
- **Classification:**  
  - Decision Tree (or other) to predict “Increase” vs. “Decrease.”  

_Models chosen for interpretability and efficiency on structured data._

---

## Implementation Steps

1. **Data Preprocessing**  
   - Clean news text (remove stopwords, punctuation).  
   - Encode sentiment labels.  
2. **Feature Engineering**  
   - Aggregate sentiment per day.  
   - Merge with price change features.  
3. **Train/Test Split**  
   - 80% training, 20% testing.  
4. **Model Training**  
   - Fit both regression and classification models.  
5. **Performance Evaluation**  
   - Compute RMSE for regression; accuracy for classification.  
6. **Visualization**  
   - Plot sentiment vs. price change.  
   - Compare predicted vs. actual movements.

---

## Evaluation Metrics

- **Regression:** Root Mean Squared Error (RMSE)  
- **Classification:** Accuracy, Confusion Matrix

---

## Visualization

- Time-series plots of aggregated sentiment and stock price.  
- Scatter plots showing sentiment score vs. price movement.  
- Bar charts of model performance comparisons.

---

## Challenges & Limitations

- **Multifactor Market:** Prices are influenced by more than just news (earnings, macro events).  
- **Sentiment Noise:** NLP tools may misinterpret financial jargon.  
- **Reaction Time:** Market may react before or after publication, introducing lag.

---

## Conclusion

This project explores the intersection of NLP and finance by testing whether news sentiment can serve as a practical indicator for short-term stock price movements. Findings will inform the feasibility of sentiment-driven trading signals and highlight areas for future improvement.

