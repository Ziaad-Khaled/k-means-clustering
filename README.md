# K-Means Image Clustering and Classification

This project implements the K-means clustering algorithm to cluster images from the CIFAR-10 dataset into three categories: airplane, bird, and truck.

## Project Description

The project follows these key steps:

1. **K-Means Clustering with K = 3**:
   - The K-means algorithm is applied to the images in the train folder with K set to 3.
   - To ensure robustness, the algorithm is run 10 times with different random initializations, as the choice of initialization can significantly impact the results.

2. **Selecting the Best Clustering Outcome**:
   - The Davis Bouldin index is used to determine the best clustering outcome among the 10 runs from Step 1.

3. **Classifying Images by Majority**:
   - For each class of images (airplane, bird, and truck), the project identifies the cluster to which the majority of images belong.
   - For example, if the majority of airplane images are assigned to Cluster 3, then Cluster 3 is considered as the cluster representing the airplane class.

4. **Image Classification**:
   - The cluster centers identified in Step 3 are used to classify the images in the test folder.
   - Classification is based on the shortest Euclidean distance between each image and the cluster centers. 
