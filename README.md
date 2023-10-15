# Aquifer

Aquifer is a K-means clustering implementation in Python. It is not special. I am not rebranding my own special implementation as a new algorithm called "Aquifer". I just wanted to name it something better than "k-means-python" or something generic.

I am writing this code as a way for me to learn machine learning algorithms. This one, obviously, is being written to learn the K-means clustering algorithm.

I was first exposed to this Algorithm in COGS 118B (unsupervised machine learning) at UCSD. Our first project of the quarter was to implement K-means clustering, as well as multi-dimensional gaussian clustering algorithms that I completely forget. The task was to cluster MNIST dataset. I really like K-means because of how simple it is. We worked on this project overnight probably from around 9PM to 6AM and I think only the first 40 minutes of it was spent working on the K-means algorithm. The rest was the gaussian stuff. I'm mentioning that detail to give you insight into how much more complex the gaussian stuff was compared to the K-means algorithm. This is notable because, in the end, K-means did probably 90-95% as well as the gaussian clustering. It's also incredibly intuitive to understand. All around good algorithm.

## K-means clustering

K-means is a clustering algorithm. It is an unsupervised learning algorithm. It does not need to know the answers to be able to cluster the data into K classes.

### Algorithm

K-means works by iteratively clustering all datapoints into K clusters based on distance. That is the simplest case. As with the Kernel Trick with SVMs, I assume distance is not the only similarity metric that can be used. I will be using distance.

First, select K data points to serve as cluster centers

Then, until convergence (which I will discuss shortly), iterate over all data points, performing the following steps:

1. calculate the distance from point i to each cluster
2. assign this datapoint to the cluster whose center is nearest

Convergence is reached when less than some limit N points are re-assigned in a complete iteration over the dataset (I think).

This is all just based on my own understanding, I have not consulted any resources, so this could all be completely wrong.

## Data

Link to dataset [here](https://www.kaggle.com/datasets/franoisgeorgesjulien/nasa-exoplanet-archive-planetary-systems/data).
