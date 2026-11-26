# Comparative Analysis of ML Algorithms for Prediction of Audience Interest Based on Movie Review and Rating

B.Tech Capstone Project, SR University
Guide: Dr. Asha S
Team: [E.Tharuni], [M.Leena Sai], [K.Sathwika]

## Overview
We score real user reviews with VADER sentiment analysis and combine sentiment with rating,
votes and popularity into an Audience Interest Score. Movies are grouped into Low, Medium
and High interest, and three ML models are compared.

## Results
| Model | Accuracy |
|---|---|
| Logistic Regression | 95.6% |
| Random Forest | 94.9% |
| Decision Tree | 89.3% |

Data: 3,748 movies with 12,952 reviews.
Note: the interest category is built from the same four features, so high accuracy is expected.

## Tech stack
Python, pandas, NLTK VADER, scikit-learn, Google Colab, Power BI

## How to run
1. Open notebook/Movie_Audience_Interest.ipynb in Google Colab.
2. Upload the movies and reviews CSV files when asked.
3. Run all cells.

## Data
TMDB movie metadata and user reviews: [dataset link]
