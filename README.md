
# Euclidean and Manhattan Distance Calculations


<p align="center">
  <img width="600" height="400" src="https://miro.medium.com/max/657/1*p2WnXXcQZzcFt3NHX50VjA.png">
</p>

## 1. Introduction:

In this short mini project we will see examples and comparisons of distance measures. Specifically, we'll visually compare the Euclidean distance to the Manhattan distance measures. The application of distance measures has a multitude of uses in data science and is the foundation of many algorithms we'll be using such as Princical Components Analysis (PCA).

A good distance metric helps in improving the performance of Classification, Clustering, and Information Retrieval process significantly. In this article, we will discuss different Distance Metrics and how do they help in Machine Learning Modelling.

## 2. Euclidean Distance

The “Euclidean Distance” between two objects is the distance you would expect in “flat” or “Euclidean” space; it’s named after Euclid, who worked out the rules of geometry on a flat surface. The Euclidean is often the “default” distance used in e.g., K-nearest neighbors (classification) or K-means (clustering) to find the “k closest points” of a particular sample point. The “closeness” is defined by the difference (“distance”) along the scale of each variable, which is converted to a similarity measure. This distance is defined as the Euclidian distance.

Mathematically, it’s calculated using Pythagoras’ theorem. The square of the total distance between two objects is the sum of the squares of the distances along each perpendicular co-ordinate.

We are using Pandas to load our dataset .CSV file and use Numpy to compute the __Euclidean distance__ to the point (Y=5, Z=5 and Y=3, Z=3) that we choose as reference. On the left here we show the dataset projected onto the YZ plane and color coded per the Euclidean distance we just computed. As we are used to, points that lie at the same Euclidean distance define a regular 2D circle of radius that distance.

Note that the __SciPy library__ comes with optimized functions written in C to compute distances (in the scipy.spatial.distance module) that are much faster than our (naive) implementation.

<p align="center">
  <img width="600" height="400" src="https://raw.githubusercontent.com/mohamedziane/DistanceInMachineLearning_Euclidean_and_Manhattan/main/images/img1.png">
  <img width="600" height="400" src="https://raw.githubusercontent.com/mohamedziane/DistanceInMachineLearning_Euclidean_and_Manhattan/main/images/img2.png">

</p>

## 3. Manhattan Distance Metric

Manhattan distance is simply the sum of absolute differences between the points coordinates. This distance is also known as the taxicab or city block distance as it measure distances along the coorinate axis which creates "paths" that look like a cab's route on a grid-style city map.

We display the dataset projected on the XZ plane here color coded per the Manhattan distance to the (X=5, Z=5) reference point. We can see that points laying at the same distance define a circle that looks like a Euclidean square.

Applications of Manhattan distance metric include:

- Regression analysis: It is used in the linear regression to find a straight line that fits a given set of points

- Compressed sensing: In solving an underdetermined system of linear equations, the regularisation term for the parameter vector is expressed in terms of Manhattan distance. This approach appears in the signal recovery framework called compressed sensing

- Frequency distribution: It is used to assess the differences in discrete frequency distributions.

<p align="center">
  <img width="600" height="400" src="https://raw.githubusercontent.com/mohamedziane/DistanceInMachineLearning_Euclidean_and_Manhattan/main/images/img3.png">
  <img width="600" height="400" src="https://raw.githubusercontent.com/mohamedziane/DistanceInMachineLearning_Euclidean_and_Manhattan/main/images/img4.png">
</p>

## 4. Euclidean vs. Manhattan Distance Comparison

Now let's create distributions of these distance metrics and compare them. We leverage the scipy dist function to create these matrices similar to how you manually created them earlier in the exercise.

<p align="center">
  <img width="600" height="400" src="https://raw.githubusercontent.com/mohamedziane/DistanceInMachineLearning_Euclidean_and_Manhattan/main/images/img5.png">
</p>

## 5. Bonus: Cosine Similarity

Cosine similarity calculates similarity by measuring the cosine of angle between two vectors.

Mathematically speaking, Cosine similarity is a measure of similarity between two non-zero vectors of an inner product space that measures the cosine of the angle between them. The cosine of 0° is 1, and it is less than 1 for any angle in the interval (0,π] radians. It is thus a judgment of orientation and not magnitude: two vectors with the same orientation have a cosine similarity of 1, two vectors oriented at 90° relative to each other have a similarity of 0, and two vectors diametrically opposed have a similarity of -1, independent of their magnitude. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
