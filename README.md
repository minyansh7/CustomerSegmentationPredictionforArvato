# CustomerSegmentationPredictionforArvato
Capstone Project: Create a Customer Segmentation Report for Arvato Financial Services


1. [Project Introduction](#motivation)
2. [Project Summary and Thoughts](#summary)
4. [Licensing, Authors, and Acknowledgements](#licensing)


 
## 1. Project Introduction<a name="motivation"></a>
In the project, a mail-order sales company in Germany is interested in identifying segments of the general population to target with their marketing in order to grow. Demographic information has been provided for both the general population at large as well as for prior customers of mail-order company in order to build a model of the customer base of the company. The target dataset contains demographic information for targets of a mail-out marketing campaign. The objective is to identify which individuals are most likely to response to the campaign and become customers of the mail-order company.

## 2. Project Summary and Thoughts<a name="summary"></a>
I. PCA Componets Analysis

In this project, PCA analysis is applied to reduce the dimensions of the data for clustering and modelling. It compressed the data from 215 dimensions to 152 components while preserved 95% variance.

To tackle the challenge of explainging the PCA components of identified clusters, I use cluster centres as represents of clusters. Inverse analysis of PCA components are implemented to obtain the original attributes and values for those center points. In this way, the typical characteristics of customer segments are obtained.

II. Metrics Selection for Supervised Machine Learning Classification

When comes to supervised machine learning modelling for prediction, there are in depths in metrics selection. GridSearchCV is implemented using ROC_AUC score.It measures the distinguishment between positive and negative classes, which are customers who respond and who don’t respond. 

Unlike accuracy score, the most common evaluation metrics is not appropriate this case. As it only counts the positive class for the group of customers who respond, while most of people show no response to the campaign in the training dataset. Thus, accuracy should not be used.

III. Further Improvement

Logistic Regression model is identified as the best model for building the prediction modelling. The best score is 0.563481. Apply the model upon MAILOUT_TEST dataset, and achieve the final score of 0.55985 on Kaggle. The closer the score to 1, the better the performance of the model. We can see there are still room for improvement considering data cleaning and feature tranformation and modeling process.


## 3. Licensing, Authors and Acknowledgements<a name="licensing"></a>
Must give credit to Arvato for the data.

Thanks to Udacity community's knowledge sharing that supports the project.



## If you are interested in this project, please see my project post:https://tinyurl.com/2knpwzwz
