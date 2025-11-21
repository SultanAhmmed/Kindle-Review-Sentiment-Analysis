# Kindle Review Sentiment Analysis

This project performs sentiment analysis on Kindle reviews, classifying them as either positive or negative. The process involves several key steps:

## 1. Data Loading and Initial Exploration

- The dataset `all_kindle_review.csv` is loaded using pandas.
- The 'reviewText' and 'rating' columns are selected for analysis.

## 2. Data Preprocessing and Cleaning

- **Rating Binarization**: Ratings of 1 and 2 are converted to 0 (negative), and ratings of 3, 4, and 5 are converted to 1 (positive).
- **Text Normalization**: Review text is converted to lowercase.
- **Noise Removal**: Special characters, stopwords, URLs, HTML tags, and additional spaces are removed from the review text.
- **Lemmatization**: Words are reduced to their base or root form.

## 3. Train-Test Split

- The preprocessed data is split into training and testing sets to prepare for model development and evaluation.

## 4. Feature Extraction

Two common text vectorization methods are used to convert text data into numerical features:

- **Bag-of-Words (BoW)**: Implemented using `CountVectorizer`.
- **TF-IDF (Term Frequency-Inverse Document Frequency)**: Implemented using `TfidfVectorizer`.

## 5. Model Training and Evaluation

- A **Gaussian Naive Bayes** classifier is trained using both the BoW and TF-IDF features.
- The models are evaluated using standard classification metrics: **accuracy score**, **confusion matrix**, and **classification report** to assess their performance.
