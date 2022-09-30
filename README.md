# Credit_Risk_Analysis 
## Overview of the Credit Risk Analysis:
##### Credit risk is an inherently unbalanced classification problem, as good loans greatly outnumber risky loans. In this exercise I'll be comparing several machine learning techniques to train and evaluate an unbalanced credit card dataset to see which model best predicts credit risk. 6 different machine learning models will be evaluated using the metrics of precision, recall (sensitiviy), & balanced accuracy. The following techniques will be used:

  - Oversampling the data via the **RandomOverSampler** and **SMOTE** algorithms
  - Undersampling the data via the **ClusterCentroids** algorithm
  - A combination approach of over & undersampling using the **SMOTEENN** algorithm
  - Compare two different ensemble classifiers, the **BalancedRandomForestClassifier** and **EasyEnsembleClassifier** algorithms


## Results:
### RandomOverSampler Model
![01RandomOverSampler](https://user-images.githubusercontent.com/105818879/193207622-8ac9d033-994c-40d5-8360-71d11ef78556.png)
  - balanced accuracy score: 65%
  - "high_risk" precision score: 1%
  - recall score: 62%
***

### SMOTE Model
![02SMOTE](https://user-images.githubusercontent.com/105818879/193207738-784b0d71-5409-4af3-a89c-93e8bc8aec4a.png)
  - balanced accuracy score: 65%
  - "high_risk" precision score: 1%
  - recall score: 63%
***

### ClusterCentroids Model
![03ClusterCentroids](https://user-images.githubusercontent.com/105818879/193207786-faecc562-05cb-44ce-9a62-9ea87a8384e5.png)
  - balanced accuracy score: 53%
  - "high_risk" precision score: 1%
  - recall score: 61%
***

### SMOTEENN Model
![04SMOTEENN](https://user-images.githubusercontent.com/105818879/193207835-18c94639-6f7a-41f9-b1dc-b52e4362c4f6.png)
  - balanced accuracy score: 63%
  - "high_risk" precision score: 1%
  - recall score: 71%
***

### BalancedRandomForestClassifier Model
![05BalancedRandomForestClassifier](https://user-images.githubusercontent.com/105818879/193207930-ab67576d-8959-4535-b21c-b0d4780fbe9b.png)
  - balanced accuracy score: 79%
  - "high_risk" precision score: 4%
  - recall score: 67%
***

### EasyEnsembleClassifier Model
![06EasyEnsembleClassifier](https://user-images.githubusercontent.com/105818879/193207979-220c5d91-dfc8-4d20-80cd-8cd46e036d1a.png)
  - balanced accuracy score: 93%
  - "high_risk" precision score: 7%
  - recall score: 91%

## Summary:
#### The two ensamble learning algorthms greatly outperformed the first four algorithms by combining weak learning algorithms into a strong learner. The EasyEnsembleClassifier correctly sorted 91% of "high risk" individuals into the "high risk" credit category. However, with a precision score of only 7% (0.07) it's reliability with regards to positive classification is still very low. Use of the algorithm would incorrectly classifly an enormous amount of "low risk" individuals as "high risk." I would not recommend using any of the models evaluated here for the purposes of accurately predicting credit risk.  
