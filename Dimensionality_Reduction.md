# Dimensionality Reduction

Why reduce the dimension of the feature space? 
1. Curse of dimensionality
1. To avoid overfitting during training phase
1. Easier data collection
1. Interpretability
1. Computational Efficiency
1. Storage Space

There are two flavors of Dimensionality Reduction: 
1. Feature Selection 
2. Feature Extraction


## Feature Selection
1. Filter Methods
    1. Variance Threshold - Univariate Statistcs
    1. Pairwise Correlation - Bivariate Statistics
    1. Correlation with Target
    1. Information Gain
1. Embedded Methods
    1. L1 (LASSO) Regularization
    1. Decision Trees and Random Forest Feature Importance
1. Wrapper Methods
    1. Recursive Feature Elimination (RFE)
    1. Sequential Feature Selection (SFS)
    1. Permutation Importance

### Filter Methods
- Analyzing the intrinsic properties of the features themselves. 

### Embedded Methods
- These methods of feature selection are embedded into the model algorithm itself and they are part of optimizing the objective function. 

### Wrapper Methods
- We fit the model on different subsets of the features, and based on the performance of the model according to the baseline model (or a previous model), we eliminate a feature or more and proceed iteratively. 

