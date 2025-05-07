# Twitter Sentiment Analysis on "Supernatural"

# Overview
This project aims to analyze public sentiment toward the TV series Supernatural using Twitter data. By leveraging the Sentiment140 dataset and implementing multiple machine learning algorithms, the project explores sentiment classification through the lens of real-world, large-scale social media data. The process involves comprehensive data preprocessing, exploratory analysis, and model evaluation, following the Knowledge Discovery in Databases (KDD) methodology.

# Data Source and Characteristics
The dataset used is the Sentiment140 dataset, obtained from Kaggle. It consists of 1.6 million tweets labeled as positive (4), neutral (2), or negative (0) sentiments. The dataset includes the following features:

Target (Sentiment label: 0, 2, or 4)
ID (Unique tweet identifier)
Date (Tweet timestamp)
Query (Search term used)
User (Username of tweet author)
Text (The tweet content)

The tweets were filtered to focus specifically on those related to the Supernatural series, ensuring relevance to the study.

# KDD Process

# 1. Data Processing
Selection: Filtered relevant tweets about Supernatural from Sentiment140.

Cleaning: Removed URLs, mentions, hashtags, special characters, and normalized text. Emoticons were handled appropriately to preserve sentiment cues.

Transformation: Tokenization, lowercasing, and stemming were applied to standardize the text. TF-IDF and word embeddings (Word2Vec/GloVe) were used to vectorize data.

Reduction: Dimensionality was reduced using TF-IDF and embeddings to improve performance and computation efficiency.

# 2. Data Mining Methods
Multiple models were trained and evaluated:

Logistic Regression
Linear Support Vector Classifier (LinearSVC)
XGBoost Classifier
Multinomial Naive Bayes
Voting Classifier (ensemble approach)

These models were selected for their strength in text classification tasks and scalability to large datasets.

# Evaluation and Results

# Evaluation Metrics
Each model was assessed using the following metrics:

Accuracy
Precision
Recall
F1-score
Support

These metrics helped assess the balance between correctly identifying sentiments and avoiding misclassifications.

# Key Results

# Model==Accuracy==Comments
Logistic Regression==0.82==Strong balance of precision and recall across sentiment classes
LinearSVC==0.82==Robust performance, similar to Logistic Regression
XGBoost==0.77==High precision, but lower recall on negative sentiment
MultinomialNB==0.80==Effective on negative sentiment, slightly weaker on positive class
Voting Classifier==0.82==Best overall balance by combining strengths of individual models

The Voting Classifier, Logistic Regression, and LinearSVC emerged as top performers, showing consistent and reliable sentiment classification on tweets about Supernatural.

# Conclusion
This project demonstrates how sentiment analysis can provide meaningful insights into public opinion by mining and interpreting large-scale Twitter data. The combination of comprehensive preprocessing, diverse modeling strategies, and robust evaluation ensures reliable results. These models serve as scalable tools for analyzing sentiment in social media platforms, adaptable to a variety of real-world applications beyond the Supernatural fandom.
