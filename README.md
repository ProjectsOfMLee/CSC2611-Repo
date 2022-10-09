# CSC2611-Repo-MingyiLi

[Question-1-Synchronic word embedding](https://github.com/ProjectsOfMLee/CSC2611-Repo/blob/main/LabQ1_MingyiLi.ipynb)

[Question-2-Diachronic word embedding](https://github.com/ProjectsOfMLee/CSC2611-Repo/blob/main/LabQ2_MingyiLi.ipynb)

Q1

- Calculate cosine distance between each pair of word embeddings you have extracted, and report the Pearson correlation between word2vec-based and human similarities. [1 point] 
  - PearsonRResult(statistic=0.830817384168786, pvalue=5.943545020602274e-11))
- Comment on this value in comparison to those from LSA and word-context vectors from analyses in the earlier exercise. [1 point]
  - The rounded by 2 results from the previous exercise:
    - Pearson Correlation between Human and M1: PearsonRResult(statistic=0.32, pvalue=0.01)
    - Pearson Correlation between Human and M1Plus: PearsonRResult(statistic=0.19, pvalue=0.10)
    - Pearson Correlation between Human and M2_10: PearsonRResult(statistic=0.19, pvalue=0.13)
    - Pearson Correlation between Human and M2_100: PearsonRResult(statistic=0.37, pvalue=0.00)
    - Pearson Correlation between Human and M2_300: PearsonRResult(statistic=0.36, pvalue=0.00)

  - *The Pearson Correlation result between word2vec-based and human similarities is much closer to 1.0 than all the previous results (around 0.2 to 0.4) from LSA and word-context vectors, which suggests that word2vec embeddings reflect the similarity of word meanings better than LSA and word-context vectors from analyses in the earlier exercise, in the sense that word2vec results are much more positively correlated to human-deemed similarities.* 

- Report the accuracy on the semantic analogy test and the syntactic analogy test [2 points] 
  - 0.7401448525607863 
- Repeat the analysis with LSA vectors (300 dimensions) from the earlier exercise, comment on the results in comparison to those from word2vec. [1 point] 
  - (rounded by 4) 0.0012 for semantic analogy test & 0.0028 for syntactic analogy test  
  - Comment:
    - LSA analogy test accuracy results are remarkably lower than those derived from word2vec
    - In terms of syntactic and semantic word modeling, word2vec performs much better than LSA in analogy tasks
- Suggest a way to improve the existing set of vector-based models in capturing word similarities in general, and provide justifications for your suggestion. [2 points]
  
  There are several ways to improve the existing vector-based models in capturing word similarities:
  1. Learn and capture deeper and multiple meanings of words will reduce the mistakes in calculating similarity. Bidirectional models such as ELMo, BERT and ERNIE would beat the above-mentioned models. Because they are trained to learn the word embeddings from more contexts through architectures such as bidirectional deep LSTM layers and transformers with multi-head attention layers. This encapsulates the word meanings better and hence can increase the accuracy in capturing word similarities. While the existing set of vector-based models like word2vec map 1 vector to 1 word, this sometimes mix up and collapse different semantics and syntaxes that English words often have, causing inaccuracy in the calculation of word similarities.
  2. So far the existing set of vector-based models have not considered word position, which is key to a better representation of both syntactic and semantic aspects. Incorporate word position in context (sentence, document, etc.) will improve the existing set of vector-based models in capturing word similarities in general.
  3. Another way of improving the exist set of vector-based models in capturing word similarities  Measuring how common they are in different geographical places. For example, there exist different analogies in different english-speaking countries that aren't used elsewhere often. 
  4. (Maybe we could consider developing/crafting a loss function when doing analogy test.)
