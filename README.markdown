# Recommendations with IBM

## Project Overview
This project is part of the Data Scientist Nanodegree by Udacity. It follows a structured approach to building and evaluating recommendation systems, using data on user-article interactions to explore, rank, and personalize recommendations through various techniques.

![IBM Watson](/ibm-watson.png)

## Project Structure
The project is divided into the following tasks:

### I. Exploratory Data Analysis
- Investigate the dataset to understand the distribution of users, articles, and interactions.
- Visualize and summarize basic statistics, such as the most viewed articles and unique user engagement.

### II. Rank-Based Recommendations
- Build simple popularity-based recommendations by identifying the most read articles.
- Suitable for cold-start scenarios (e.g., new users) where personalized data is unavailable.

### III. User-User Based Collaborative Filtering
- Construct a user-item interaction matrix.
- Use dot products between user vectors to find similar users.
- Recommend articles that similar users have engaged with but the target user has not.
- Utilizes the following preprocessed `.p` files:
  - `user_item_matrix.p`: Full interaction matrix.
  - `user_item_train.p`: Training split of interactions.
  - `user_item_test.p`: Test split for evaluation.

### IV. Matrix Factorization (via SVD)
- Use Singular Value Decomposition (SVD) to identify latent features of users and articles.
- Predict user preferences for unseen articles based on learned latent structures.
- Evaluate performance against the test set.
- Analyze limitations due to implicit feedback (no ratings) and data sparsity.

## Technologies Used
- Python
- Pandas, NumPy
- Pickle (for saving and loading preprocessed interaction matrices)
- Scikit-learn (for SVD implementation)
- Jupyter Notebook (for prototyping and experimentation)

## Data Files
The following `.p` (pickle) files are loaded to streamline data access and reduce recomputation:
- `user_item_matrix.p`: Full user-item interaction DataFrame.
- `user_item_train.p`: Subset of interactions for training.
- `user_item_test.p`: Subset of interactions for testing recommendations.