## When to use Machine Learning?

- Problems for which existing solutions require a lot of hand-tuning or long lists of rules Ex:- Spam Filter (Rule based spam filter will like contain a long list of ever expanding rules)
- Problems that are too complex for traditional approaches or no known algorithm Ex:- Speech Recognition
- Fluctuating Environments: ML system can adapt to new data Ex:- ML model can evolve to detect new types of spam easily
- Get insights about complex problems and large amounts of data Ex:- ML can uncover new patterns

## Type of Machine Learning

- Supervised
- Unsupervised
- Reinforcement
- Semi-supervised

> `Regression algorithms can be used for classification and vice versa` Ex:- Logistic Regression is commonly used for binary classification, it can also output the probability of belonging to a class

> Some Neural Networks can be unsupervised, such as autoencoders and restricted Boltzmann machines. They can also be semisupervised such as deep belief networks and unsupervised training

> Try dimension reduction before using ML algorithm. It will run much faster, the data will take less disk and memory space and in some cases also perform better

## Offline vs Online Learning

- Offline a.k.a batch learning
- System is incapable of learning incrementally
- Training using the full dataset can take hours, lot of computing resources and a lot of money
- Autonomous systems (smart phones or Mars rover) has limited resources

- Online learning is great for systems that receive data as a continuous flow
- Incrementally train on data
- How fast online learning systems adapt to data is called `learning rate`
- If bad data is fed to an online learning system's performance will gradually decline
- Closley monitor input drift and model performance

## Instance-Based vs Model-Based Learning

- How well ML generalize to perform well on unseen data
- Instance based learning generalizes based on similarity distance
- Build model using examples and use model to predict

> Fitness function measures how good the model is while a Cost function measures how bad is the model

## Main Challenges of Machine learning

> Bad data or Bad Algorithm

> The Unreasonable Effectivenss of Data - Fairly simple algorithms and complex ones performed identically well once they were given enough data
> Trade off spending time between algorithm development vs corpus development

- Non representative training data
  - Leads to poor model performance
  - Sampling bias - 1936 US Presidential Elections - Landon vs Roosevelt, Literary Digest conducted a polling survey and predicted with high confidence that Landon is going to win by 57% votes but Roosevelt won by 62%
- Insufficient quantity of training data
- Poor quality data
  - training data is full of outliers, missing data and noise.
- Irrelevant Features
  - garbage in, garbage out
- Overfitting the training data
  - model performs well on training data but does not generalize well
  - Overfitting happens when the model is too complex relative to the amount of data.
  - Simplify the model with fewer number of attributes in the training data or constraining the model
  - Gather more training data
  - Reduce the noise in the training data
- Underfitting the training data
  - model is too simple to learn the underlying structure in data
  - select a more powerful model with more attributes
  - Feeding better features to learning algorithm
  - Reducing the constraints in the model

> Constraining the model to make it simpler and reduce the risk of overfitting is called `regularization`. The amount of regularization to apply during learning can be controlled by `hyperparameter`

## Testing and Validation

How do you know how well a model will generalize to new unseen data?

- Split data into two sets - `training` and `test` datasets
- Train the model on training set and test it using the test set

> The error rate on new cases is called `generalization error`

- If training error is low but the generalization error is high, then model is `overfit`
- `cross validation` is a technique where training set is split into complementary subsets
