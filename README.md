# CryptoBERT
This repository contains the code and data for the project "Applicability of Financial Sentiment Analysis Tools using BERT Neural Network". The project explores the implementation and feasibility of a sentiment analysis model trained on cryptocurrency-related tweets for analyzing the sentiment of news headlines.

The study investigates the NLP CryptoBERT model, which is based on the BERT (Bidirectional Encoder Representations from Transformers) architecture and BERTweet language model. It has been pre-trained on 850M English tweets and further fine-tuned with 2M cryptocurrency-related posts. The model classifies sentiment as bullish, bearish, or neutral, which are mapped to the positive, negative, and neutral labels of the news headlines. The main objective is to assess the performance of this model, initially fine-tuned on cryptocurrency tweets, in classifying the sentiment of news headlines into positive, negative, or neutral categories.

Methodology: The study involves preprocessing the headlines, transforming sentiment labels to match the model's output, and evaluating the model's performance using accuracy, precision, and recall metrics.

Key Components
Data: The news headlines dataset contains over 10,700 annotated headlines with sentiment labels (positive, negative, neutral). The headlines are preprocessed to match the input requirements of the CryptoBERT model.
1. News_headlines_tagged_uncleaned.csv: Original data containing true labels of news headlines. Source: https://www.kaggle.com/datasets/ankurzing/aspect-based-sentiment-analysis-for-financial-news
2. News_headlines_tagged.csv: Cleaned data with original labels.
3. News_headlines_tagged_cryptobert.csv: Data containing predictions of the model.

The project contains 3 .ipynb notebooks to be run in the following order:
1. CleanData.ipynb– to be run first. Preprocesses the testing data. It outputs "News_headlines_tagged.csv".
2. CryptoBert.ipynb– to be run second. Produces forecasts from CryptoBERT. Input: "News_headlines_tagged.csv file.". It outputs: "News_headlines_tagged_cryptobert.csv"
Source: https://huggingface.co/ElKulako/cryptobert
3. NewsHeadlinesAnalysis.ipynb– to be run third. Analysis of the performance of the model. Input 1: "News_headlines_tagged.csv – cleaned data". Input 2: "News_headlines_tagged_cryptobert.csv"

Conclusion: The results highlight the challenges of domain adaptation, showing that CryptoBERT tends to overestimate neutrality and struggles with correctly classifying positive and negative sentiments in news headlines. The project demonstrates that while CryptoBERT performs well on cryptocurrency tweets, its generalization to news headlines is limited due to contextual and linguistic differences. The findings emphasize the need for domain-specific considerations and further research to enhance the robustness of sentiment analysis models across diverse text genres.
