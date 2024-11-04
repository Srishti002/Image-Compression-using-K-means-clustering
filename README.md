# Image Compression using K-means clustering 
## Introduction 
This project is about *Image Compression* using *K-Means* clustering
### Clustering :
- Clustering comes under unsupervised learning means labels are not present.
- Clustering looks for one particular type of structure in data.
  ![](https://github.com/Srishti002/Image-Compression-using-K-means-clustering/blob/main/Images/Screenshot%202024-11-04%20154243.png)
- There are various clustering techniques but here we are using K-Means

### K-Means Clustering :
- K-Means clustering gropus unlabelled data into *K* number of clusters and the value of K is predefined.
- K-Means algorithm :
  
  > Given a particular unlabelled data and we have to group this data into K number of clusters.
  
  > The first step here is to randomly initialize k cluster centroid n1,n2,n3...nk.

  > Then we assign labels to our data by calculating the distance between the centroids and data points. A particular datapoint is alloted the Label of that centroid whose distance with it is minimum.
  
  > Now, we have to move our cluster centroids in order to get perfect result. So, we will take mean of all datapoints associated with a paticular centroid. Whatever the mean comes we shift this particular centroid to the mean value . This process happens with all the clusters present.

  > The above two steps that is assiging labels and moving centroids are repeated to N number of iterations untill we get perfect results.

  ![](https://github.com/Srishti002/Image-Compression-using-K-means-clustering/blob/main/Images/Screenshot%202024-11-04%20160532.png)

  The above image shows K=3 means we have to divide our data into three groups. This image shows how initially we have randomly initialized centroids and then we have moved our centroids to get the perfect result and number of iterations is 10.

## Step By Step Guide :

1. First load the desired image whichu want to compress
2. Then convert it into 2D shape.
3. Now randomly initialize the centroids.
   ![]()
