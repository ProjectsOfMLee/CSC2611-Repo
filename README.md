# CSC2611-Repo-MingyiLi

[Question-1-Synchronic word embedding](https://github.com/ProjectsOfMLee/CSC2611-Repo/blob/main/LabQ1_MingyiLi.ipynb)

[Question-2-Diachronic word embedding](https://github.com/ProjectsOfMLee/CSC2611-Repo/blob/main/LabQ2_MingyiLi.ipynb)

- Calculate cosine distance between each pair of word embeddings you have extracted, and report the Pearson correlation between word2vec-based and human similarities. [1 point] 
  - PearsonRResult(statistic=0.830817384168786, pvalue=5.943545020602274e-11))
- Comment on this value in comparison to those from LSA and word-context vectors from analyses in the earlier exercise. [1 point]
  - The results from the previous exercise:
    - Pearson Correlation between Human and M1: PearsonRResult(statistic=0.32, pvalue=0.01)
    - Pearson Correlation between Human and M1Plus: PearsonRResult(statistic=0.19, pvalue=0.10)
    - Pearson Correlation between Human and M2_10: PearsonRResult(statistic=0.19, pvalue=0.13)
    - Pearson Correlation between Human and M2_100: PearsonRResult(statistic=0.37, pvalue=0.00)
    - Pearson Correlation between Human and M2_300: PearsonRResult(statistic=0.36, pvalue=0.00)

  - *The Pearson Correlation result between word2vec-based and human similarities is much closer to 1.0 than all the previous results (around 0.2 to 0.4) from LSA and word-context vectors, which suggests that word2vec embeddings reflect the similarity of word meanings better than LSA and word-context vectors from analyses in the earlier exercise, in the sense that word2vec results are much more positively correlated to human-deemed similarities.* 

