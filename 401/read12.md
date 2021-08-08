# Read 12: Pandas in 10

## Pandas:

- A python package used for data manipulation and analysis.

### Pandas using in:
### Object creation
- Series by passing a list of values, letting pandas create a default integer index.
```
s = pd.Series([1, 3, 5, np.nan, 6, 8])
```

- DataFrame by passing a NumPy array, with a datetime index and labeled columns.
```
df = pd.DataFrame(np.random.randn(6, 4), index=dates, columns=list("ABCD"))
```

### Viewing data

- df.head() -->  top rows of the frame
- df.tail(3) --> bottom rows of the frame
- df.index --> display the index
- df.columns --> display coloumns.
- df.to_numpy() --> datatype to float 
- describe() --> shows a quick statistic summary of your data
### Selection
- Getting (df["A"]) --> Selecting a single column
- Selecting via [], which slices the rows.
- Selection by label (df.loc[:, ["A", "B"]])
- Selection by position --> Select via the position of the passed integers or lists
- Boolean indexing --> Using a single column’s values to select data.
- Using the isin() method for filtering:
- Setting --> Setting a new column automatically aligns the data by the indexes. by label, by position, by assigning with a NumPy array.

### Missing data
pandas primarily uses the value np.nan to represent missing data (NaN)

### Operations
- Stats
- Apply
- Histogramming
- string methods.

### Merging
- Concat
- Join

### Grouping
Steps: 
1. Splitting the data into groups based on some criteria
2. Applying a function to each group independently
3. Combining the results into a data structure

### Reshaping
- Stack
- Pivot Tables

Time series, Categoricals, Plotting and Getting data in/out.