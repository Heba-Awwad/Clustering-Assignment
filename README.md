# Clustering-Assignment
Clustering Assignment  for DM
Clustering Algorithms
In this Assignment you will explore and experiment with clustering in some of its applications in image segmentation. This assignment focusses on two clustering techniques: K-means and DBSCAN. K-means is one of the most commonly used clustering methods as it is quite easy to understand and implement.
The data sets for problem one can be found in the file Mnist.zip which is accessible through the course’s Moodle page. the dataset represents the pixel gray value of the 28x28 digit images. The compressed file include two CSV files “mnist_train,csv” and “mnist_test.csv”merge them together to get one file, which it consists of 70000 records and 785 columns, 784 for attributes and 1 for label (the digit image value).
<img width="1566" height="719" alt="image" src="https://github.com/user-attachments/assets/012e32b2-a301-4d22-b3aa-ae93cf6784c5" />
Set number of iterations (MAX ITER) to 20 and number of clusters k to 10 for all the experiments carried out. Your driver program should ensure that the correct number of iterations are run
Problem A
Use the Euclidean distance as the distance measure for clustering, and to compute the cost function SSE for every iteration t.
𝑆𝑆𝐸=ΣΣ𝑑𝑖𝑠𝑡2(𝑚𝑖,𝑥)𝑥∈𝐶𝑖𝐾𝑖=1
1.
Generate a graph where you plot the cost function SSE(t) as a function of the number of iterations t=1...20.
2.
What is the percentage change in cost after 10 iterations of the K-Means algorithm
(Hint: to be clear, the percentage refers to (cost[0]-cost[9])/cost[9].)
3.
Generate a graph where you plot the accuracy as a function of the number of iterations t=1...20.
4.
Generate a graph where you plot the Silhouette Coefficient as a function of the number of iterations t=1...20
Problem B
Repeat the experiment as part A but using cosine similarity as a measure similarity for clustering and the cost function as
𝐶𝑆𝑆𝐸=ΣΣ(1−𝑐𝑜𝑠(𝑚𝑖,𝑥))𝑥∈𝐶𝑖𝐾𝑖=1
1.
Generate a graph where you plot the cost function SSE(t) as a function of the number of iterations t=1...20.
2.
What is the percentage change in cost after 10 iterations of the K-Means algorithm
3.
Generate a graph where you plot the accuracy as a function of the number of iterations t=1...20.
4.
Generate a graph where you plot the Silhouette Coefficient as a function of the number of iterations t=1...20
5.
Is Euclidean distance K-Means better than cosine similarity K-Mean in terms of cost function? Explain your reasoning.
Problem C
Use the Silhouette Coefficient to find the best number of clusters k for the data set. i.e. run the k-mean algorithm for k = 1, 2,….,40 and calculate the Silhouette Coefficient. Generate a graph where you plot the Silhouette Coefficient as a function of the number of cluster k=1...40.
1.
When Euclidean distance is used as the distance measure for clustering
2.
When cosine similarity is used as a measure similarity for clustering
Note: the best number of k is the knee of the graph.
Doe the best k found is equal to 10 in both cases.
Note: how to calculate the accuracy of clustering
Once you finish an iteration of clustering,
First label the clusters.
Labeling cluster ci by and digit j is by:
counting the labels of the data point in the cluster ci
sort the data point counts in increasing order
consider the label of the cluster ci is the label of the data point with the max count.
Second
Accuracy of cluster ci is the ration between the data points label by the ci label to the all-data points in the cluster ci
Finally
The whole clustering accuracy is the average of the cluster’s accuracy.
