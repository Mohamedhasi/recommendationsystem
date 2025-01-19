# E-Commerce Product Recommendation System
Overview
This project implements a collaborative filtering-based recommendation system for an e-commerce platform, which provides personalized product recommendations for users based on their previous interactions. The system leverages advanced techniques like Cosine Similarity and Singular Value Decomposition (SVD) to generate highly accurate recommendations. A RESTful API, built using Flask, allows for real-time interaction with the recommendation engine.

Features
Core Functionalities

User-Based Recommendations: Generates personalized product recommendations for users.

Collaborative Filtering: Uses past user interactions to infer preferences and make predictions.

Matrix Factorization: Employs SVD to uncover latent features in user-product interactions for better recommendations.

API Endpoint: Provides a RESTful endpoint for users to fetch recommendations dynamically.

Additional Insights

Data Exploration: The project includes detailed analysis and visualization of the dataset to understand user behavior.

Sparse Matrix Handling: Efficiently processes sparse datasets with millions of interactions.

Evaluation Metrics: Calculates RMSE to evaluate the accuracy of the recommendations.

Technologies Used

Programming Language
Python 3.8+: The main language for implementing the recommendation logic and API.
Libraries and Frameworks

Flask: For building the RESTful API.

Pandas, NumPy: For data manipulation and preprocessing.

scikit-learn: For similarity calculations and performance evaluation.

SciPy: For implementing SVD.

Matplotlib, Seaborn: For data visualization.

Database
CSV File: The dataset (ratings_Electronics.csv) is stored as a CSV file for simplicity.

Dataset
Source
The dataset used in this project is ratings_Electronics.csv, which contains user ratings for various electronic products. Each record includes:

User ID: Unique identifier for each user.
Product ID: Unique identifier for each product.
Rating: The rating (1–5) given by a user to a product.

Dataset Preprocessing
Removed unnecessary columns (e.g., timestamps).

Filtered users with fewer than 50 ratings to ensure data quality.
Created a sparse interaction matrix for efficient computation.

Project Workflow
Data Loading and Cleaning: The dataset is read and preprocessed for further analysis.

Exploratory Data Analysis (EDA):
Analyzed user and product distributions.
Visualized rating trends using bar plots.

Collaborative Filtering:
Created a user-item interaction matrix.
Calculated similarities between users using Cosine Similarity.

Matrix Factorization:
Applied SVD to decompose the interaction matrix into latent features.
Predicted missing ratings for unobserved interactions.

Recommendation Engine:
Identified top-N products for each user.
Exposed recommendations through a Flask-based API.

Evaluation:
Measured RMSE between actual and predicted ratings to assess accuracy.
