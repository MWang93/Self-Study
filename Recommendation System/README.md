Learning, RS Implementation will be published on Work GitHub (private repo).

# Types 
- Content-based recommendation (based on item attributes)
- Collaborative filtering (based on similar iteractions)
  - User-based: Both User1 and User2 like Item1 and Item2, So User1 and User2 are considered as similar users. User1 also liked Item3, so we guess User2 also likes Item3 (similar to User1).
  - Item-based: 
    - 1. Find similar items by using a similarity metric.
      2. For a user, recommend the items most similar to the items (s)he already likes.
    - Both Item1 and Item2 are liked by User1 and User2, So Item1 and Item2 are considered are similar item. User3 likes Item1, so we guess User3 also like Item2 (similar to Item1).
- Hybrid
- Popularity Trends

# Algorism
- Memory Based
  - Correlation Similarity (KNN)
    1. Jaccard Similarity: n_users (rated item1 and item2) / n_users (rated item1 or item2), typically used in **Implicit Feedback** model.
    2. Cosine Similarity: cosine of the item vectors.
    3. Pearson Similarity：pearson coefficient between the item vectors.
- Model Based 
  - Matrix Factorization (SVD, SGD, ALS): Break a user-item feature matrix into a product of matrics, n_users * r_features AND r_features * m_items. The latent features are hidden features which are derived from the observed features using matrix factorization.
  - Deep Learning / Neural Net
- Graph Algorithms (pinterest recommendation system)
- Association Rules

# Evaluate
- RMSE doesn't tell a true story, always low….
- Ranking Metrics: MAP(classification) and NDCG(regression)  
  - http://fastml.com/evaluating-recommender-systems/
  - http://sdsawtelle.github.io/blog/output/mean-average-precision-MAP-for-recommender-systems.html

# Library
- Lightfm: https://github.com/lyst/lightfm
- Surprise: http://surpriselib.com/
- Implicit: https://github.com/benfred/implicit
- Spotlight: https://github.com/maciejkula/spotlight
- Fastai: https://github.com/fastai/fastai/tree/master/fastai
- Pyspark ALS: http://www.learnbymarketing.com/993/pyspark-als-and-recommendation-outputs/
- Crab: https://github.com/muricoca/crab
- Graph Lab: https://turi.com/
