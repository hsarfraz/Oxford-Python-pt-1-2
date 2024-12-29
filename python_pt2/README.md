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

## Week 3: Supervised Learning: Regression

## Week 4: Supervised Learning: Classification

## Week 5: More Classification, Decision Trees. Ensemble Methods

## Week 6: Introduction to Neural Networks and Deep Learning

## Week 7: Deep Learning: CNNs for Image Processing and RNNs for Time Series Analysis

## Week 8: Dimensionality Reduction and Unsupervised Learning

## Week 9: RNNs for NLP. Attention-based models (Transformers)

## Week 10: GANs, Autoencoders and Reinforcement Learning
