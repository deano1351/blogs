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
