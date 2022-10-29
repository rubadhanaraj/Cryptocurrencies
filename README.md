# Cryptocurrencies
## Overview 
The purpose of the analysis is to analyze data using unsupervised machine learning techniques algorithms, which help us explore data without a clear output in mind.
K-means algorithm was used, which is the main unsupervised algorithm that groups similar data into clusters. Principal component analysis (PCA), which employs many different features was also used to speed up the process.The main objectives of this project were
* Describe the differences between supervised and unsupervised learning, including real-world examples of each.
* Preprocess data for unsupervised learning.
* Cluster data using the K-means algorithm.
* Determine the best number of centroids for K-means using the elbow curve.
* Use PCA to limit features and speed up the model.

## Results 
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked us to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. The data was not ideal, so it had to be processed to fit the machine learning models. Since there is no known output, unsupervised machine learning was used. To group the cryptocurrencies, clustering algorithm was used. Data visualisation have been used to share the findings.

1. Preprocessing the Data for PCA 
A DataFrame is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df DataFrame 

![image](https://user-images.githubusercontent.com/108298416/198807100-b5b70d82-7e9f-4f36-bb83-523b125165f0.png)

2. Reducing Data Dimensions Using PCA
The Principal Component Analysis (PCA) algorithm was applied to reduce the dimensions of the X DataFrame to three principal components and these dimensions were placed in a new DataFrame.

![image](https://user-images.githubusercontent.com/108298416/198809732-ee648013-30d2-4982-ad49-b8e4f8280843.png)

3. Clustering Cryptocurrencies Using K-means
An elbow curve was created using hvPlot to find the best value for K.

![image](https://user-images.githubusercontent.com/108298416/198812170-f79be8a8-2c47-4d92-ba3d-74c20b252d8a.png)

CLustered dataframe was created by concatenating the crypto_df and pcs_df DataFrames on the same columns.

![image](https://user-images.githubusercontent.com/108298416/198812392-869e73a7-8973-49bf-8520-ee609379964c.png)
![image](https://user-images.githubusercontent.com/108298416/198812369-da6a7a43-70c7-4ab7-921b-299a8312c7ed.png)

4. Visualizing Cryptocurrencies Results
3D scatter plot was created using the Plotly Express function to plot the three clusters from the clustered_df DataFrame

![image](https://user-images.githubusercontent.com/108298416/198812507-7f533e9f-0b86-44e8-be6c-9c1ebbae3d60.png)

Tradable cryptocurrencies table was created using the hvplot.table() function. 

![image](https://user-images.githubusercontent.com/108298416/198812628-8968f395-80f4-47fe-ba59-934e329f01e0.png)

A hvplot scatter plot was created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data was ordered by "Class".

![image](https://user-images.githubusercontent.com/108298416/198812773-3e9fd2b0-f55d-4b61-962b-6001c676625f.png)

## Summary
* Based on the predictions of the K clusters for the cryptocurrencies data, the cryptocurrencies can be clustered into 4 groups.
* Based on the analysis, it is identified as there are 532 cryptocurrencies based on similarities of their features.
