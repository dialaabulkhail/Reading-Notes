# Pandas
`import pandas as pd`

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

### DataFrame
![]()

