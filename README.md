# Crypto Market Sentiment Analysis Pipeline

An end-to-end Python pipeline that analyzes the relationship between
cryptocurrency price movements and financial news sentiment, using
real-time market data and a BERT-based NLP model.

## Overview

This project investigates whether sentiment signals extracted from
financial news headlines correlate with short-term price changes in
major cryptocurrencies (BTC, ETH). The pipeline collects price and
news data via REST APIs, classifies news sentiment using a fine-tuned
financial language model, and analyzes the alignment between sentiment
and market behavior.

## Tech Stack

- **Language**: Python 3
- **NLP Model**: FinBERT (BERT-based, fine-tuned for financial text)
- **Libraries**: pandas, transformers (Hugging Face), requests
- **APIs**: CoinMarketCap (price data), NewsAPI (news headlines)
- **Environment**: Google Colab

## Pipeline Components

1. **Price Data Collection** — Fetches BTC/ETH price time series from
   CoinMarketCap API.
2. **News Data Collection** — Retrieves financial news headlines via
   NewsAPI, filtered by relevance to crypto markets.
3. **Sentiment Classification** — Applies FinBERT to score each
   headline as positive, negative, or neutral.
4. **Correlation Analysis** — Aligns daily aggregated sentiment scores
   with price movements to surface relationships.

## Status

Active project — capstone for *Dealing with Data* (NYU, Spring 2026).
Code and analysis notebooks will be added to this repository.

## Author

**Tianzheng Peng** — NYU MSIS, Class of 2027  
[LinkedIn](https://www.linkedin.com/in/tianzheng-peng) · tp2836@nyu.edu
