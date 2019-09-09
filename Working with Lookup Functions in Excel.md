## Introduction
In this guide, you will learn how to work with lookup functions in Microsoft Excel 2019. There are various lookup functions which are present in the Excel 2019 version, as mentioned below:

- ADDRESS Function 
- AREAS Function
- UNIQUE Function
- CHOOSE Function
- COLUMN Function
- COLUMNS Function
- FILTER Function
- FORMULATEXT Function 
- GETPIVOTDATA Function
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
 
 ## LOOKUP Functions
In this section, you will learn about each of these lookup functions through various scenarios.

### ADDRESS Function
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

Let us consider a scenario where you can learn how to implement the `ADDRESS` function in Excel. Consider the example given below.

| A | B| C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Sr. No.** | **Row_Num** | **Column_Num** | **Abs_Num** | **A1** | **Sheet_text** | **Address Formula** | **Result** |
| 1 | 1 | 4 |  |  |  | =ADDRESS(B1, C1) |  ? |
| 2 | 3 | 5 | 1 |  |  | =ADDRESS(B2,C2,D2) | ? |
| 3 | 2 | 1 | 2 | 1 |  | =ADDRESS(B3, C3, D3, E3) | ? |
| 4 | 7 | 11 | 3 | 0 | sheet1 | =ADDRESS(B4, C4, D4, E4, F4) | ? |
| 5 | 18 | 12 | 4 | 1 |  | =ADDRESS(B5, C5, D5, E5) | ? |

The result will be updated as shown below:

| A | B| C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Sr. No.** | **Row_Num** | **Column_Num** | **Abs_Num** | **A1** | **Sheet_text** | **Address Formula** | **Result** |
| 1 | 1 | 4 |  |  |  | =ADDRESS(B1, C1) |  $D$1 |
| 2 | 3 | 5 | 1 |  |  | =ADDRESS(B2,C2,D2) |  $E$3 |
| 3 | 2 | 1 | 2 | 1 |  | =ADDRESS(B3, C3, D3, E3) |  A$2 |
| 4 | 7 | 11 | 3 | 0 | sheet1 | =ADDRESS(B4, C4, D4, E4, F4) | sheet1!R[7]C11 |
| 5 | 18 | 12 | 4 | 1 |  | =ADDRESS(B5, C5, D5, E5) | L18 |

### AREAS Function
It gives the number of areas in a given reference where an area is a range of contiguous cells or a single cell.

The `AREAS` function has the following syntax:


```
=AREAS(reference)
```

The argument used in this function is mentioned below:

- reference =  `Required`, it is a reference to a cell or range of cells and refer to multiple areas. In case, you want to specify a single argument for multiple references, then you must include extra sets of parentheses. In that way the comma will not be interpreted  as a field separator by the Microsoft Excel.

Let us consider a scenario where you can learn how to implement the `AREAS` function in Excel. Consider the example given below.

| A | B| C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Sr. No.** | **Row_Num** | **Column_Num** | **Abs_Num** | **A1** | **Sheet_text** | **AREA Formula** | **Result** |
| 1 | 1 | 4 |  |  |  | =AREAS(B1:C1) |  ? |
| 2 | 3 | 5 | 1 |  |  | =AREAS(B2:C2, D2) | ? |
| 3 | 2 | 1 | 2 | 1 |  | =AREAS(B3:E3) | ? |
| 4 | 7 | 11 | 3 | 0 | sheet1 | =AREAS(B4:D4, E4, F4) | ? |
| 5 | 18 | 12 | 4 | 1 |  | =AREAS(B5:C5 B5) | ? |

The result will be updated as shown below:

| A | B| C | D | E | F | G | H |
| --- | --- | --- | --- | --- | --- | --- | --- |
| **Sr. No.** | **Row_Num** | **Column_Num** | **Abs_Num** | **A1** | **Sheet_text** | **AREA Formula** | **Result** |
| 1 | 1 | 4 |  |  |  | =AREAS(B1:C1) |  1 |
| 2 | 3 | 5 | 1 |  |  | =AREAS(B2:C2, D2) | 2 |
| 3 | 2 | 1 | 2 | 1 |  | =AREAS(B3:E3) | 1 |
| 4 | 7 | 11 | 3 | 0 | sheet1 | =AREAS(B4:D4, E4, F4) | 3 |
| 5 | 18 | 12 | 4 | 1 |  | =AREAS(B5:C5 B5) | 1 |

### UNIQUE Function
The `UNIQUE` function returns unique values from a list of values.

The `UNIQUE` function has the following syntax:


```
=UNIQUE(range)
```

Let us consider a scenario where you can learn how to implement the `UNIQUE` function in Excel. Consider the example given below where you have few values given in different rows:

| A | B | C |
| --- | --- | --- |
| **SR. NO.** | **VALUE** | **UNIQUE VALUES** |
| 1 | 15 |  |
| 2 | 18 |  |
| 3 | 15 |  |
| 4 | 16 |  |
| 5 | 18 |  |

Now you can apply `=UNIQUE(B1:B5)` function to get the unique values from the given list of values and the output will be as shown below:

| A | B | C |
| --- | --- | --- |
| **SR. NO.** | **VALUE** | **UNIQUE VALUES** |
| 1 | 15 | 15 |
| 2 | 18 | 16 |
| 3 | 15 | 18 |
| 4 | 16 |  |
| 5 | 18 |  |

### CHOOSE Function
`CHOOSE` function uses index_num to return a value from the list of value arguments. 

The `CHOOSE` function has the following syntax:


```
=CHOOSE(index_num, value1, [value2], ...)
```

The arguments used in this function are mentioned below:

- index_num =  `Required`, it specifies the selected value argument. This argument must be a number that lies between 1 and 254, or a formula or reference to a cell containing a number between 1 and 254.

- Value1, value2, ... = Value1 is a `Required` argument whereas subsequent values are `Optional` argument.     

Let us consider a scenario where you can learn how to implement the `CHOOSE` function in Excel. Consider the example given below.

| A | B | C |
| --- | --- | --- |
| **SR. NO.** | **Function** | **Output** |
| 1 | =CHOOSE(4,"Monday", "Tuesday", "Wednesday", "Thursday", "Friday") | Thursday |
| 2 | =CHOOSE(2, 2, "Cat", 23, 321, "ABC") | Cat |
| 3 | =CHOOSE(1,34,323,3221,1221) | 34 |

