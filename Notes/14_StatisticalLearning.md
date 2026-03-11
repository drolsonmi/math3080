# Statistical Learning
Reading
* James et al., Chapter 2

## What is Statistical Learning?
This is an umbrella term for all statistical algorithms used to learn from data
* aka Data Mining
* aka Machine Learning
* algorithms aka models

These are a list of some of the common models that we will be seeing through this semester and the next:

![Machine Learning Landscape](https://raw.githubusercontent.com/drolsonmi/math3480/refs/heads/main/Notes/Images/3480_ML_Landscape.png)

* What are supervised models? 
* What are unsupervised models?

We'll learn most of these models throughout the three semesters. This semester, we will for sure learn:
* Linear Regression
* Logistic Regression
* Possibly k-Nearest Neighbors
* Possibly another if there's time

## Notation
Some common notation:
* $y$ is used for true output values
* $\hat{y}$ is used for predicted output values from a model
* $\vec{x}$ is a vector, or a series of values, such as input for a model
* $\mathbf{A}$ is a matrix, or a series of vectors, like a dataset or a series of observations - similar to the DataFrame or more like the 2D numpy array we have already seen 
* $x_{ij}$ is the $j^{th}$ variable (column) of the $i^{th}$ observation (row) in a dataset (matrix)

Other notation can be given as we go along.

## Statistical Learning
Let's consider a study comparing Years of Education to a person's Income.
> Draw a series of points that are almost sigmoidal with noise

In truth, there may be a relationship between the years of education and the income. This relationship is $f(x)$. 
> Draw $f(x)$ with a light grey color

However, no value exactly follows this relationship, so the true equation is,

$$y = f(x) + \epsilon$$

where $\epsilon$ is a random error term. This is truth.

In reality, though, we usually don't know $f(x)$. We often have no way of knowing if there even is a true relationship. So, we are left to analyze (like we did using the tools we learned before Spring Break) and to create models to try to follow statistical patterns to estimate $f(x)$. This estimate is now $\hat{f}(x)$.
> Draw $\hat{f}(x)$ somewhat off of $f(x)$

Since we have no way of estimating $\epsilon$, this is the best we can often do, so,

$$\hat{y} = \hat{f}(x)$$

## Statistical Error
Can we improve $\hat{f}(x)$? Absolutely! There are two error quantities involved in this prediction:
* __Reducible error__: The part of the error we can minimize as we bring $\hat{f}(x)$ closer to $f(x)$
* __Irreducible error__: The part of the error we can't reduce because of the noise (random error term $\epsilon$)

To explain this mathematically, we can find the expected value of the squared difference between the predicted and true values of y.

$$\begin{align*}E(y-\hat{y})^2 &= E[f(x) + \epsilon - \hat{f}(x)]^2 \\
&= [f(x) - \hat{f}(x)]^2 + Var(\epsilon)\end{align*}$$

The term $[f(x) - \hat{f}(x)]^2$ represents the reducible error as we can minimize this difference as the model improves. However, the random errors in $Var(\epsilon)$ can never be reduced.

As a result, there will always be an upper bound on our accuracy metrics. If we ever get a 100% accuracy measurement on our models, we should be very suspicious...


## Models vs. Inference
In one of our first lectures, we learned that there are three stages to Data Science, and we used an astronomical example for this:
1. Gathering data (Tico Bray collected data on planetary motion)
2. Analysis and Modeling (Johannes Kepler created equations that seemed to explain planetary motion)
3. Explanation and Generalization (Isaac Newton created the Law of Universal Gravitation which gave meaning to Kepler's equation and explained planetary motion)

Let's revisit this in light of what we have learned about Statistical Learning. 

When we are modeling, our goal is to find the value of $\hat{y}$, but the function $\hat{f}(\vec{x})$ is ultimately not important. (This was Kepler's job in the astronomy example.)
* In some cases, this function is unknown - a black box. 
* In fact, some argue that Neural Networks shouldn't be used at all because even though we know the number that make the model $\hat{f}(\vec{x})$, we really don't have any meaning to those numbers

However, when we are doing Inference, our goal is not necessarily to find the value of $\hat{y}$, but to understand and estimate $f(x)$ itself. (This was Newton's job in the astronomy example.)