#
# Crypto Clustering

## Description:
* Applying the __K-means__ algorithm and __principal component analysis (PCA)__ to __classify cryptocurrencies__ according to their __price fluctuations__ across __various timeframes__. Specifically, price changes over __intervals spanning 24 hours, 7 days, 30 days, 60 days, 200 days,__ and __1 year__.
#
## __Process__:
* __Find__ the __Best Value for k__ Using the __Original Scaled DataFrame__ and the __Elbow Method__.
    * __Result__:
        * The __best value__ for __k__ is __4__.
* __Cluster Cryptocurrencies__ with __K-Means__ Using the __Original Scaled Data__ with __4 clusters__.
* __Optimize Clusters__ with __Principal Component Analysis__.
    * __Result__:
        * __The total explained variance__ of the __three principal components__ is __89.5%__.
* __Find__ the __Best Value for k__ Using the __PCA Data__ and the __Elbow Method__.
    * __Result__:
        * The __best value__ for __k__ is __4__, __not differing__ from the __original scaled data__.
* __Cluster Cryptocurrencies__ with __K-Means__ Using the __PCA Data__ with __4 clusters__.
* __Determine__ the __Weights__ of __Each Feature__ on __Each Principal Component__.
    * __Results__:
        * __PCA1__: 
            * __price_change_percentage_200d__ and __price_change_percentage_1y__ have the __strongest positive influence__ at __59%__ and __56%__. 
            * __price_change_percentage_24h__ has the __strongest negative influence__ at __-41%__
        * __PCA2__: 
            * __price_change_percentage_30d__, __price_change_percentage_14d__ and __price_change_percentage_60d__ have the __strongest positive influence__ at __56%, 54%__ and __43%__. 
            * __price_change_percentage_1y__ has the __strongest negative influence__ at __-15%__.
        * __PCA3__: 
            * __price_change_percentage_7d__ has the __strongest positive influence__ at __78.7%__. 
            * __price_change_percentage_60d__ and __price_change_percentage_24h__ have the __strongest negative influence__ at __-36%__ and __-21.8%__.