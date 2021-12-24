# Credit_Risk_Analysis

## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, employing different techniques to train and evaluate models with unbalanced classes is necessary. The purpose of this project is to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally, I evaluated the performance of these models and made a written recommendation on whether they should be used to predict credit risk.

## Results

### 1.Resampling Models
#### Oversampling

##### Naive Random Oversampling

    - Accuracy: 61.6%

        High Risk: 
        - Precision: 1%
        - Recall: 61%

        Low Risk:
        - Precision: 100%
        - Recall: 68%
        
##### SMOTE Oversampling
  
    - Accuracy: 62.3%

        High Risk: 
        - Precision: 1%
        - Recall: 61%
        
        Low Risk:
        - Precision: 100%
        - Recall:  64%

#### Undersampling

##### Cluster Centroids
   
    - Accuracy: 62.3%

        High Risk: 
        - Precision: 1% 
        - Recall: 57%
        
        Low Risk:
        - Precision: 100%
        - Recall:  45%


### 2. SMOTEENN Algorithm

#### Combination (Over and Under) Sampling

##### SMOTEENN
    
    - Accuracy: 61.6%

        High Risk: 
        - Precision: 1%
        - Recall: 69%
        
        Low Risk:
        - Precision: 100%
        - Recall:  54%

### 3. Ensemble Classifiers

##### Balanced Random Forest Classifier

    - Accuracy: 78.8%

        High Risk: 
        - Precision: 4%
        - Recall: 67%
        
        Low Risk:
        - Precision: 100%
        - Recall: 91%

##### Easy Ensemble Classifier

    - Accuracy: 93.2%

        High Risk: 
        - Precision: 4%
        - Recall: 67%
        
        Low Risk:
        - Precision: 100%
        - Recall:  91%


## Summary
It can be seen that Easy Ensemble AdaBoost method is superior compared to other methods. It results in higher balanced accuracy score, precision, and recall. I believe this is due to the reduction in bias that these methods provide. 
  
However, precision for high-risk group is still very low (ie. 0.09). Since precision is a measure of how reliable a positive classification is, I would recommend neither of these methods as none are reliable for high-risk groups. Therefore, more data is needed for a reliable recommendation. 








