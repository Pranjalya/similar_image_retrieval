# Similar Image Retrieval

*You can find the Google Colaboratory notebook [here](https://colab.research.google.com/github/Pranjalya/similar_image_retrieval/blob/master/Image_Retrieval.ipynb)*

**A similar image retrieval system using Autoencoders in Tensorflow framework.**

### Steps
1. Build a an encoder and decoder architecture.
2. Since we have unlabelled dataset, we train the model by computing the loss between original and reconstructed image by the network.
3. Having trained, we store the intermediate latent vectors for the images.
4. For similar image retrieval, I have demonstrated 2 approaches:
  1. *Using Euclidean Distance*
      - Compute the Euclidean distance betwen the image you want to search for and other images.
      - Return the n closest images with least distances.
    
  2. *Using Clustering approach*
      - Cluster the latent vectors using K Means or MiniBatch K Means.
      - Get the images from the cluster for the image you want to retrieve.
      - [ToDo] Add elbow technique to get a better intuition to the number of clusters.
