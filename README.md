# Project5-OpenClassrooms
Segment the customers of an e-commerce site

## Business case
Olist is a Brazilian company that offers a sales solution on online marketplaces.

The company wants to provide its e-commerce teams with a customer segmentation that they can use on a daily basis for their communication campaigns.

For this mission, Olist provided an anonymized database containing information on order history, products purchased, satisfaction comments, and customer location since January 2017. 

## Objectives

My goal is to understand the different types of users through their behavior and personal data.

I will have to provide the marketing team with an actionable description of my segmentation and its underlying logic for optimal use, as well as a proposal for a maintenance contract based on an analysis of the stability of the segments over time

## Main results
Potentially interesting variables for segmentation were selected: monetary value, recency, frequency, customer reviews, variables associated with the delivery date, distance between seller and buyer and ratio between delivery costs and product prices.

Missing values were replaced and several analyses were realized:

-	Univariate analysis to study the distributions of variables. 
-	Outlier analysis 
-	An analysis of the correlations of the variables, which showed that the variables are weakly correlated
-	A PCA, which showed that recency and review_score explain a large part of the variance

After the EDA, several types of unsupervised models (K-Means, DBSCAN, Birch and Agglomerative Clustering) were tested using different combinations of variables.

The best segmentation is obtained by training a K-Means, with 6 clusters, on the RFM variables + review_score. This segmentation allows to distinguish between loyal customers, recent customers, customers who placed a single order and very dissatisfied customers.

A limitation of segmentation is that most customers placed a single order. If customers start to place more orders, the segmentation may need to be changed; if that’s the case, we will have more information on the 'average' behavior of customers and other variables may help to better differentiate the client groups.

## Aquired skills
-	Tune the hyperparameters of an unsupervised algorithm in order to improve it
-	Evaluate the performance of an unsupervised learning model
-	Develop an unsupervised learning model adapted to the business problem

