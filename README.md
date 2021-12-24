# Credit_Risk_Analysis
## Overview

Credit risk is an inherently unbalanced classification problem, as good loans easily outnumber risky loans. Therefore, employing different techniques to train and evaluate models with unbalanced classes is necessary. The purpose of this project is to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling.

Using the credit card credit dataset, I oversampled the data using the RandomOverSampler and SMOTE algorithms, and undersampled the data using the ClusterCentroids algorithm. Then, I used a combinatorial approach of over- and undersampling using the SMOTEENN algorithm. Next, I compared two new machine learning models that reduce bias, BalancedRandomForestClassifier and EasyEnsembleClassifier, to predict credit risk. Finally, I evaluated the performance of these models and made a written recommendation on whether they should be used to predict credit risk.

## Results

### 1. Resampling Models
#### Oversampling

##### Naive Random Oversampling
![Navie Random Oversampling](https://user-images.githubusercontent.com/89143725/147320490-df724fbf-3945-4821-bcd0-6db6a5ce3198.png)

    - Accuracy: 61.6%

        High Risk: 
        - Precision: 1%
        - Recall: 61%

        Low Risk:
        - Precision: 100%
        - Recall: 68%
        
##### SMOTE Oversampling
  ![SMOTE Oversampling](https://user-images.githubusercontent.com/89143725/147320496-936a6685-1376-4e66-93c8-8dce3fc6e487.png)

    - Accuracy: 62.3%

        High Risk: 
        - Precision: 1%
        - Recall: 61%
        
        Low Risk:
        - Precision: 100%
        - Recall:  64%

#### Undersampling

##### Cluster Centroids
   ![Undersampling Cluster Centroids](https://user-images.githubusercontent.com/89143725/147320519-afdf7104-e75c-4bb0-a926-93001559baf7.png)

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
    ![Combination Sampling SMOTEENN](https://user-images.githubusercontent.com/89143725/147320534-87ab167e-7f92-45a5-8e8e-cc57cb971b73.png)

    - Accuracy: 61.6%

        High Risk: 
        - Precision: 1%
        - Recall: 69%
        
        Low Risk:
        - Precision: 100%
        - Recall:  54%

### 3. Ensemble Classifiers

##### Balanced Random Forest Classifier
![Balanced Random Forest Classifier](https://user-images.githubusercontent.com/89143725/147320539-02bb26d7-aa70-4b37-ab00-973649dd48b9.png)

    - Accuracy: 78.8%

        High Risk: 
        - Precision: 4%
        - Recall: 67%
        
        Low Risk:
        - Precision: 100%
        - Recall: 91%

##### Easy Ensemble Classifier
![Easy Ensemble AdaBoost Classifier](https://user-images.githubusercontent.com/89143725/147320547-832141d2-1d93-4971-8c3f-684dc642a34c.png)

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








