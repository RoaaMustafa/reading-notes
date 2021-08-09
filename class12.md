# Pandas in 10
## [Pandas in 10](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)
### Pandas
It is a fast, flexible, and expressive data structures designed to make working with relational or labeled data both easy and intuitive

### importing 
```
import numpy as np

import pandas as pd
```
### Object creation

+ Creating a Series by passing a list of values,
+ Creating a DataFrame by passing a NumPy array, with a datetime index and labeled columns
+ Creating a DataFrame by passing a dict of objects that can be converted to series
+ The columns of the resulting DataFrame have different dtypes
+ 
 ### viewing Data
 + df.head()
 + df.tail(3)  
 + df.index
 +  df.columns
 +  DataFrame.to_numpy() gives a NumPy representation of the underlying data
 +  DataFrame.to_numpy() is fast and doesn’t require copying data.
 +  DataFrame with multiple dtypes, DataFrame.to_numpy() is relatively expensive
 +  describe() shows a quick statistic summary of your data
 + Transposing your data:df.T
 +  Sorting by an axis: df.sort_index(axis=1, ascending=False)

### Getting
+ Selecting a single column, which yields a Series, equivalent to df.A
+ Selecting via [], which slices the rows
#### Selection by label
+ For getting a cross section using a label: `df.loc[dates[0]]`

+  Selecting on a multi-axis by label:`df.loc[:, ["A", "B"]]`
+  Showing label slicing, both endpoints are included: `df.loc["20130102":"20130104", ["A", "B"]]`
+  Reduction in the dimensions of the returned object:`df.loc["20130102", ["A", "B"]]`
+  For getting a scalar value: d`f.loc[dates[0], "A"]`
+  For getting fast access to a scalar (equivalent to the prior method): `df.at[dates[0], "A"]`
### Selection by position
+ Select via the position of the passed integers:`df.iloc[3]`
+ By integer slices, acting similar to NumPy/Python: `df.iloc[3:5, 0:2]`
+ By lists of integer position locations, similar to the NumPy/Python style: `df.iloc[[1, 2, 4], [0, 2]]`
+ For slicing rows explicitly: `df.iloc[1:3, :]`
+ For slicing columns explicitly: `df.iloc[:, 1:3]`
+ For getting a value explicitly: `df.iloc[1, 1]`
+ For getting fast access to a scalar (equivalent to the prior method): `df.iat[1, 1]`
### Boolean indexing
+ Using a single column’s values to select data. :`df[df["A"] > 0]`
+ Selecting values from a DataFrame where a boolean condition is met. `df[df > 0]`
+ Using the isin() method for filtering: `df2[df2["E"].isin(["two", "four"])]`
### Setting
+ Setting a new column automatically aligns the data by the indexes.   `s1 = pd.Series([1, 2, 3, 4, 5, 6], index=pd.date_range("20130102", periods=6))`
+ Setting values by label:

`df.at[dates[0], "A"] = 0`
+ Setting values by position:

`df.iat[0, 1] = 0`
+ Setting by assigning with a NumPy array:
`df.loc[:, "D"] = np.array([5] * len(df))`



## [Pandas - Getting Started](https://pandas.pydata.org/pandas-docs/stable/getting_started/intro_tutorials/index.html)
## [Real Python - Pandas Tutorials](https://realpython.com/learning-paths/pandas-data-science/) 
