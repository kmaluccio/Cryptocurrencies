# Cryptocurrencies
In this project, we use unsupervised machine learning to find groupings, trends, or other information about cryptocurrencies to show why crypto is a good investment.

## Overview of analysis

We use unsupervised machine learning algorithms to learn about possible trends or patterns in cryptocurrencies. During this analysis, we find how many tradable cryptocurrencies there are currently and create visualizations to show the distinct groups that correspond to the three principal components found using the PCA algorithm on the data.

First, the data has to be preprocessed for PCA. To do this, we use pandas to help preprocess the data, perform data selection and prepare the data for the principal component analysis. The StandardScaler sklearn library (fit_transform) is used to standardize the features from the new data frame that was created using pandas. Then, using the PCA algorithm we reduce the data dimensions and are able to obtain three principal components. Next, we use K-means algorithm to cluster the cryptocurrencies into appropriate groupings by finding the best K value to use with the data frame we have created. Finally, we create visualizations including an elbow curve, a table showing the tradable cryptocurrencies and 2D/3D scatter plots made with poorly express and hvplot to show the distinct groups that correspond to the three principal components.


## Results

We begin by showing the top of the cryptocurrency data frame that has been loaded using pandas and the crypto CSV file.

![crypto dataframe](https://github.com/kmaluccio/Cryptocurrencies/blob/main/images/crypto-df.png)

Below is the elbow curve that shows us our best K value is 4.

![elbow curve](https://github.com/kmaluccio/Cryptocurrencies/blob/main/images/elbow-curve.png)

With the information from the elbow curve, we use k=4 and perform the K-means algorithm. The result of principal components is stored in a data frame shown below.

![principal components](https://github.com/kmaluccio/Cryptocurrencies/blob/main/images/principal-components.png)

Below is the 3D-scatter with PCA data and the clusters. To see the clusters more closely, you can zoom in or move the graph around and focus on sections or specific clusters of the data.

![three dimensional clustering](https://github.com/kmaluccio/Cryptocurrencies/blob/main/images/3Dcluster.png)

Below is the scatter plot with the scaled data that was found using MinMaxScaler with the tradable cryptocurrencies.

![scatter plot scaled](https://github.com/kmaluccio/Cryptocurrencies/blob/main/images/scatter-plot-scaledData.png)

- The python script is in a Jupyter Notebook file saved in the repo folder. The CSV cryptocurrency data can be found at [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

