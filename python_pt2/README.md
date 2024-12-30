# Python Programming for Data Science - Part 2 Syllabus Overview

## Week 1: Introduction to the Course / ML / Linear Regression

Skills needed for data science (Math & Stats, Computer Science, Subject Matter Expertise)

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/data%20science%20skills.jpg?raw=true)

Data Science Lifecycle (not all of these steps have to be taken but here are the general steps)

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/data%20science%20lifecycle.jpg?raw=true)

Data Types

1. Structured (tabular)
2. Semi-Structured (JSON, XML)
3. Unstructured (Images, text)

Traditional Computing vs. Machine Learning

* The main difference between traditional computing and ML is that in traditional computing you define your own set of rules for the program to follow but in ML, the program is given the data and will set the rules by itself

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/traditional_computing_vs_ML.jpg?raw=true)

Types of ML models (3 checks that you have to perform)

1. Ask whether the ML model is trained with human supervision (Supervised, Unsupervised, and Reinforcement Learning)
2. Can the model learn incrementally, on the spot? (online vs. batch learning)
3. Can the model compare new data points to known data points or does it detect patterns in the training data and build a predictive model (instance-based vs. model-based learning)

Supervised Learning (Classification & Regression)

* Classification: the data points are assigned a label
* Regression: In regression, the label belongs to a continuous range so you are trying to predict the function.
* Supervised learning examples: k-Nearest Neighbors, Linear Regression, Logistic Regression, Naive Bayes Classification, Support Vector Machines (SVMs), Gaussian Processes, Decision Trees and Random Forests, Ensemble Methods, Neural Networks

Unsupervised Learning (Clustering, Anomaly Detection, Dimensionality Reduction, Neural Networks)

* In unsupervised learning, the data does not have any labels so the ML model would need to identify patterns and create its own groups

Reinforcement Learning (Markov Decision Processes, Q-Learning)

* The computer program makes decisions and gets notified if it has made a good or bad decision. Based on this feedback, the computer program learns from its previous performance when making another decision

Batch vs. Online Learning

* Batch: Batch learning systems can't learn incrementally and can only be trained using available data. These types of systems can be trained offline and can then be launched into production
* Online: Systems that can be trained incrementally since they receive data sequentially either individually or in small groups called mini-batches

Instance-based vs. Model-based learning

* Instance-based (K-nearest neighbors): the model memorises the instances that they can seen in the training data and try to identify those patterns in the testing data
* Model-based (neural networks): the model used the neural network to identiy patterns/groups in the training data

Overfitting and Regularisation

* Overfitting is when the model performs well on the training data but it does not generalize well with new data
* Regularisation is when you make a model simple to reduce the risk of overfitting

Machine Learning Model Data Training Process

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/training_testing_validation_data_process.jpg?raw=true)

## Week 2: Overview of a data-science preprocessing pipeline

Steps needed in a Machine Learning Project

1. Understand the business problem
2. Get the data (this step can be hard especially whenit comes to cleaning data)
3. Discover and visualise the data to gain insights
4. Prepare the data for the Machine Learning algorithm
5. Select a model and train it
6. Fine-tune your model
7. Present your solution
8. Launch, monitor, and maintain your system

Understanding the problem and the type of ML model that needs to be used

Objective: to be able to predict the house prices in Kings County, Washington, US

* Is it supervised, unsupervised, or reinforcement learning?
    *  Supervised learning is required to predict the house prices in King County since you need samples of house pricing data to train the ML model to make predictions
* Is it a classification task, a regression task, or something else?
    *  The price of houses is a continuous variable and not a categorical variable
* Should you use batch learning or online learning techniques?
    *   Batch learning can be used since there isn't a huge number of datasets to process. Online learning would be needed if there were millions (or billions) of datasets that exsisted online.
 
Step 1: Things to observe in datasets to gain insights

*  Name of each attribute and its characteristics
*  Variable/attribute Type (categorical, int/float, bounded/unbounded, text, structured)
*  % of missing values
*  Noisiness and type of noise (stochastic, outliers, rounding errors, etc)
*  Usefulness for the task
*  Type of distribution (Gaussian, Uniform, Logarithmic)
*  For supervised learning tasks, identify the target attributes (what is variable gives the output)

Step 2: Ways to gain insights from data

* Visualize the data
* Study the correlations between attributes
* Study how you would solve the problem manually
* Identify the promising transformations you may want to apply
* Identify extra data that would be useful

Simple Statisitics: Sampling

* A sample aims to represent the whole population 

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/sampling.jpg?raw=true)

Simple Statisitics: Data, Variables, and Distributions

* Univariate and multivariate represent two approaches to statistical analysis. Univariate involves the analysis of a single variable in your data while multivariate analysis examines two or more variables
* Variables can be: quantitative, categorical, ordinal
* The variable distribution describes how many times a value appears in the dataset

Simple Statisitics: Characteristics of a distribution

* Central tendency: Do the values cluster around a particular point?
* Modes: Is there more than one cluster?
* Spread: How much variability is there in the values?
* Tails: How quickly does the probability drop off as we move away from the modes?
* Outliers: Are there extreme values far from the mode?

Summary Statistics: Central Tendency

* Mean: Central tendency of the distribution

$$
\overline{x} = \frac{1}{N} * \sum_{i=1}^{N} x_i
$$

* Median: The middle value in the dataset, one ordered
   * The median is a more robust estimator than the mean as it is less susceptible to outliers (values that differ substantially from the rest of the data) 
* Mode: The value (integer or categorical) that occur most frequently

Summary Statistics: Quantiles

* Quantiles are cut points dividing the range of a distribution into continuous intervals with equal frequencies probability
* Quartiles in statistics are values that divide your data into quarters

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/quartiles.jpg?raw=true)

Simple Statistics: Spread

* Variance: Describes the variability or spread of a distribution around the mean value

$$
s^2 = \frac{1}{N} \sum_{i=1}^{N} (x_i - \overline{x})^2
$$

* The square root of the variance is the standard deviation (s)
* Bessel's correction formula:

$$
s^2 = \frac{1}{N-1} \sum_{i=1}^{N} (x_i - \overline{x})^2
$$

Simple Statistics: Covariance

* If we have N samples $(x_i,y_i)$ from a bivariate distribution where i=1,...,N the covariance is an estimate of how variation in x is related to variation in y
* In simple terms, covariance lets us know the relationship between two or more variables
* The covariance is defined as:

$$
Cov(x,y) = \frac{1}{N-1} \sum_{i=1}^{N} (x_i - \overline{x})*(y_i - \overline{y})
$$

Simple Statistics: Covariance Matrix

* For multivariate data, variance and covariance can be expressed together in a covariance matrix V:

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/covariance_matrix.jpg?raw=true)

Simple Statistics: Covariance and correlation

* The Pearson's correlation coefficient between X and Y normalizes the covariance such that the statistics lies between -1 and 1

$$
Cov(x,y) = \frac{Cov(x,y)}{s_x s_y} =\frac{1}{N-1} \sum_{i=1}^{N} \frac{(x_i-\overline{x})*(y_i-\overline{y})}{s_x s_y})
$$

Hence, the correlation matrix C for x and y is:

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/pearsons_correlation_coefficient.jpg?raw=true)

Here is a graphical explanation of correlation:

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/correlation_graph.jpg?raw=true)

## Week 3: Supervised Learning: Regression

Regression Performance Measures/Metrics

* We need to look at how well a regression performs on a dataset when we look at a Machine Learning model. I have listed a list of regression performance measures below:
* Mean Square Error

$$
MSE = \frac{1}{N} \sum_{i=1}^{N} (y_i-\hat{y})^2
$$

Choose some Algorithms

* The next step is to identify some good regression algorithms that we can use to train a few models. Here are some examples of Regression Algorithms:
* Linear Regression: Ordinary Least Squares
   * Closed form solution (Normal Equation)
   * Gradient Descent
* Polynomial Regression
* Regularized Models
   * Ridge Regression
   * Lasso Regression
* Decision Trees Regression
* Something else (Support Vector Machines, Neural Networks...)
* Ensemble Models, Random Forests

![Skills Chart](https://github.com/hsarfraz/Oxford-Python-pt-1-2/blob/main/image/linear_regression.jpg?raw=true)

Gradient Decent

* Our goal is to minimize the random error $\epsilon_i$ for the $x_i$ value (this is shown by they yellow line in the image). To do this, we would need to tweat the weights $\beta$ iteratively to minimize the cost function
* To minimize the cost function, we would need to measure the local gradient of the error function with respect to the the weights $\beta$ and tweak $\beta$ in the direction of the decending gradient. Once the gradient equals zero, you have reached a minimum.

## Week 4: Supervised Learning: Classification

## Week 5: More Classification, Decision Trees. Ensemble Methods

## Week 6: Introduction to Neural Networks and Deep Learning

## Week 7: Deep Learning: CNNs for Image Processing and RNNs for Time Series Analysis

## Week 8: Dimensionality Reduction and Unsupervised Learning

## Week 9: RNNs for NLP. Attention-based models (Transformers)

## Week 10: GANs, Autoencoders and Reinforcement Learning
