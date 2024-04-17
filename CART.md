# Classification and Regression Trees (CART)

When a Decision Tree classifies the predicted output into categories, it is called a Classfication Tree. \
When a Decision Tree predicts numeric values it is called Regression Tree.

**Which feature to choose to start classification at the very top of the tree?**
* We use each input feature to classify the output feature only once, and calculate the impurity of the classification. 
* If a leaf has perfect classification, it is called *Pure* leaf, but if the classification is not perfect in a leaf (meaning, it has misclassifed some data), then the leaf is called *Impure* leaf. 
* We choose the feature with lowest impurity over other features as first decision tree node. 


**How do you quantify the impurity of the leaf?**
* There are various methods to quantify the impurity. The most popular one is Gini Impurity. Other ones are Entropy and Information Gain.

**How do you calculate Gini Impurity of a categorical feature?**
* Gini Impurity for the left leaf node derived from classification in decision tree: 
$$ G_{Left} = 1 - (p(Yes))^2 - (p(No))^2 = 1 - (\frac{N_{Yes|Left}}{N_{Yes|Left} + N_{No|Left}})^2 - (\frac{N_{No|Left}}{N_{Yes|Left} + N_{No|Left}})^2$$ 
* Similarly, Gini Impurity for the right leaf node derived from classification in decision tree:
$$ G_{Right} = 1 - (p(Yes))^2 - (p(No))^2 = 1 - (\frac{N_{Yes|Right}}{N_{Yes|Right} + N_{No|Right}})^2 - (\frac{N_{No|Right}}{N_{Yes|Right} + N_{No|Right}})^2$$  
* But the number of data points on the left leaf node $(N_{Yes|Left} + N_{No|Left})$ is not equal to the data points on the right leaf node $N_{Yes|Right} + N_{No|Right}$. That means, the Gini Impurity calculated for the two nodes do not carry same weight. 
* Therefore, the Total Gini Impurity of the Decision tree stump is the weighted average of the two Gini Impurities: 
$$(\frac{N_{Left}}{N_{Left} + N_{Right}})G_{Left} + (\frac{N_{Right}}{N_{Left} + N_{Right}})G_{Right}$$

**How do you calculate Gini Impurity of a numerical feature?**
*

**How to prevent overfittng of a Decision Tree?**