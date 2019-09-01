## Introduction
In this guide, you will learn how to work with lookup functions in Microsoft Excel 2019. There are various lookup functions which are present in the Excel 2019 version, as mentioned below:

- ADDRESS function 
- AREAS function
- UNIQUE Function
- CHOOSE function
- COLUMN function
- COLUMNS function
- FILTER function
- FORMULATEXT function 
- GETPIVOTDATA function
- HLOOKUP function 
- HYPERLINK function
- INDEX function
- INDIRECT function
- LOOKUP function
- MATCH function
- OFFSET function
- ROW function
- ROWS function
- VLOOKUP Function
- TRANSPOSE function 
- SORT function
- SORTBY function
- RTD function
 
## ADDRESS Function
The `ADDRESS` function gives us the address  for a cell based on  the given  row and column number.

The `ADDRESS` function has the following syntax:


```
=ADDRESS(row_num, column_num, [abs_num], [a1], [sheet_text])
```

The arguments used in this function are mentioned below:


- row_num = `Required`, it is a  numeric value that specifies the row number to be used in the cell reference.
- column_num = `Required`, it is a  numeric value that specifies the column number to use in the cell reference.
- abs_num = `Optional`, it is a numeric value that specifies the type of reference to return.
| --- | --- |
| **abs_num** | **Returns type of reference** |
| 1 or omitted | Absolute |
| 2 | Absolute row; relative column |
| 3 | Relative row; absolute column |
| 4 | Relative |


