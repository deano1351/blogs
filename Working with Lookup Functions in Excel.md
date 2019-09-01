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
- abs_num = `Optional`, it is a numeric value that specifies the type of reference to return as mentioned in the table below:

| A | B |
| --- | --- |
| **abs_num** | **Returns type of reference** |
| 1 or omitted | Absolute |
| 2 | Absolute row; relative column |
| 3 | Relative row; absolute column |
| 4 | Relative |

- A1 = `Optional`, it is a logical value that specifies the A1 or R1C1 reference style. A1 style means, columns are labeled alphabetically, and rows are labeled numerically whereas R1C1 reference style means, both columns and rows are labeled numerically. If the A1 argument value is TRUE or omitted in the function, the `ADDRESS` function will return an A1-style reference; if the A1 argument value is FALSE, the ADDRESS function will return an R1C1-style reference.
- sheet_text =  `Optional`, it is a text value that specifies the name of the worksheet to be used as the external reference. If the sheet_text argument value is omitted, no sheet name will be used, and the address returned by the function refers to a cell on the current sheet.


