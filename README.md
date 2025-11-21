# Kindle Review Sentiment Analysis

## Project Overview
This project focuses on performing sentiment analysis on Kindle book reviews, classifying them as either positive or negative. The analysis utilizes the `all_kindle_review.csv` dataset, which includes the review text and associated ratings.

## Methodology
1.  **Data Loading & Exploration:** Initial loading and inspection of the dataset.
2.  **Data Preprocessing:**
    *   **Rating Conversion:** 5-star ratings were binarized (ratings < 3 = negative, >= 3 = positive).
    *   **Text Cleaning:** Lowercasing, removal of special characters, stopwords, URLs, HTML tags, and extra spaces.
    *   **Lemmatization:** Words were reduced to their base forms.
3.  **Train-Test Split:** Data was split into 80% training and 20% testing sets.
4.  **Feature Extraction:** Both Bag-of-Words (BoW) and TF-IDF (Term Frequency-Inverse Document Frequency) were used to convert text into numerical features.
5.  **Machine Learning Model:** Gaussian Naive Bayes was employed for classification.

## Results
*   **Accuracy:**
    *   Bag-of-Words (BOW): 0.5867
    *   TF-IDF: 0.5896
*   **Performance:** Both models showed similar, relatively low accuracy. The models struggled particularly with correctly classifying negative reviews (Class 0), exhibiting low precision for this class.
*   **Model Suitability:** Gaussian Naive Bayes was found to be sub-optimal for the discrete and sparse nature of the text features (BoW, TF-IDF), which violates the model's assumption of normally distributed features.

## Discussion & Future Improvements
*   The current Gaussian Naive Bayes model performance is limited due to its assumption mismatch with text features and the presence of class imbalance in the dataset.
*   **Next Steps:**
    *   Explore alternative machine learning models better suited for text classification (e.g., Multinomial Naive Bayes, Logistic Regression, SVM, BERT).
    *   Investigate more advanced text vectorization techniques (e.g., Word Embeddings).
