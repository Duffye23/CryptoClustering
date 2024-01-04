# CryptoClustering

THe point of this challenge was to work on unpervised machine learning. Plotting the original data, we can see that a few of the x values are leaps and bouds above the rest. To normalize this result so our testing is meaningful, I applied a standard scalar.</br>

Image of the original data. You can see the spikes.</br>
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/7c1f395e-0b7d-4a92-bf34-6fe06a8b3c77)</br>

Data after it has been normalized, it is much more compact and there are no outliers: </br>
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/98774e0a-119e-44b3-b007-df04c394664a)</br>

I then found the best number of cluster groups to use for the model.</br>
The inertia curve kinks at k=4, indicating that our optimal cluster total is 4 for this dataset.
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/22d3eb78-a885-42fd-97d1-60b54ad54d6e)</br>

I then fit the normalized data to the KMeans model with the number of clusters set to 4 (as we discerned to be the optimal amount). 
While grouped, the data is still fairly intermingled</br>
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/8dc4f91c-cafe-439c-bd7f-8f5fd7132dbe)</br>

The next step was to repeat the process but instead we applied Principal Component Analysis which seeks to amalgamate information into smaller components for more accurate exploration. As prompted I selected the data be split into 3 components, and the three components combined to explain 88.442851% of the data.</br>
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/c0be88cb-844f-4e9a-9233-cf8e25b327e6)</br>

I then calculated the optimal k value for the PCA exploration and it once again came out to 4.</br>
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/f8129770-8fdb-48b6-aa04-1dd10390f2ab)</br>

I then completed the same procedure as above with the PCA data and created the following plot:</br>
![image](https://github.com/Duffye23/CryptoClustering/assets/58863493/4bcb3d8b-7f56-4af5-9311-be55fa567418)</br>

AS you can tell, the PCA scatter plot has the same number of clusters as the regular cluster method but are much more distinct in their clusters. We can conclude that PCA allows for a more distinct cluster spread and therefore sorting.</br>

Sources Used:
- Carleton Bootcamp zoom recordings and lesson activities.
