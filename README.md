# Recommendation System  Matrix Factorization
 Personalized movie recommendations using Matrix Factorization

 
![1_rbSXIekioP0QUpwXBkrhcA](https://github.com/rbhardwaj2186/Recommendation-System--Matrix-Factorization/assets/143745073/60f1c9fc-bf64-4928-b0d8-083300d591e5)

The recommendation model used in this project is based on Matrix Factorization and Collaborative Filtering. Here’s a step-by-step explanation:

## Data Preparation: The model first imports the necessary libraries and datasets. It merges the movies and ratings datasets based on the ‘movieId’ column.

## Data Cleaning: It drops unnecessary columns and handles missing values.

## Data Transformation: The model creates a pivot table where each row represents a user and each column represents a movie. The entries of this matrix are the ratings that a user gives to a movie.

## Matrix Factorization: The model applies Singular Value Decomposition (SVD) to the pivot table. SVD is a dimensionality reduction technique that factorizes the user-movie matrix into the product of two lower dimensionality orthogonal matrices and a diagonal matrix. This process captures the latent relationships between users and movies.

## Similarity Computation: The model computes the correlation coefficient for every pair of movies based on their latent features obtained from SVD. This results in a similarity matrix where each entry represents the similarity between two movies.

## Recommendation: Given a movie, the model finds other movies with a high correlation coefficient in the similarity matrix. These are the movies that are most similar to the given movie and are hence recommended to the user.

### This approach is a form of Collaborative Filtering as it uses the behavior of users (their ratings) to make recommendations. It’s also a form of Content-Based Filtering as it uses information about the items (movies) to make recommendations. The combination of these techniques allows the model to make accurate and personalized recommendations.
