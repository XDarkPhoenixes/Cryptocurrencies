# Cryptocurrencies

## Purpose
Using unsupervised machine learning to discover trends and groupings in different cryptocurrencies in order to convince the firm Accountability Accounting to invest in those new currencies.

### Preprocessing the Data for Principal Component Analysis (PCA)
For preprocessing, only those cryptocurrencies that are being traded, having a working algorithm, and having coins mined were kept.

![Is-Trade](https://user-images.githubusercontent.com/84931545/142740160-72597ac3-8f16-4c05-90cb-24677a0ddfec.PNG)

![mined](https://user-images.githubusercontent.com/84931545/142740163-2998eaeb-c4b7-486a-9107-67143892e0f6.PNG)

![working_algorithm](https://user-images.githubusercontent.com/84931545/142740170-12d47e22-0e3d-4ad6-a3a8-75274c565e7f.PNG)


get_dummies() method was used to create variables for the two text features. StandardScaler() was used to standardize the data. 

![Get_dummies](https://user-images.githubusercontent.com/84931545/142740174-6e2085b8-3e82-4d7c-a7d9-42a57618e167.PNG)

![Standard](https://user-images.githubusercontent.com/84931545/142740183-b7cec77a-d201-4cea-bed7-9b222d90cb9c.PNG)


### Reducing Data Dimensions Using PCA.
The dimensions of the DataFrame were reduced to three.

![three_dimensions](https://user-images.githubusercontent.com/84931545/142740192-81fc78ae-0acb-4f5a-951e-50cb68568175.PNG)

### Clustering Cryptocurrencies Using K-means
An elbow curve using hvPlot was created and the best value for K is found. K-means algorithm was run to make predictions of the K clusters for the cryptocurrencies' data. The prediction was added to the new DataFrame after concatenation.

![K-mean](https://user-images.githubusercontent.com/84931545/142740195-48afa294-8ece-4503-85be-40dd9ae43caf.PNG)
![run](https://user-images.githubusercontent.com/84931545/142740203-d3ce453e-b4c5-4dac-a890-065ee38b6b1d.PNG)
![Concat](https://user-images.githubusercontent.com/84931545/142740211-51914f34-7559-4e73-8991-12fae20db3b5.PNG)

## Visualizing Results.

![4](https://user-images.githubusercontent.com/84931545/142740216-f5f8bc60-d313-4aed-8ceb-155d7c3ef348.PNG)

3D scatter plot shows 4 clusters; There are 532 tradable cryptocurrencies. A table with tradable cryptocurrencies was created using hvplot.table(); After scaling the tradable cryptocurrencies using MinMaxScaler(), a scatter plot was created showing 4 clusters with respect to TotalCoinSupply and TotalCoinsMined.



![table](https://user-images.githubusercontent.com/84931545/142740227-7b94e084-3c81-46e7-bc58-242d5383e823.PNG)

![scatter](https://user-images.githubusercontent.com/84931545/142740753-dae961b6-a9ce-4a62-875a-1f85f0bfe957.PNG)



