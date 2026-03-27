<head>
<title>k-Nearest Neighbors</title>
<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    displayMath: [['$$', '$$'], ['\\[', '\\]']]
  }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>
</head>

# k-Nearest Neighbors
Reading
* James et al., 4.1 An Overview of Classification
* James et al., 4.2 Why Not Linear Regression?
* James et al., 2.2.3 The Classification Setting
* James et al., 3.5 Comparison of Linear Regression with k-Nearest Neighbors

## Classification Models
<img src="https://raw.githubusercontent.com/drolsonmi/math3480/refs/heads/main/Notes/Images/3480_ML_Landscape.png" width=550 alt="Machine Learning Landscape">

With regression models, we were able to measure the effectiveness of models by taking the distance between our predicted value ($\hat{y}$) and the true value ($y$). In classification models, however, the output is simply which class an observation belongs to - there is no distance to measure. 

For example, if you have a picture of a cat and a model classifies it as a horse, how do you measure the distance between the prediction of horse and the true value of cat? You can't. So, we go to a different form of evaluation:
* Confusion Matrix
* Accuracy, Precision, Recall, F1-Score

There are a number of classification models. Most of these will be addressed in MATH 3480. This semester, we will focus on the k-Nearest Neighbors algorithm.

## The Concept behind k-Nearest Neighbors
The k-Nearest Neighbors (kNN) algorithm takes a point and gives it a classification based on the characteristics of points near it.

The value of $k$ tells kNN to look at the $k$ nearest points.
* Count the number of neighbors with each category
* The category with the highest count becomes the classification of our point in question

> Example: Cats have sharper claws and shorter ears, dogs have less sharp claws and longer ears
>    * Create graph on the board with claw sharpness on the x-axis and ear length on the y-axis
>    * Add a number of 'C' and 'D' points to the board to indicate pre-known values
>    * Add another unknown point 
>    * Count the number of nearby points and make an estimate of what the unknown point likely is


## Potential Problems/Questions
As $k$ changes, it could change the result. How do we know what value of $k$ to use? This is kind of arbitrary, but we generally use the following rule:
$$k = \sqrt{n}$$

What if the number of points around my point is split evenly between groups?
* If $k$ is even, we could be equally balanced between two categories
* If $k$ is a multiple of the number of groups to classify, we could be equally balanced between all categories
* Put it all together $\to$ choose a prime $k$ near $\sqrt{n}$


### Distance Measures
How do we determine the distance? 

#### Euclidean Distance
The __euclidean distance__ is the typical distance we have learned since gradeschool. It can be depicted with a right triangle and solved using the Pythagorean Theorem.

First, let's say that we have two points $a$ and $b$. We want the distance $d$ between $a$ and $b$. Let's define $d_x$ to be the distance in the x-dimension, so $d_x = a_x - b_x$. Then we can depict the distance between two points as a right triangle with sides $d_x$ and $d_y$ with $d$ as the hypoteneuse.

In 2 dimensions, the distance between points $a$ and $b$ is $d$ and can be calculated as,

$$d = \sqrt{d_x^2 + d_y^2}$$

In 3 dimensions, the distance is,

$$d = \sqrt{d_x^2 + d_y^2 + d_z^2}$$

What would be the distance in $n$ dimensions?

$$d = \sqrt{\sum_{i=0}^n d_i^2}$$

#### Manhattan Distance
With the euclidean distance, we squared each term. Why? Because Pythagoras showed if we want it to make sense physically, it needs to be that way. However, there are other ways to express distance.

Imagine you are in New York City and you want to go from $a$ to $b$. Can you go in a straight line? Not likely. You likely actually have to travel the length of $d_x$ and $d_y$. In this case,

$$d = d_x + d_y$$

Essentially, we are just adding the length of all the dimensions together. Because this example demonstrates the idea so well, we often call this type of distance the __Manhattan distance__. In $n$ dimensions,

$$d = \sum_{i=0}^n |d_i|$$

#### Norms
We have seen how to measure a distance with a power of 1 and with a power of 2. Can we do it with a power of 3? 4? 20? 100? Yes! This distance measure is often called a __Norm__. When we deal with a norm of power $p$, we specifically call it an $L_p$ norm.

$$L_p = \left(\sum_{i=0}^n |d_i|^p\right)^{1/p}$$

* The Manhattan Distance is an L1-Norm since it is based on a power of 1
* The Euclidean Distance is an L2-Norm since it is based on a power of 2

#### Infinity Norm
There is another useful norm that is commonly seen, known as the L$\infty$-Norm.

$$L_\infty = \left(\sum_{i=0}^n |d_i|^\infty\right)^{1/\infty}$$

What does this do?
* Consider the $L_p$ norm for a very large $p$
* Dimensions with large measures will become exponentially large, and dimensions with small measures will become insignificant
* The larger $p$ becomes the more insignificant the smaller dimensions become
* At some point, only the largest dimension will remain

$$L_\infty = \left(\sum_{i=0}^n |d_i|^\infty\right)^{1/\infty} = \max{d_i}$$

Many of these norms are used throughout Data Science. With the kNN algorithm, the standard (default) option is generally the euclidean distance. 

## Hard Classification vs. Soft Classification
Let's take an example where we have a sample of 100 training points being divided into three categories A, B, and C. We take the nearest $k$ points where $k$ is the prime number nearest $\sqrt{n} = \sqrt{100} = 10$. So, let's choose $k=11$.

We put a point on the graph and count the nearest $k=11$ points and get the following results:
  |   A   |   B   |   C   |
  | :---: | :---: | :---: |
  |   2   |   8   |   1   |

Once we have counted the $k$ nearest neighbors, how do we interpret the counts?

Classification models often have two methods to interpret:
* With __Hard Classification__, we count the cases in each class and the majority wins
  * Since B had the most counts, we classify our point in category B.
* With __Soft Classification__, we calculate a percentage for each class and report a probability of being in each class
  * $P(A) = \tfrac{3}{11} = 0.18$
  * $P(B) = \tfrac{8}{11} = 0.73$
  * $P(C) = \tfrac{1}{11} = 0.09$