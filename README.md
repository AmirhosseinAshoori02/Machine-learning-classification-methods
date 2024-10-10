# Machine Learning Classification Methods

## Table of Contents
1. [Support Vector Machine (SVM)](#support-vector-machine-svm)
2. [Decision Tree](#decision-tree)
3. [Neural Network, Random Forest, and K-Means](#neural-network-random-forest-and-k-means)
4. [Results and Visualizations](#results-and-visualizations)

---

## Support Vector Machine (SVM)

Support Vector Machine (SVM) is used in this project for classification tasks. The SVM algorithm works by finding the optimal hyperplane that separates classes. Here, both **hard margin** and **soft margin** approaches are explored:

- **Hard Margin**: This approach assumes data is linearly separable and tries to find a hyperplane that perfectly divides the classes without any error. It’s less flexible and is effective when classes are well-separated.
- **Soft Margin**: This variation allows some points to be on the wrong side of the hyperplane, introducing a penalty parameter (C) that controls the trade-off between maximizing the margin and minimizing classification error. This makes it more suitable for noisy data or overlapping classes.
- I trained these models on datasets that are generated using the DrawData library.

### Advantages
- Performs well on high-dimensional data and works with both linear and non-linear data.
  
### Disadvantages
- Requires parameter tuning and is computationally expensive for large datasets.

---

## Decision Tree

The Decision Tree algorithm in this project is implemented for classification tasks. It splits the data based on features that provide the best separation of classes. The splitting criteria used here include **Gini Impurity** and **Entropy**. These criteria measure the impurity or disorder at each node, guiding the decision tree to make splits that increase the purity of the classes in each leaf.

- **Gini Impurity**: Measures the frequency of a random sample being incorrectly classified.
- **Entropy**: Measures the disorder or impurity; lower entropy indicates a more orderly distribution.
- I trained this model on lung cancer dataset.

### Advantages
- Simple to interpret and visualize with minimal preprocessing requirements.
  
### Disadvantages
- Prone to overfitting and sensitive to noisy data.

---

## Neural Network, Random Forest, and K-Means

This section includes **Neural Network**, **Random Forest**, and **K-Means** models:

### Neural Network
The Neural Network model is used for handling complex, non-linear relationships. It consists of interconnected layers where each neuron is connected to neurons in the next layer. This model is particularly well-suited for tasks involving unstructured data, like images or text.
- I trained this model on heart dataset.
- **Advantages**: Suitable for complex tasks and able to model non-linear relationships.
  
- **Disadvantages**: Computationally expensive, requires significant tuning, and may overfit on small datasets.

### Random Forest
Random Forest is an ensemble method that combines multiple decision trees. Each tree is trained on a different subset of data and features, reducing overfitting and improving accuracy. The final prediction is an average (for regression) or a majority vote (for classification) of all trees in the forest.
- I trained this model on Dataset_1.
- **Advantages**: Reduces overfitting, handles large datasets well, and provides feature importance scores.
  
- **Disadvantages**: Less interpretable than a single decision tree and requires more computational resources.

### K-Means Clustering

K-Means is an unsupervised learning algorithm used for clustering data into groups. The algorithm works by defining `k` centroids and then assigning each data point to the nearest centroid, iteratively refining the positions of the centroids until the assignments no longer change. The goal is to minimize the variance within clusters.
- I trained this model on heart dataset.
- **Advantages**: Simple and easy to implement, Efficient for large datasets.

- **Disadvantages**: Requires pre-specifying the number of clusters (k), Sensitive to initial placement of centroids, which can affect result, Struggles with clusters of varying sizes and densities.

---

## Results and Visualizations

### 1. Decision Tree
The Decision Tree model achieved an accuracy of **100%**. Below is the visualization of the trained Decision Tree:

![Decision Tree](./Decision%20Tree.png)

### 2. Support Vector Machine (SVM) - Hard Margin
The Hard Margin SVM was used to classify data that is linearly separable without any errors, providing a clear decision boundary between classes.

![Hard Margin SVM](./Hard%20Margin.png)

### 3. Support Vector Machine (SVM) - Soft Margin
The Soft Margin SVM introduces flexibility by allowing some data points to lie on the wrong side of the margin, making it suitable for data with minor overlaps or noise.

![Soft Margin SVM](./Soft%20Margin.png)

### 4. K-Means Clustering
K-Means clustering was applied to group data into distinct clusters based on similarity. The visualization below shows the clusters formed and the centroids.

![K-Means Clustering](./Kmeans.png)

### 5. Neural Network
The Neural Network was employed to capture complex relationships in the dataset, achieving an accuracy of **88%**. The network architecture is visualized below:

![Neural Network](./Nueral%20Network.png)

### 6. Random Forest
The Random Forest model, an ensemble of decision trees, provided robust performance with an accuracy of **99%**. Below is a visualization of one of the trees in the Random Forest:

![Random Forest](./Random%20forest.png)

---

### Summary of Accuracies:
- **Decision Tree**: 100%
- **Neural Network**: 88%
- **Random Forest**: 99%

Each model visualization and result demonstrates the effectiveness and differences between various machine learning approaches applied to the dataset in this project.

## Conclusion

This project provides a hands-on implementation of various machine learning algorithms, each with its unique strengths and weaknesses. Through this exploration, we aim to understand the conditions under which each algorithm excels, providing insights for future applications in different data contexts.
