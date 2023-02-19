# Sampling
Assignment on Sampling for UCS654

## Description
This assignment has a dataset regarding credit cards.
It is a binary classification problem.
The dataset is imbalanced and hence it is balanced by using random over sampling technique.
After balancing the dataset, different sampling techniques are used and 5 different models have been applied to get the accuracy on testing set.
The dataset is divided into a 25-75 ratio of testing and training set.

## Methodology
1. Balancing Dataset
2. Creating different types of samples
3. Training different machine learning models
4. Testing the models
5. Analysing the Result obtained

## Sampling Technique Description and Sampling Size Formula
1. Simple Random Sampling
A simple random sample is a subset of a statistical population in which each member of the subset has an equal probability of being chosen.

![image](https://user-images.githubusercontent.com/72306997/219949613-305e70c5-37f5-4e5d-815e-92e1f4d31f5e.png)

>Z = 1.96 (for 95% confidence)
>
>p = 0.5
>
>E = 0.03 (assumed 3%)
>
>n = 1067

2. Stratified Sampling
Stratified sampling is a method of sampling that involves the division of a population into smaller subgroups known as strata.

![image](https://user-images.githubusercontent.com/72306997/219949629-2e744eff-ae24-4702-8899-83dba4ec9670.png)

>Z = 1.96 (for 95% confidence)
>
>p = 0.5
>
>E = 0.07 (assumed 7%)
>
>S = 2
>
>n = 784 (392 for each class)

3. Systematic Sampling
Systematic sampling is a probability sampling method where we select members of the population at a regular interval.
Samples taken on every 5th interval

4. Cluster Sampling
Cluster sampling is a probability sampling method in which we divide a population into clusters and then randomly select some of these clusters as sample.

>Rows per Cluster = 20
>
>Number of Clusters = 28 (sqrt(n/2) where n is the total number of rows)

5. Multi-Stage Sampling
In this method we have used a combination of sampling technique, i.e. cluster and simple random. The dataset is divided into clusters and then random samples are chosen from those clusters.


## Final Result Table
|                        | Simple Random | Stratified | Systematic | Cluster | Multi-Satge |
| ---------------------- | ------------- | ---------- | ---------- | ------- | ----------- |
| Logistic Regression    |91.01          |91.32       |79.22       |91.30    |94.00        |
| Decision Tree          |99.62          |96.42       |92.20       |95.65    |92.00        |
| Support Vector Machine |69.66          |63.26       |70.12       |72.17    |70.00        |
| Gaussian Naive Bayes   |76.02          |75.00       |77.92       |66.95    |58.00        |
| K-Nearest Neighbors    |98.12          |95.91       |92.20       |88.69    |86.00        |

## Discussion
From the table, we can conclude that we achieve maximum accuracy when we apply Decision Tree Algorithm upon taking samples using the Simple Random Sampling technique. We get an accuracy of 99.62%.

___

## License
[MIT](https://choosealicense.com/licenses/mit/)

___

## Written By
Name : Vaibhav Verma
  
Roll No. : 102003423

Sub-Group: 3CO17
