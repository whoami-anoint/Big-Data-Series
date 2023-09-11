# Unit 2: 
## Chapter 2 - Analytical Theory and Methods

[![Share on Twitter](https://img.shields.io/badge/-Share%20on%20Twitter-blue?logo=twitter&style=flat-square)](https://twitter.com/intent/tweet?text=https%3A%2F%2Fgithub.com%2Fwhoami-anoint%2FBig-Data-Series)
[![GitHub discussions](https://img.shields.io/github/discussions/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/discussions)
[![GitHub pull requests](https://img.shields.io/github/issues-pr/whoami-anoint/DevOps)](https://github.com/whoami-anoint/Big-Data-Series/pulls)

### Clustering and Associated Algorithms

### **Clustering Overview:**
  - Clustering is a fundamental data analysis technique used to group similar data points together based on certain similarity metrics.
  - It's valuable for discovering patterns, relationships, and structures in data.

 **K-Means Clustering:**
  - K-Means is a popular clustering algorithm.
  - It partitions data points into 'K' clusters based on the Euclidean distance between data points and cluster centroids.
  - It's used in various applications, including customer segmentation and image compression.

- **Hierarchical Clustering:**
  - Hierarchical clustering builds a tree-like structure of clusters.
  - It can be agglomerative (bottom-up) or divisive (top-down), where data points are merged or split based on similarity.
  - Hierarchical clustering is helpful in visualizing data hierarchies.

### Association Rules

- **Association Rules Overview:**
  - Association rules are used to discover interesting relationships between variables in large datasets.
  - They are typically expressed in the form of "if-then" statements, such as "If a customer buys product A, they are likely to buy product B."

- **Apriori Algorithm:**
  - Apriori is a classic algorithm for generating association rules.
  - It uses a level-wise search approach to find frequent itemsets (sets of items that often occur together).
  - The algorithm prunes infrequent itemsets, making it efficient for large datasets.

- **Support and Confidence:**
  - Support measures how frequently an itemset occurs in the dataset.
  - Confidence measures the likelihood that a rule is true.
  - Users can set minimum support and confidence thresholds to filter out less interesting rules.

### Candidate Rules

- **Candidate Rules in Apriori:**
  - In the Apriori algorithm, candidate rules are generated and tested iteratively.
  - The algorithm starts with individual items as candidates and progressively combines them into larger itemsets.
  - Candidate rules that meet the support and confidence thresholds become valid association rules.

- **Rule Pruning:**
  - Rule pruning is crucial to eliminate uninteresting or redundant rules.
  - It helps maintain a manageable set of rules for analysis.
  - Pruning techniques often involve removing rules that do not meet specified criteria or have lower significance.
