# Cryptocurrency Market Trends and News Sentiment Analysis

An end-to-end Python pipeline that investigates the relationship between
cryptocurrency market performance and financial news sentiment, using
real-time market data and a BERT-based NLP model.

## Overview

This project examines whether sentiment extracted from news headlines
correlates with short-term cryptocurrency price movements. It collects
market data and news articles via REST APIs, classifies headline
sentiment using FinBERT (a financial-domain BERT model), and analyzes
the alignment between sentiment and price across the top 10 coins by
market cap.

## Tech Stack

- **Language**: Python 3
- **NLP Model**: FinBERT (`ProsusAI/finbert`) via Hugging Face transformers
- **Libraries**: pandas, NumPy, requests, matplotlib, transformers
- **APIs**: CoinGecko (market data), The Guardian (news articles)
- **Environment**: Google Colab

## Pipeline

1. **Market Data Collection** — Top 20 coins by market cap from CoinGecko,
   including 24h/7d price change, market cap, and trading volume.
2. **News Collection** — ~100 recent news headlines from The Guardian
   API across 10 major coins.
3. **Sentiment Classification** — FinBERT runs locally on each headline,
   producing positive/neutral/negative labels with confidence scores.
4. **Data Cleaning** — Missing-value handling, outlier detection
   (|24h change| > 20%), and standardized formatting.
5. **Analysis** — Five questions covering price movement, sentiment
   distribution, sentiment-price correlation, media coverage vs.
   trading volume, and market cap tier comparisons.
6. **Visualization** — Bar charts, scatter plots with trend lines,
   and dual-axis comparisons.

## Key Findings

- Bitcoin and Ethereum dominate both news coverage and trading volume.
- Sentiment and 24-hour price change show limited correlation in the
  current snapshot, consistent with efficient market hypothesis over
  short horizons.
- All top 10 coins fall in the Large Cap tier (>$10B), reflecting
  concentration of value at the top of the market.

## Files

- `crypto_sentiment_analysis.ipynb` — Full pipeline and analysis

## Status

Spring 2026 — *Dealing with Data*, NYU MSIS.

## Author

**Tianzheng Peng** — NYU MSIS, Class of 2027
[LinkedIn](https://www.linkedin.com/in/tianzheng-peng) · tp2836@nyu.edu
