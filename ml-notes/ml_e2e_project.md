## ML End to End Project <a name="home"></a>

### Steps

1. [Frame the Problem](#frame-the-problem)
2. [Get the data](#get-data)

#### Frame the Problem <a name="frame-the-problem"></a>

1. What is the business objective? (Why? because building the machine learning model is not the end goal)
2. How does the company expect to use and benefit from the model?
3. What algorithms to select?
4. What performance measure to use to evaluate the model?
5. How much effort to spent on tweaking it?
6. What does the current solution look like?
7. Is it supervise, unsupervised or reinforcement learning?
8. Is it a regression, classification or something else?
9. Select a performance measure. Ex:- Regression Tasks - RMSE, MAE (if outliers exist)
10. Verify the assumptions

[home](#home)

#### Get the data <a name="get-data"></a>

1. Use [pandas]() to read to a dataframe

```
import pandas as pd

df = pandas.read_csv("")
```

2. Split the data into train and test

```
from sklearn.model_selection import train_test_split
train_set, test_set = train_test_split(df,
                                       test_size=0.2,
                                       random_state=42)
```

> Random Sampling can introduce sampling bias. Important to maintain stratified sampling
> Dividing the population into homogenous subgroups called stratified sampling, the right number of instances is sampled from each stratum to guarantee test set is representative of the overall population

```
from sklearn.model_selection import StratifiedShuffleSplit

```

3. Look for correlations among target vs features
4. Use pandas scatter_matrix to find corelations

```
from pandas.plotting import scatter_matrix
```

5. Handle missing data

```
df.dropna(['col1']) # drop rows that have na for col1

df.drop('col1', axis=1) # drop the whole column

df['col1'].fillna(median_val, inplace=True) # use median of values to fill missing values

from sklearn.impute import SimpleImputer

imputer = SimpleImputer(strategy = 'median')
imputer.fit(col1_num)
```

6. Handle Categorical data

```
from sklearn.preprocessing import OrdinalEncoder
ordinal_encoder = OrdinalEncoder()
col1_encoded = ordinal_encoder.fit_transform(col1)

from sklearn.preprocessing import OneHotEncoder

```

7. Feature Scaling - Get all attribtes to the same scale. Ex:- min-max scaling and standardization

> min-max scaling is called `normalization`
