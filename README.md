Spam Detection Using NLP & Machine Learning 
Overview
This project builds a spam detection model using natural language processing (NLP) and multiple machine learning algorithms. The goal is to classify SMS messages as ham (not spam) or spam with high accuracy and precision.
Dataset
Dataset: spam.csv (contains SMS messages labeled as ham or spam)
Initial shape: 5572 rows, 5 columns
After cleaning (removing duplicates and unnecessary columns): 5169 rows, 2 columns
Steps in the Project
1. Data Cleaning
Removed unnecessary columns (Unnamed: 2, 3, 4)
Renamed columns to target and text
Encoded labels: ham = 0, spam = 1
Removed duplicates

2. Exploratory Data Analysis (EDA)
Visualized class imbalance (ham >> spam)
Checked message length, word count, sentence count
Created WordClouds for spam and ham messages
Generated frequency plots of most common words

3. Text Preprocessing
Lowercased all text
Tokenization using NLTK
Removed stopwords and punctuation
Applied stemming (PorterStemmer)

4. Feature Extraction
Used TF-IDF Vectorization (max_features=3000)
Prepared feature matrix X and target vector y

5. Model Building & Evaluation
Tested multiple classifiers:
SVC, KNN, Naive Bayes, Decision Tree, Logistic Regression, Random Forest, AdaBoost, Bagging, Extra Trees, Gradient Boosting, XGBoost
Best performing models:
Voting Classifier (SVC + MNB + ExtraTrees)

Accuracy: ~98.16%
Precision: ~99.17%
Stacking Classifier
Accuracy: ~97.87%
Precision: ~93.28%

6. Model Saving
Vectorizer saved: vectorizer.pkl
Model saved: model.pkl

Conclusion

The model is highly accurate and precise for SMS spam detection. Using a combination of preprocessing, TF-IDF, and ensemble methods (voting/stacking), this project demonstrates an end-to-end ML workflow.
