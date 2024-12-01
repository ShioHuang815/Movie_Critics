# Movie_Critics

## Overview

This project aims to analyze and predict critic ratings for movies using various features such as runtime, genre, rating, and more. It includes data exploration, feature engineering, and modeling to uncover insights and improve prediction accuracy.

## Table of Contents

1. Data Source
2. Exploratory Data Analysis (EDA)
3. Feature Engineering
4. Modeling
5. Future Directions
6. Files in the Repo

## 1. Data Source

The data is sourced from a PostgreSQL database named everything2024, containing movie details such as:

Title, Genre, Directors
Release Dates (Theater and Streaming)
Runtime, Ratings (Critic and Audience)
Count of Ratings
The dataset was transformed into a CSV file for further processing.

## 2. EDA

Key steps in EDA:

Distribution of movies released over time.
Analysis of critic and audience ratings.
Popularity trends based on audience count.
Insights into rating distributions and their influence on critic ratings.
Highlights:
Audience ratings typically skew higher than critic ratings.
A decline in movie data post-2015 led to filtering movies released before 2010.

## 3. Feature Engineering

Genre: Converted into dummy variables.
Rating: Mapped to numerical categories to capture critic preferences.
Movie Title: Transformed into title length as a numeric feature.
Directors: Top 100 directors encoded as dummy variables.
Kid-Friendliness: Binary feature based on movie rating (e.g., G, PG).

## 4. Modeling

Runtime Only: Baseline model with runtime as the sole feature.
Runtime + Kid-Friendly: Added binary feature for kid-friendliness.
Runtime + Kid-Friendly + Genre: Included genre dummy variables.
Runtime + Kid-Friendly + Genre + Rating Mapped: Added mapped ratings.
Runtime + Genre + Rating + Directors: Switched kid-friendliness with director dummy variables.
Runtime + Genre + Rating + Title Length: Replaced directors with movie title length.

Key features: Runtime, Rating, Genre, and Movie Title Length.

## 5. Future Directions

Further improvements and Insight

## 6. Files in the Repo

1. requirements.txt
This file lists all the Python packages and their respective versions required for the project. It ensures that anyone replicating your work can install the same dependencies for consistent results.

2. .ignore or .gitignore
Specifies files and directories that Git should ignore to avoid unnecessary version control of unwanted files.

3. movies.csv
This file is a local backup of the dataset fetched from the PostgreSQL database. It allows for quicker access to the data without reconnecting to the database for every analysis.

4. movie_critics.ipynb
This file is where most codes are within, along with visualizations and results