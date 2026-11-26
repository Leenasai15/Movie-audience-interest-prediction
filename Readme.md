# Comparative Analysis of ML Algorithms for Prediction of Audience Interest Based on Movie Review and Rating

B.Tech Capstone Project, SR University
Guide: Dr. Asha S
Team: E. Tharuni, M. Leena Sai, K. Sathwika

## Overview
This project scores real user reviews with VADER sentiment analysis and combines sentiment
with rating, votes and popularity into an Audience Interest Score. Movies are grouped into
Low, Medium and High interest, and three machine learning models are compared. The results
are explored in an interactive Power BI dashboard.

## Pipeline
1. Load and clean the movies and reviews data
2. Clean review text and score every review with VADER (compound score -1 to +1)
3. Average the sentiment for each movie and join it with the movie data (inner join)
4. Apply log transform and Min-Max scaling to rating, votes, popularity and sentiment
5. Calculate the Audience Interest Score:
   (0.30 x Rating) + (0.25 x Votes) + (0.25 x Popularity) + (0.20 x Sentiment)
6. Split the score into Low, Medium and High interest classes (quantile based)
7. Train and compare Logistic Regression, Decision Tree and Random Forest
   (stratified 80/20 split, GridSearchCV, 5-fold cross-validation)
8. Export the results for the Power BI dashboard

## Results
| Model | Accuracy |
|---|---|
| Logistic Regression | 95.6% |
| Random Forest | 94.9% |
| Decision Tree | 89.3% |

Final data: 3,748 movies with 12,952 reviews.

Note: the interest category is built from the same four features, so high accuracy is
expected. Future work is to test on an independent target such as box office.

## Repository contents
- Capstone_.ipynb : Google Colab notebook with the complete pipeline
- movies.csv, reviews.csv, genres.csv, cast.csv, crew.csv : input dataset (TMDB)
- final_master_dataset.csv : final data with sentiment, scores and categories
- review_sentiment_scores.csv : VADER score for every review
- "model_metrics.csv", "classification_report_*.csv", "confusion_matrix_*.csv",
  "feature_importance.csv", "test_predictions.csv" : model results
- *.png : charts (interest distribution, sentiment distribution, model comparison,
  confusion matrices, feature importance)

## Tech stack
Python, pandas, NumPy, Matplotlib, Seaborn, NLTK VADER, scikit-learn, Google Colab, Power BI

## How to run
1. Open Capstone_.ipynb in Google Colab.
2. Upload movies.csv and reviews.csv when asked.
3. Run all cells (Runtime > Run all).

## Data
The input data comes from TMDB (https://www.themoviedb.org): movie metadata and user reviews.

