# Pandas
Pandas is a fast, powerful and easy data analysis and manipulating tool

`import pandas as pd`

[why to use pandas](https://realpython.com/lessons/pandas-dataframe-overview/)

## Object creation
### series
a serie is one dimensionsl array that holds any data type.
to create a series using pandas:

` s = pd.Series(data, index=index)`

- data could be anything.
- index will start from zero if not provided.
- series can be instantiated from dictionaries:

```
d = {"b": 1, "a": 0, "c": 2}`
pd.Series(d)
```

- if we rearranged the index:
```
pd.Series(d, index=["b", "c", "d", "a"])
output:
b    1.0
c    2.0
d    NaN
a    0.0
```
[More on series](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html)

## DataFrame
The main data structure of pandas.
- Creating a DataFrame by passing a NumPy array
[DataFrames](https://realpython.com/lessons/introduction-pandas-dataframe/)
```
dates = pd.date_range("20220101", periods=6)
df = pd.DataFrame(np.random.rand(6 ,4), index = dates, columns=list("ABCD"))
df
```
output --> 
```
                   A         B         C         D
2013-01-01  0.469112 -0.282863 -1.509059 -1.135632
2013-01-02  1.212112 -0.173215  0.119209 -1.044236
2013-01-03 -0.861849 -2.104569 -0.494929  1.071804
2013-01-04  0.721555 -0.706771 -1.039575  0.271860
2013-01-05 -0.424972  0.567020  0.276232 -1.087401
2013-01-06 -0.673690  0.113648 -1.478427  0.524988
```
- Creating a DataFrame by passing a dictionary of objects
```
df2 = pd.DataFrame(
    {
        "A": 1.0,
        "B": pd.Timestamp("20130102"),
        "C": pd.Series(1, index=list(range(4)), dtype="float32"),
        "D": np.array([3] * 4, dtype="int32"),
        "E": pd.Categorical(["test", "train", "test", "train"]),
        "F": "foo",
    }
)

```
output --->
```
     A          B    C  D      E    F
0  1.0 2013-01-02  1.0  3   test  foo
1  1.0 2013-01-02  1.0  3  train  foo
2  1.0 2013-01-02  1.0  3   test  foo
3  1.0 2013-01-02  1.0  3  train  foo
```

## Viewing data
To view the top and bottom rows of the frame:
- pd.head()  --> prints the first 5 rows
- pd.tail() --> prints the last 5 rows.
- pd.tail(3) --> will show last 3 rows in the frame 

Gives a NumPy representation of the underlying data:
- DataFrame.to_numpy() -->  fast and doesn’t require copying data.
>> NumPy arrays have one dtype for the entire array, while pandas DataFrames have one dtype per column.
pandas will find the NumPy dtype that can hold all of the dtypes in the DataFrame. This may end up being object, which requires casting every value to a Python object.

## Selection
### Getting
- df["A"]
- df[0:3]
- df["20130102":"20130104"]

>>> .loc is strict when you present slicers that are not compatible (or convertible) with the index type.

### Selection by label
- df.loc[dates[0]] --> For getting a cross section using a label
- df.loc[:, ["A", "B"]] --> Selecting on a multi-axis by label
- df.loc["20130102":"20130104", ["A", "B"]] --> Showing label slicing, both endpoints are included
- df.loc["20130102", ["A", "B"]] --> Reduction in the dimensions of the returned object
- df.loc[dates[0], "A"] --> For getting a scalar value
- df.at[dates[0], "A"] --> For getting fast access to a scala


### Selection by position
- df.iloc[3] --> Select via the position of the passed integers
- df.iloc[3:5, 0:2] --> by integer slicing
- df.iloc[[1, 2, 4], [0, 2]] --> By lists of integer position locations
- df.iloc[1:3, :] --> For slicing rows explicitly
- df.iloc[:, 1:3] --> For slicing columns explicitly
- df.iloc[1, 1] --> For getting a value explicitly
- df.iat[1, 1] --> For getting fast access to a scalar


### Boolean indexing
- df[df["A"] > 0]
- df[df > 0]

### Setting
Setting a new column automatically aligns the data by the indexes
- df["F"] = s1
- df.at[dates[0], "A"]
- df.iat[0, 1]

## Missing data
pandas primarily uses the value np.nan to represent missing data.
- Reindexing allows you to change/add/delete the index on a specified axis. This returns a copy of the data:
```
df1 = df.reindex(index=dates[0:4], columns=list(df.columns) + ["E"])
df1.loc[dates[0] : dates[1], "E"] = 1
```

- To drop any rows that have missing data:

 df1.dropna(how="any")

- Filling missing data:

df1.fillna(value=5)
 
- To get the boolean mask where values are nan:

pd.isna(df1)

## Operations
### Stats
Operations in general exclude missing data.

Performing a descriptive statistic:

```
df.mean()
 
A   -0.004474
B   -0.383981
C   -0.687758
D    5.000000
F    3.000000
```

more pandas operations: [link](https://pandas.pydata.org/pandas-docs/stable/user_guide/10min.html#selection-by-label)


[Panda python](https://www.youtube.com/watch?v=dcqPhpY7tWk&t=391s&ab_channel=PythonProgrammer)

