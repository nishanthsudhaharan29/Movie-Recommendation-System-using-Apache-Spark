# Pumpkinmeter: A Movie Recommendation System

## Project Description

Pumpkinmeter is a collaborative filtering-based movie recommendation system developed as part of a Big Data Analysis course. Built using Apache Spark and Python, the project demonstrates how large-scale user-item interactions can be harnessed to deliver personalized movie suggestions. 

The system analyzes the [MovieLens dataset](https://grouplens.org/datasets/movielens/) — containing over 27 million user ratings — and applies the Alternating Least Squares (ALS) algorithm from Spark’s MLlib to uncover latent user preferences. 

Through user testing scenarios, Pumpkinmeter recommends movies based on both niche interests and mainstream popularity, depending on filtering thresholds. This solution supports Ripe Pumpkins, a startup aiming to enhance user engagement and retention with intelligent movie suggestions powered by data-driven insights.

**Key Features:**
- ⚙Scalable model training with Apache Spark
- Personalized recommendations for new users
- Scenario-based testing (25 vs. 100+ ratings filtering)
- Python 3-compatible, with improved data handling and ALS tuning

This project illustrates the practical application of machine learning in building real-world recommender systems.
