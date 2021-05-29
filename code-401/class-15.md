# intro to machine learning


**Supervised Learning**

Supervised learning includes tasks for "labeled" data (i.e. you have a target variable).

- In practice, it's often used as an advanced form of predictive modeling.
- Each observation must be labeled with a "correct answer."
- Only then can you build a predictive model because you must tell the algorithm what's "correct" while training it (hence, "supervising" it).
- Regression is the task for modeling continuous target variables.
- Classification is the task for modeling categorical (a.k.a. "class") target variables.


**Unsupervised learning**

Unsupervised learning includes tasks for "unlabeled" data (i.e. you do not have a target variable).

- In practice, it's often used either as a form of automated data analysis or automated signal extraction.
- Unlabeled data has no predetermined "correct answer."
- You'll allow the algorithm to directly learn patterns from the data (without "supervision").
- Clustering is the most common unsupervised learning task, and it's for finding groups within your data.


### Exploratory Analysis

The purpose of exploratory analysis is to "get to know" the dataset.


### Data cleaning
Better data beats fancier algorithms.



The first step to data cleaning is removing unwanted observations from your dataset.

This includes duplicate or irrelevant observations.

- check for typos or inconsistent capitalization.

### Feature Engineering


Feature engineering is about creating new input features from your existing ones.


**Combine Sparse Classes**

The next heuristic we’ll consider is grouping sparse classes.

Sparse classes (in categorical features) are those that have very few total observations. They can be problematic for certain machine learning algorithms, causing models to be overfit.


### Model Training
There are a variety of performance metrics you could choose from. 

- For regression tasks, we recommend Mean Squared Error (MSE) or Mean Absolute Error (MAE). (Lower values are better)
- For classification tasks, we recommend Area Under ROC Curve (AUROC). (Higher values are better)
