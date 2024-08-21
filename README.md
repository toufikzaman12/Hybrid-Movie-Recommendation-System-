
# Comparative Analysis of Hybrid Movie Recommendation Systems

This repository contains the source code, datasets, and documentation for the project titled "Comparative Analysis of Hybrid Movie Recommendation Systems." The project was developed as part of a summer internship at NIT Sikkim by students from Jalpaiguri Government Engineering College.

## Introduction

Recommender systems are crucial in many domains, especially in online platforms like Netflix, Amazon, and YouTube, where personalized content delivery is essential. This project focuses on developing and comparing three hybrid movie recommendation systems that integrate both content-based and collaborative filtering techniques. The goal is to analyze the effectiveness of these systems in providing accurate and relevant movie recommendations.

## Team Members

- **Basudeb Roy**
- **SK Rajesh** 
- **Md Toufikzaman**

## Mentorship

- **Dr. Bam Bahadur Sinha**  
  Assistant Professor, Computer Science and Engineering Department, NIT Sikkim
- **Dr. Pratyay Kuila**  
  Assistant Professor, Computer Science and Engineering Department, NIT Sikkim

## Internship Duration

- **8 weeks** (19 June - 15 August 2024)

## Objectives

The primary objectives of the project are:

1. **Develop Hybrid Recommender Systems**: Create three distinct hybrid recommendation systems combining content-based and collaborative filtering techniques.
2. **Comparative Analysis**: Evaluate and compare the systems based on performance metrics like MAE, RMSE, precision, recall, and F1-score.
3. **Address Challenges**: Overcome common issues in recommendation systems such as data sparsity and computational complexity.
4. **Suggest Improvements**: Identify potential improvements and future research directions for hybrid recommendation systems.

## Datasets

The project makes use of publicly available movie datasets:

- **`links.csv`**: Maps `movieId` to external identifiers like `imdbId` and `tmdbId`.
- **`movies.csv`**: Contains movie information including `movieId`, `title`, and `genres`.
- **`ratings.csv`**: Provides user ratings with fields for `userId`, `movieId`, `rating`, and `timestamp`.
- **`tags.csv`**: Contains user-generated tags with fields for `userId`, `movieId`, `tag`, and `timestamp`.

## Methodology

### System Architectures

#### 1. Md Toufikzaman's Hybrid System

- **Content-Based Filtering**: Implemented using TF-IDF to calculate the similarity between movies based on genres and tags.
- **Collaborative Filtering**: Utilizes cosine similarity on a user-item matrix to recommend movies based on user preferences.
- **Hybrid Approach**: Combines the scores from both content-based and collaborative filtering using a weighted sum to generate final recommendations.

#### 2. SK Rajesh's Hybrid System

- **Collaborative Filtering (SVD)**: Applies Singular Value Decomposition for matrix factorization, predicting user ratings by learning latent factors.
- **Content-Based Filtering (Genre Overlap)**: Measures similarity by comparing overlapping genres between movies.
- **Hybrid Approach**: Integrates the results from SVD-based collaborative filtering and genre overlap-based content filtering.

#### 3. Basudeb Roy's Hybrid System

- **Collaborative Filtering (Item-Based Cosine Similarity)**: Uses item-item similarity with cosine similarity to identify related movies based on user ratings.
- **Content-Based Filtering (TF-IDF)**: Employs TF-IDF to find similar movies based on genre descriptions.
- **Hybrid Approach**: Merges item-based collaborative filtering with TF-IDF content-based filtering to provide recommendations.

### Implementation Details

- **Data Preprocessing**: Involves cleaning the dataset, handling missing values, and normalizing the data for better model performance.
- **Model Training**: Each model is trained using a subset of the data, with hyperparameters tuned to optimize performance.
- **Integration**: The hybrid systems are implemented by combining the predictions from both content-based and collaborative models.

### Evaluation Metrics

The systems are evaluated using the following metrics:

- **Mean Absolute Error (MAE)**: Measures the average absolute difference between predicted and actual ratings.
- **Root Mean Squared Error (RMSE)**: Calculates the square root of the average squared differences between predicted and actual ratings.
- **Precision**: The proportion of relevant items recommended out of all recommended items.
- **Recall**: The proportion of relevant items recommended out of all relevant items available.
- **F1-Score**: The harmonic mean of precision and recall, providing a balance between the two.

### Challenges Encountered

- **Data Sparsity**: The issue of having too many missing ratings in the user-item matrix, which was mitigated by combining different filtering approaches.
- **Computational Complexity**: High computational costs, especially with SVD and item-based filtering on large datasets, were addressed by optimizing the algorithms and using efficient data structures.

## Results and Discussion

The comparative analysis yielded the following insights:

- **Accuracy**: SK Rajesh's SVD-based system achieved the lowest MAE and RMSE, indicating high accuracy in predicting ratings.
- **Relevance**: Basudeb Roy's system demonstrated the best precision and recall, making it the most effective at recommending relevant items.
- **Balance**: Md Toufikzaman's system provided a balanced performance across all metrics, making it versatile for different use cases.

## Future Work

Potential future directions include:

- **Deep Learning Approaches**: Investigating the use of neural networks and deep learning techniques for hybrid recommendation systems.
- **Real-Time Recommendations**: Developing systems capable of providing recommendations in real-time based on user interactions.
- **User Feedback Integration**: Incorporating mechanisms to learn from user feedback and improve recommendations dynamically.

## Conclusion

This project successfully developed and evaluated three hybrid movie recommendation systems, each with unique strengths and weaknesses. The findings highlight the trade-offs between accuracy, relevance, and computational efficiency in hybrid recommender systems. These insights can inform future research and development in this area.

## Acknowledgements

We would like to express our gratitude to our mentors, Dr. Bam Bahadur Sinha and Dr. Pratyay Kuila, for their invaluable guidance and support. We also thank NIT Sikkim for providing the resources necessary to carry out this project. Special thanks to our families, friends, and peers for their encouragement throughout this journey.

## Appendix

- **Appendix A**: Detailed Code Implementation and Explanations
- **Appendix B**: Additional Experiments and Performance Metrics
- **Appendix C**: User Study and Feedback

