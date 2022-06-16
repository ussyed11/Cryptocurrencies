# Cryptocurrencies
## Overview
Accountability Accounting, a prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. So, they’ve asked us to create a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment.

The data we will be working with is not ideal, so it will need to be processed to fit the machine learning models. Since there is no known output for what we are looking for, we decided to use unsupervised learning. To group the cryptocurrencies, we decided on a clustering algorithm. We’ll use data visualizations to share our findings with the board.

## Procedures and Results
The imported DataFrame before cleaning had 1252 rows of data.  We cleaned the dataframe to keep the current trading ones that have a working algorithm. We droped all the rows with nulll values. We dropped the trading column as we already retrieved the needed values. Then we standardized out data through via StandardScaler() function.  

After we standardized the data, we used PCA to reduce dimension to three principal components and created a new dataframe.  Then we used this data for clustering crytocurrencies using K-Means by creating an elbow curve to find the k values as shown in the image below from our code:

![Screen Shot 2022-06-16 at 3 53 54 PM](https://user-images.githubusercontent.com/98566486/174162864-ec65e8f1-b73a-42a2-b3db-10d723647def.png)

Then we created a new DataFrame including predicted clusters and cryptocurrencies features and by combining the crypto_df and pcs_df DataFrames on the same columns. We generated the 3D-Scatter with the PCA data and the clusters.

![Screen Shot 2022-06-16 at 3 56 01 PM](https://user-images.githubusercontent.com/98566486/174163170-b5df03af-9590-4cf8-a490-5dbf5fc22fa9.png)

![Screen Shot 2022-06-16 at 3 56 17 PM](https://user-images.githubusercontent.com/98566486/174163298-e1e5505e-6a25-46cf-8d0a-0d9dd2082ba6.png)


After that, we created a table with tradable cryptocurrencies and print the results.  We found that there are 532 tradeable cryptocurrencies:

![Screen Shot 2022-06-16 at 5 05 34 PM](https://user-images.githubusercontent.com/98566486/174163558-485e9a14-c7e6-4ab9-a103-d51ccdab73f9.png)

Finally, we created a new DataFrame that has the scaled data.  We used this scaled data to create a hvplot scatter plot:

![Screen Shot 2022-06-16 at 3 56 51 PM](https://user-images.githubusercontent.com/98566486/174163913-e325816c-3eae-4e54-a948-1f5ba8c35cb9.png)

## Summary

Through our unsupervised machine learning analysis, we demonstrated cryptocurrencies can be clusteredin groups. While there are differences between all cryptocurrencies, there are definitive categorizations by our finding. We not only have found clustering patterns, but also identified outliers. Our finding is useful to help a business venture to further explore the world of cryptocurrencies and potiential investments. 
