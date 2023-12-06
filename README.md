# Lazy FCA

A big homework to merge [Lazy Learning](https://en.wikipedia.org/wiki/Lazy_learning)
and [Formal Concept Analysis](https://en.wikipedia.org/wiki/Formal_concept_analysis).
Created for the course Ordered Sets in Data Analysis (GitHub [repo](https://github.com/AndrewDiv/FCALC))
taught in Data Science Master programme in HSE University, Moscow. 

# Task description

## Intention of the homework
 
This homework serves as an entry point for students into the data science world.     
So it introduces students to three main topics: 
1. **Typical machine learning project**: \
   The loading a dataset, feature engineering, designing a new predictive algorithm, results comparison;     
2. **Lazy learning**: \
   Predicting labels for small or rapidly changing data; 

## To-do list

* Bare minimum (4 pts.)
  * [ ] Find a dataset for binary classification:\
  _Ideal dataset would be: openly available, with various datatypes (numbers, categories, graphs, etc),
  with hundreds of rows_;
  * [ ] Describe scaling (binarization) strategy for the dataset features,
  * [ ] Describe prediction quality measure best suited for the dataset \
   _(e.g. accuracy, f1 score, or any 
  [measure](https://en.wikipedia.org/wiki/Evaluation_of_binary_classifiers) that you find reasonable)_,
   

## How to submit

Students are expected to provide the working code and pdf report for their homework by the end of the semester. 

The code should be available on the students GitHub accounts.

A pdf report should describe the reasoning behind every step of your homework. For example,
it should contain a description of your dataset, what quality measure you have chosen (and why), 
how did you optimize the prediction function, etc.  

## Intro to baseline algorithm

### Binary classification setup

This homework focuses on the task of binary classification. 
That is, we are given the data $X = \\{x_1, x_2, x_3, ...\\}$
and the corresponding labels $Y$ where each label $y \in Y$ is either True of False.
The task is to make a "prediction" $\hat{y}$ of a label $y \in Y$ for each datum $x \in X$ as if $y$ is unknown.

To estimate the quality of predictions we split the data $X$ into two non-overlapping sets $X_{train}$ and $X_{test}$.
Then we make make a prediction $\hat{y}$ for each test datum $x \in X_{test}$
based on the information obtained from the training data $X_{train}$. 
Finally, we measure how well predictions $\hat{y}$ represent the true test labels $y$.  

The original data $X$ often comes in various forms: numbers, categories, texts, graphs, etc.
So to make all these kinds of data look the same we scale (binarize) the dataset. 
Now we can say that there are a set of attributes $M$ where each attribute $m \in M$ is either describes $x$ or not.
That is, we replace each $x \in X$ with its binary analogue $x_{bin} \subseteq M$.


