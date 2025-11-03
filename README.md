# Audience Segmentation Using K-Means Clustering

## Introduction

### **_Please read the PDF file for full project details._**

This Audience Segmentation Using K-Means Clustering Project is my personal project developed to strengthen my understanding of unsupervised learning and its application in large-scale audience data. The goal is to explore how users naturally group together based on their movie viewing patterns and genre ratings, and to uncover meaningful audience segments without relying on predefined labels.

This is a data-driven project, meaning the analysis is guided by the behavior and characteristics of the data rather than a specific prediction task. Instead of beginning with a fixed hypothesis, the approach allows the data itself to reveal patterns and insights-highlighting differences in engagement levels, genre preferences, and rating tendencies among user clusters.
From these observed behaviors, content and marketing strategies are then defined for each audience segment, aligning platform actions with real viewing patterns and satisfaction trends.

Specifically, I apply the K-Means algorithm, an unsupervised learning technique that partitions users into clusters based on their viewing and rating behavior across genres. To visualize these clusters and interpret user differences more intuitively, I use Principal Component Analysis (PCA) purely for visualization purposes, projecting high-dimensional user data into a two-dimensional space that highlights the main patterns of variation.

---

## Technologies

- Python
  
- Jupyter Notebook
  
- Pandas, NumPy 

- Matplotlib

- Scikit-learn

---

## Dataset

The MovieLens dataset is imported directly from Kaggle using the kagglehub library. [The Movie Dataset]("https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset/")

Two CSV files are loaded for analysis:

- "movies_metadata.csv" contains movie details and genres, 45,466 observations (rows) of 25 variables (columns). Variables of interest include: "genres", "id", and "original_title".

- "ratings.csv" includes user ratings from users, 26,024,289 observations (rows) of 4 variables (columns). These are "userId", "movieId", "rating", and "timestamp".

**After preprocessing, the dataset for audience segmentation contains about 266,000 users who rated 45,000 titles, totaling 11.3 million ratings.**

---

## Finding

| **Cluster**                                         | **Profile Summary**                                                                                                 | **High-Rated Genres (≥3)**                                                               | **Content / Product Strategy**                                                                                                       | **Marketing & Engagement Actions**                                                                                                                                |
| --------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **New Explorers**                        | Avg **9 movies/user**. <br> Light casual users showing moderate interest, especially in emotional and mainstream genres. | *Drama, Thriller, Comedy*                                                                | Personalize based on top genres to reduce choice overload. Curate a “Quick Picks” or “Tonight’s Watch” list with trending titles.    | Targeted push notifications (Drama/Thriller), onboarding playlists (“Start with Top 5 in Comedy”), and watch-streak or first-10 rewards to encourage consistency. |
| **Expanding Enthusiasts**                          | Avg **18 movies/user**. <br> Positive sentiment with moderate frequency; open to multiple genres.                        | *9/20 genres* high-rated (Drama, Romance, Thriller, Action)                              | Encourage cross-genre exploration (“If you liked Drama, try Thriller”). Highlight series/franchises to boost repeat engagement.      | Run personalized discovery campaigns, introduce achievement badges, and create genre-challenge events to sustain interest.                                        |
| **Quiet Viewers (Churn Risk)**               | Avg **5 movies/user** <br> Lowest engagement and low satisfaction (<3 ratings across genres).                           | *None consistently ≥3*                                                                   | Focus on quality-over-quantity: promote only top-rated or editor-curated titles. Simplify recommendations to avoid overwhelm.        | Send re-engagement campaigns (“We think you’ll love these picks”), collect feedback via surveys, and offer watch credits to reactivate usage.                     |
| **Loyalists (Heavy Positive Viewers)** | Avg **69 movies/user** <br> Strong engagement and broad satisfaction across genres.                                     | *14/20 genres* (except for TV Movie, Foreign, Western and Animation - rated below 2.5)         | Implement advanced personalization; recommend new releases, niche titles, and sequels in their preferred genres.                     | Offer early access/previews, social sharing features, and VIP reward programs for loyal users.                                                                    |
| **Premium Loyalists**                            | Avg **135 movies/user** <br> The most active and satisfied viewers; high ratings across nearly all genres.              | *15/20 genres* (all genres were rated above 2.5) | Recommend diverse, long-form, and international content to sustain novelty. Apply hybrid recommendation models (content + behavior). | Create VIP or ambassador programs, beta-tester opportunities, and personalized “Year in Review” summaries to reinforce connection and loyalty.                    |

