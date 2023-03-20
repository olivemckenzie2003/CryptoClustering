# CryptoClustering

Challenge: Python and unsupervised learningto predict if crpytocurrences are affected by 24 hour or 7 day prices

File "Crypto_Clustering.ipynb" contains all the python code.

Used StandardScaler() module from scikit-learn to normalize the data from the CSV file "crypto_market_data.csv"
create a DataFrame with the scaled data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.



Find the Best Value for k Using the Original Scaled DataFrame
Use the elbow method to find the best value for k using the following steps:
Create a list with the number of k values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.



Cluster Cryptocurrencies with K-means Using the Original Scaled Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the original scaled data:
Initialize the K-means model with the best value for k.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
Create a copy of the original data and add a new column with the predicted clusters.
Create a scatter plot using hvPlot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Color the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.



Optimize Clusters with Principal Component Analysis
Using the original scaled DataFrame, perform a PCA and reduce the features to three principal components.
Retrieve the explained variance to determine how much information can be attributed to each principal component 
Create a new DataFrame with the PCA data and set the "coin_id" index from the original DataFrame as the index for the new DataFrame.
Find the Best Value for k Using the PCA Data

Find the best value for k using PCA data
Use the elbow method on the PCA data to find the best value for k using the following steps:
Create a list with the number of k-values from 1 to 11.
Create an empty list to store the inertia values.
Create a for loop to compute the inertia with each possible value of k.
Create a dictionary with the data to plot the Elbow curve.
Plot a line chart with all the inertia values computed with the different values of k to visually identify the optimal value for k.


Cluster Cryptocurrencies with K-means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:
Initialize the K-means model with the best value for k.
Fit the K-means model using the PCA data.
Predict the clusters to group the cryptocurrencies using the PCA data.
Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot as follows:
Using hvPlot, create a scatter plot by setting x="PC1" and y="PC2". Color the graph points with the labels that you found by using K-means. Then add the crypto name to the hover_cols parameter to identify the cryptocurrency that each data point represents. (4 points)

Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.


Create a composite plot by using hvPlot to compare the elbow curve that you created from the original data with the one that you created from the PCA data. 

Create a composite plot by using hvPlot to compare the cryptocurrency clusters that resulted from using the original data with those that resulted from the PCA data. 
