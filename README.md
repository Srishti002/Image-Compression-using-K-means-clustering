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

1. First load the desired image which you want to compress
2. Then convert it into 2D shape.
3. Now randomly initialize the centroids. Here K=16 means we are selecting 16 different pixels from 16384 pixel values.
   
   ![](https://github.com/Srishti002/Image-Compression-using-K-means-clustering/blob/main/Images/Screenshot%202024-11-04%20164657.png)

4. Now assign label to the rest of the pixel values means here we have selected our K=16 so initially 16 pixels as centroids were selected randomly so now we have to assign these values to the the rest of the pixels. Here we are calculating euclidean distance.

   ![](https://github.com/Srishti002/Image-Compression-using-K-means-clustering/blob/main/Images/Screenshot%202024-11-04%20164847.png)

6. Now we have to move our cluster centroids by calculating the mean of datapoints associated with the particular cluster.

   ![](https://github.com/Srishti002/Image-Compression-using-K-means-clustering/blob/main/Images/Screenshot%202024-11-04%20170251.png)

7. Result :

   ![](https://github.com/Srishti002/Image-Compression-using-K-means-clustering/blob/main/Images/Screenshot%202024-11-04%20184547.png)

## Conclusion :
An Image consists of many different unique colours. After converting image(128 * 128 * 3) into 2D form we get *16384 * 3* . This means that each row represents each pixel of image and each column represents color channel. 1 pixel = 3 bytes for RGB and 1 byte = 8 bits (0-255). We will select K=16 colors from above 16384 unique colors. So we will have 16 clusters which will perfectly represent all 16384*3 colors. Each original pixel is replaced by its nearest centroid. Instead of storing RGB values we only store the *16 centroid colors(16 * 3)* and index (0,1,2...15) for each pixel (16384 values)

Memory savings :
Original :- 16384 * 3 values = 49152 values
Compresses :- (16 centroids * 3 ) + 16384 = 16432 values

