# Azure Data Factory Data Flow Transformations

## Window Aggregations

The Window transformation is where you will define window-based aggregations of columns in your data streams. In the Expression Builder, you can define different types of aggregations that are based on data or time windows (aka SQL OVER clause) such as LEAD, LAG, NTILE, CUMEDIST, RANK, etc ...) and create a new field in your output that includes these aggregations with optional group-by fields.

![Window Transformation](../images/windows1.png "windows 1")

### Over
This where you will set the partitioning of column data for your window transformation. This is equivalent to the Partition By in the Over clause in SQL. If you wish to create a calculation or create an expression to use for the partitioning, you can do that by hovering over the column name and select "computed column".

<img src="../images/windows4.png" width="400">

### Sort
Also part of the Over clause is setting the Order By, or sort order. As is the case with the "Over" column selector, you can also create an expression for a calculate value in this column field for sorting.

<img src="../images/windows5.png" width="400">

### Range By
Next, set the window frame as Unbounded or Bounded. To set an unbounded window frame, set the slider to Unbounded on both ends. If you choose a setting between Unbounded and Current Row, then you must set the Offset start and end values. Both values will be positive integers. You can use either relative numbers or values from your data.

The window slider has 2 values to set: the values before the current row and the values after the current row. The Start and End offset matches the 2 selectors on the slider.

<img src="../images/windows6.png" width="400">

### Window Columns
Lastly, use the Expression Builder to define the aggregations you wish to use with the data windows such as RANK, COUNT, MIN, MAX, DENSE RANK, LEAD, LAG, etc.

<img src="../images/windows2.png" width="600">

The full list of aggregation and analytical functions available for you to use in the ADF Data Flow Expression Language via the Expression Builder are listed here: https://aka.ms/dataflowexpressions.

