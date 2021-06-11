# Breast-Cancer-Detection-using-KNN

# _RESULT_
I built a system for Benign or Malignant cancer classification based on various features like cell shape, cell size, mitoses rate, etc
On the given dataset, KNN performed better than other  possibly signifying that the ***dataset is not linearly separable*** (there could be other reasons also, like, outliers in the data set). This conforms to what scatter plot of features from dataset showed.

<img src="https://github.com/harshdeep1230/Breast-Cancer-Detection/blob/main/Breast-Cancer-Detection-using-KNN/images/10.png"  />

### DATASET
Link for the dataset used
https://archive.ics.uci.edu/ml/machine-learning-databases/breast-cancer-wisconsin/

**_DATA PREPROESSING_**
I removed empty(?) values from dataset and replaced it with some very large negative value so it can be ignored by training algorithm. I also removed id column to as it does not provide any usefull information.

##  [K-nearest neighbors (KNN)](https://medium.com/@adi.bronshtein/a-quick-introduction-to-k-nearest-neighbors-algorithm-62214cea29c7)
A **supervised** learning algorithm can be used for both classification and regression predictive problems.

KNN is a [**non-parametric**](https://machinelearningmastery.com/parametric-and-nonparametric-machine-learning-algorithms/), [**lazy learning**](https://sebastianraschka.com/faq/docs/lazy-knn.html) algorithm.
>When we say a technique is non-parametric , it means that it does not make any assumptions on the underlying data distribution. **Nonparametric methods are good when you have a lot of data and no prior knowledge, and when you don’t want to worry too much about choosing just the right features.**
>KNN is also a lazy algorithm (as opposed to an eager algorithm).It does not use the training data points to do any generalization, i.e., it doesn’t learn a discriminative function from the training data but “memorizes” the training dataset instead. 

KNN Algorithm is based on feature similarity: How closely out-of-sample features resemble our training set determines how we classify a given data point:

![](https://github.com/harshdeep1230/Breast-Cancer-Detection/blob/main/Breast-Cancer-Detection-using-KNN/images/1.png)

*Example of k-NN classification. The test sample (inside circle) should be classified either to the first class of blue squares or to the second class of red triangles. If k = 3 (outside circle) it is assigned to the second class because there are 2 triangles and only 1 square inside the inner circle. If, for example k = 5 it is assigned to the first class (3 squares vs. 2 triangles outside the outer circle).*

Some pros and cons of KNN
 
Pros:
- No assumptions about data — useful, for example, for nonlinear data
- the training phase is pretty fast ( no explicit training phase or it is very minimal)
- High accuracy (relatively) — it is pretty high but not competitive in comparison to better supervised learning models

Cons:
- Computationally expensive — because the algorithm stores all of the training data (Lack of generalization)
- High memory requirement
- Prediction stage might be slow (with big N)
