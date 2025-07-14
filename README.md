# Movie Recommendation System

## Introduction

Ripe Pumpkins is a startup that aims to offer a movie review aggregation service. Inspired by the success of personalized recommendation engines in streaming platforms, the company seeks to implement its own recommendation engine called Pumpkinmeter. This project explores the feasibility of building a collaborative filtering recommender system using Apache Spark's MLlib library, based on the MovieLens dataset. The goal is to evaluate Pumpkinmeter’s potential to enhance user engagement and retention.

## Dataset Used

The project utilizes the MovieLens dataset provided by GroupLens Research. The dataset includes:

- 27 million movie ratings
- 1.1 million tag applications
- 58,000 movies
- 280,000 users
- 14 million tag genome relevance scores across 1,100 tags

The dataset was last updated in September 2018.

## Technical Details

This project uses Apache Spark's MLlib to implement a collaborative filtering model based on the Alternating Least Squares (ALS) algorithm. Collaborative filtering is a widely used method in recommendation systems that leverages user-item interaction data.

Key ALS parameters:

- `numBlocks`: Number of partitions for parallel computation
- `rank`: Number of latent features
- `iterations`: Number of training iterations
- `lambda`: Regularization parameter to avoid overfitting
- `implicitPrefs`: Boolean to support implicit feedback
- `alpha`: Confidence level for implicit feedback data

## Challenges and Debugging

### Python Compatibility

The original codebase used in the tutorial was written in Python 2. As the project was developed using Python 3, compatibility issues and syntax errors were encountered. These were resolved by updating print statements, handling type conversions (e.g., `unicode`, `long`), and adjusting deprecated functions.

### Data Handling

Loading and parsing the large MovieLens dataset efficiently in Spark was another challenge. Preprocessing steps were applied to ensure data was properly formatted, validated, and persisted for reuse in training and testing.

### Model Tuning

Parameter tuning for ALS, particularly `rank` and `lambda`, required several iterations to achieve optimal performance and reduce overfitting. Hyperparameter tuning was performed manually based on evaluation metrics and qualitative testing.

## Results

The model was evaluated through four test cases. Two new users (myself and a colleague) each rated 10 movies, and the system generated top 15 movie recommendations for both users.

Evaluation scenarios:

- **Scenario 1:** Filtered out movies with fewer than 25 ratings
- **Scenario 2:** Filtered out movies with fewer than 100 ratings

In both cases, the recommendation system provided relevant and diverse movie suggestions based on user preferences.

## Tools and Technologies

- Python 3
- Apache Spark
- Spark MLlib (ALS)
- Jupyter Notebook
- MovieLens dataset from GroupLens

## Conclusion

This project successfully built and tested a collaborative filtering-based recommendation system using Spark MLlib. The resulting engine, Pumpkinmeter, demonstrated the ability to generate relevant recommendations using minimal user input. It provides a scalable foundation for Ripe Pumpkins to enhance user satisfaction and drive engagement through personalized movie suggestions.

