## Introduction
In this guide, you will learn how to calculate cell values using various functions in Microsoft Excel 2019. Excel formula allows users to calculate numerous amount of data in a very short time as well as very simplified manner. For an example, what if  a teacher wants to calculate the average mark scored by thousands of students in a subject? Usually it will take him hours to calculate the average through calculator but through excel, a simple drag of cells containing marks and using a simple formula, the work will be done in a very few seconds. Excel formula plays a very important role in the life of students, auditors, business professionals, etc. There are various functions present in the Excel 2019 version to calculate cell values, as mentioned below:

- SUM
- PRODUCT
- AVERAGE
- COUNT & COUNTA
- IF
- MAX & MIN
- TRIM
- DEC2BIN

## SUM Function
The `SUM` function is used to add values. It can be used to add individual values, cell references or ranges or a mix of all three.

The `SUM` function has the following syntax:


```
=SUM( number1, [number2], ... )
```
The arguments used in the function are the numbers that need to be added. As mentioned above, arguments can be individual values, cell references or ranges. To illustrate the same, let's consider the example given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 103 | 53 | 21  | 3423 | =SUM(B1:E1) | ? |
| 2 | 122 | 25 | 51 | 321 | =SUM(B2, C2, D2, E2) | ? |
| 3 | 88 | 50 | 15 | 12 | =SUM(88, 50, 15, 12) | ? |
| 4 | 62 | 57 | 17  | 343 | =SUM(B4, D4) | ? |
| 5 | 15  | 51 | 11 | 87 | =SUM(B2:E2, B5:E5) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 103 | 53 | 21  | 3423 | =SUM(B1:E1) | 3600 |
| 2 | 122 | 25 | 51 | 321 | =SUM(B2, C2, D2, E2) | 519 |
| 3 | 88 | 50 | 15 | 12 | =SUM(88, 50, 15, 12) | 165 |
| 4 | 62 | 57 | 17  | 343 | =SUM(B4, D4) | 79 |
| 5 | 15  | 51 | 11 | 87 | =SUM(B2:E2, B5:E5) | 683 |

## PRODUCT Function
The `PRODUCT` function multiplies all the numbers given as arguments and returns the product.

The `PRODUCT` function has the following syntax:


```
=PRODUCT(number1, [number2], ...)
```

The arguments used in the function are the numbers that need to be multiplied. The `PRODUCT` function is useful when you need to multiply many cells together. To illustrate the same, let's consider the example given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =PRODUCT(B1:E1) | ? |
| 2 | 22 | 2 | 5 | 31 | =PRODUCT(B2:E2, 3) | ? |
| 3 | 8 | 50 | 5 | 2 | =8 * 50 * 5 * 2 | ? |
| 4 | 6 | 7 | 17  | 3 | =PRODUCT(C4, E4) | ? |
| 5 | 15  | 5 | 11 | 8 | =PRODUCT(B2:E2, B5:E5) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =PRODUCT(B1:E1) | 2457 |
| 2 | 22 | 2 | 5 | 31 | =PRODUCT(B2:E2, 3) | 20460 |
| 3 | 8 | 50 | 5 | 2 | =8 * 50 * 5 * 2 | 4000 |
| 4 | 6 | 7 | 17  | 3 | =PRODUCT(C4, E4) | 21 |
| 5 | 15  | 5 | 11 | 8 | =PRODUCT(B2:E2, B5:E5) | 45012000 |

## AVERAGE Function
The `AVERAGE` function returns the average (arithmetic mean) of the arguments.

The `AVERAGE` function has the following syntax:


```
=AVERAGE(number1, [number2], ...)
```

Arguments present in the function can either be numbers or names, ranges, or cell references that contain numbers. To illustrate the same, let's consider the example given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =AVERAGE(B1:E1) | ? |
| 2 | 22 | 2 | 5 | 31 | =AVERAGE(B2:E2, 3) | ? |
| 3 | 6 | 7 | 17  | 3 | =PRODUCT(C3:E3) | ? |
| 4 | 15  | 5 | 11 | 8 | =PRODUCT(B2:B4) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =AVERAGE(B1:E1) | 10 |
| 2 | 22 | 2 | 5 | 31 | =AVERAGE(B2:E2, 3) | 12.6 |
| 3 | 6 | 7 | 17  | 3 | =PRODUCT(C3:E3) | 9 |
| 4 | 15  | 5 | 11 | 8 | =PRODUCT(B2:B4) | 14 |

## COUNT & COUNTA Function
The `COUNT` function is used to get the number of entries in a number field that is in a range or array of numbers whereas the `COUNTA` function counts the number of cells that are not empty in a range.

The `COUNT` function has the following syntax:


```
=COUNT(value1, [value2], ...)
```

The `COUNTA` function has the following syntax:


```
=COUNTA(value1, [value2], ...)
```

Let's consider the example given below to understand the use of `COUNT` and `COUNTA` function better:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =COUNT(B1:E1) | ? |
| 2 | 22 | 2 | 5 | 31 | =COUNTA(B2:E2) | ? |
| 3 | 6 | 7 |  | NAME | =COUNT(B3:E3) | ? |
| 4 |  TOM | 5 | 11 |  | =PRODUCT(B4:E4) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =COUNT(B1:E1) | 4 |
| 2 | 22 | 2 | 5 | 31 | =COUNTA(B2:E2) | 4 |
| 3 | 6 | 7 |  | NAME | =COUNT(B3:E3) | 2 |
| 4 |  TOM | 5 | 11 |  | =COUNTA(B4:E4) | 3 |

## IF Function
The `IF` function allows you to make a logical comparison between a value and what you expect by testing for a condition and returning a result if that condition is TRUE or FALSE.

The `IF` function has the following syntax:


```
=IF(logical_test, [value_if_true], [value_if_false])
```

**logical_test** argument used in the function is any value or expression that can be evaluated to TRUE or FALSE. Let's consider the example given below to understand this function:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =IF(B1 > D1, C1, FALSE)| ? |
| 2 | 22 | 2 | 5 | 31 | =IF(NOT(B2 = E2), TRUE, FALSE) | ? |
| 3 | 8 | 50 | 5 | 2 | =IF(B3 > 20, C1, D1) | ? |
| 4 | 6 | 7 | 17  | 3 | =IF(C4 = E4, TRUE, FALSE) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =IF(B1 > D1, C1, FALSE)| FALSE |
| 2 | 22 | 2 | 5 | 31 | =IF(NOT(B2 = E2), TRUE, FALSE) | TRUE |
| 3 | 8 | 50 | 5 | 2 | =IF(B3 > 20, C1, D1) | 5 |
| 4 | 6 | 7 | 17  | 3 | =IF(C4 = E4, TRUE, FALSE) | FALSE |

## MAX & MIN Function
The `MAX` function is used to return the largest value in a set of values whereas the `MIN` function returns the smallest number in a set of values.

The `MAX` function has the following syntax:


```
=MAX(number1, [number2], ...)
```

The `MIN` function has the following syntax:


```
=MIN(number1, [number2], ...)
```
Let's consider the example given below to understand the use of both of the functions:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =MAX(B1:E1) | ? |
| 2 | 22 | 2 | 5 | 31 | =MIN(B1:B4) | ? |
| 3 | 6 | 7 | 17  | 3 | =MAX(B1:E4) | ? |
| 4 | 15  | 5 | 11 | 8 | =MIN(B1:E4) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =MAX(B1:E1) | 21 |
| 2 | 22 | 2 | 5 | 31 | =MIN(B1:B4) | 6 |
| 3 | 6 | 7 | 17  | 3 | =MAX(B1:E4) | 31 |
| 4 | 15  | 5 | 11 | 8 | =MIN(B1:E4) | 2 |

## TRIM Function
The `TRIM` function removes all spaces from text except for single spaces between words.

The `TRIM` function has the following syntax:


```
=TRIM(text)
```

`TRIM` function can be used on text that you have received from another application that may have irregular spacing. Let's consider the example given below to understand the functionality better:

|    A    |  B   |  C   |  D  |
| --- | --- | --- | --- |
| **Sr. Number** | **TEXT** | **FORMULA** | **RESULT** |
| 1 |   APPLE | =TRIM("   APPLE  ") | ?|
| 2 | I   AM     A   DOCTOR  | =TRIM("  I   AM     A   DOCTOR ") | ? |
| 3 | GRADES | =TRIM("GRADES") | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |
| --- | --- | --- | --- |
| **Sr. Number** | **TEXT** | **FORMULA** | **RESULT** |
| 1 |   APPLE | =TRIM("   APPLE  ") | "APPLE" |
| 2 | I   AM     A   DOCTOR  | =TRIM("  I   AM     A   DOCTOR ") | "I AM A DOCTOR" |
| 3 | GRADES | =TRIM("GRADES") | "GRADES" |

## DEC2BIN Function
The `DEC2BIN` function is used to convert a decimal number to binary.

The `DEC2BIN` function has the following syntax:


```
=DEC2BIN(number, [places])
```
We can convert **Decimal** Number To **Binary/ Octal/ Hex** With Formulas or vice versa with slight modification in the formula. Let's consider an example below to illustrate the same:

|    A    |  B   |  C   |  D  | E |
| --- | --- | --- | --- | --- |
| **Sr. Number** | **DECIMAL** | **BINARY** | **HEX** | **OCTAL** |
| 1 | 4 | =DEC2BIN(B1) | =DEC2HEX(B1) | =DEC2OCT(B1) |
| 2 | 120 | =DEC2BIN(B2) | =DEC2HEX(B2) | =DEC2OCT(B2) |
| 2 | 356 | =DEC2BIN(B3) | =DEC2HEX(B3) | =DEC2OCT(B3) |

After applying the formula, the result will be updated as shown below:

|    A    |  B   |  C   |  D  | E |
| --- | --- | --- | --- | --- |
| **Sr. Number** | **DECIMAL** | **BINARY** | **HEX** | **OCTAL** |
| 1 | 4 | 100 | 4 | 4 |
| 2 | 120 | 1111000 | 170 | 78 |
| 2 | 356 | 101100100 | 544 | 164 |

Similarly, we can now convert **Binary** to **Decimal/ Octal/ Hex**, **Hex** to **Decimal/ Octal/ Binary** and **Octal** to **Decimal/ Binary/ Hex**.

### Binary to Decimal/ Octal/ Hex
You can use the syntax mentioned below for the conversion:

Syntax for **Binary** to **Decimal**:


```
=BIN2DEC(number, [places])
```

Syntax for **Binary** to **Octal**:


```
=BIN2OCT(number, [places])
```

Syntax for **Binary** to **Hex**:


```
=BIN2HEX(number, [places])
```

### Hex to Decimal/ Octal/ Binary
You can use the syntax mentioned below for the conversion:

Syntax for **Hex** to **Decimal**:


```
=HEX2DEC(number, [places])
```

Syntax for **Hex** to **Octal**:


```
=HEX2OCT(number, [places])
```

Syntax for **Hex** to **Binary**:


```
=HEX2BIN(number, [places])
```

### Octal to Decimal/ Binary/ Hex
You can use the syntax mentioned below for the conversion:

Syntax for **Octal** to **Decimal**:


```
=OCT2DEC(number, [places])
```

Syntax for **Octal** to **Binary**:


```
=OCT2BIN(number, [places])
```

Syntax for **Octal** to **Hex**:


```
=OCT2HEX(number, [places])
```

## Conclusion
So far in this guide, you have learnt few of the formulas that help you to calculate cell values but there are hundreds of more excel formulas that you can explore in the excel and make your work a lot easier.
You may also like to learn the below Excel topics:
- [Working with Time and Date Functions in Excel - Part 1](/guides/working-with-time-date-functions-excel-part-1)
- [Working with Time and Date Functions in Excel - Part 2](/guides/working-with-time-date-functions-excel-part-2)
- [Excel Logic Function Playbook](/guides/working-with-logical-functions-in-excel)
- [Working with Finance Function in Excel](/guides/working-finance-function-excel)
- [Working with Statistics Function in Excel](/guides/working-statistics-function-excel)
- [Formatting Excel Worksheets and Cells](/guides/formatting-excel-worksheets-cells)
- [Working with Lookup Functions in Excel](/guides/working-with-lookup-functions-excel)
