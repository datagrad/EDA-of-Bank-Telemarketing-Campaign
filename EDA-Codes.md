# Import all the libraries required for the Case Study

```

import pandas as pd
import numpy as np
import random
import matplotlib.pyplot as plt
import seaborn as sns
```


# Extend the view for the number of columns and rows 

```
pd.set_option('display.max_columns', 200)
pd.set_option('display.max_rows', 500)
```
# Read and display the data

```
df = pd.read_csv("application_data.csv")
df.head()
```

# Size of Dataframe
```
df.size
```

# Number of rows and columns in Application data
```
df.shape
```

# Concise summary of a DataFrame
```
df.info(verbose = True)
```

# Missing Values count

```
df.isnull().sum()
```

# Percentage of missing Values
```
k = 100*(df.isnull().sum())/307511
k.sort_values(ascending=False)
```

# Selection of Attributes (Columns from dataframe) 

```
df = df[['clm1', 'clm2', 'clm3', 'clm4']]
df
```


# Describe for Numerical (Mean, Std, min, max, count)

```
df.describe()
```

```
df.info()
```

# Percentage of missing Values

```
m = 100*(df.isnull().sum())/307511
m.sort_values(ascending=False)
```

# Changing data type

```
convert_dict = {'SK_ID_CURR': object, 'TARGET': object, 'AMT_INCOME_TOTAL': int, 'FLAG_MOBIL' : object, 'FLAG_EMP_PHONE' : object, 'FLAG_CONT_MOBILE' : object}   
df = df.astype(convert_dict)
```


# Check datatype

```
df.info()
```

```
df.NAME_TYPE_SUITE.describe()
```

# Replacing NaN values with unaccompanied

```
df["NAME_TYPE_SUITE"].fillna("Unaccompanied", inplace = True)
df.AMT_REQ_CREDIT_BUREAU_QRT.describe()
```

# Replacing NaN values with 0
```
df["AMT_REQ_CREDIT_BUREAU_QRT"].fillna(0, inplace = True)
df.AMT_GOODS_PRICE.describe()
```

# Replacing NaN values with 0
```
df['AMT_GOODS_PRICE'].fillna(0, inplace = True)
df.DEF_60_CNT_SOCIAL_CIRCLE.describe()
```

# Find median

```
df.DEF_60_CNT_SOCIAL_CIRCLE.median()
```

# Replacing NaN values with median ie 0
```
df['DEF_60_CNT_SOCIAL_CIRCLE'].fillna(0, inplace = True)
```


# Replacing NaN values with median ie 2
```
df['CNT_FAM_MEMBERS'].fillna(2, inplace = True)
```

# Changing data type for few attributes
convert_dict = {'AMT_GOODS_PRICE': int, 'AMT_REQ_CREDIT_BUREAU_QRT': int, 'DEF_60_CNT_SOCIAL_CIRCLE': int, 'CNT_FAM_MEMBERS' : int}   
df = df.astype(convert_dict)

# Changing the float variable with 2 decimal points

```
df.REGION_POPULATION_RELATIVE = df.REGION_POPULATION_RELATIVE.round(2)
df.AMT_CREDIT = df.AMT_CREDIT.round(2)
```

# Absolute Values

```
df.DAYS_BIRTH = df.DAYS_BIRTH.abs()

df.DAYS_EMPLOYED = df.DAYS_EMPLOYED.abs()

df.DAYS_ID_PUBLISH = df.DAYS_ID_PUBLISH.abs()
```


# Binning for AMT_GOODS_PRICE
```

df['AMT_GOODS_PRICE_b'] = pd.cut(df.AMT_GOODS_PRICE, [0, 200000, 400000, 600000, 800000, 4100000], labels = ['low', 'below_avg', 'avg', 'above_avg', 'high'])
```


# Binning for AMT_GOODS_PRICE
df['AMT_CREDIT_b'] = pd.cut(df.AMT_GOODS_PRICE, [40000, 200000, 400000, 600000, 800000, 4100000], labels = ['low', 'below_avg', 'avg', 'above_avg', 'high'])

df['AMT_INCOME_TOTAL'].describe()
