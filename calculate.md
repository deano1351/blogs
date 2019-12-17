## Introduction
n this guide, you will learn to calculate cell values using various functions in Microsoft Excel 2019. There are various functions present in the Excel 2019 version to calculate cell values, as mentioned below:

- SUM
- PRODUCT
- AVERAGE


## SUM Function
The `SUM` function is used to add values. It can be used to add individual values, cell references or ranges or a mix of all three.

The `SUM` function has the following syntax:


```
=SUM(number1,[number2],...)
```
The arguments used in the function are the numbers that need to be added. As mentioned above, arguments can be individual values, cell references or ranges. To illustrate the same, let's consider the example given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 103 | 53 | 21  | 3423 | =SUM(B1:E1) | ? |
| 2 | 122 | 25 | 51 | 321 | =SUM(B2, C2, D2, E2) | ? |
| 3 | 88 | 50 | 15 | 12 | =SUM(88, 50, 15, 12) | ? |
| 4 | 62 | 57 | 17  | 343 | =SUM(B4, D4) | ? |
| 5 | 15  | 51 | 11 | 87 | =SUM(B2:E2,B5:E5) | ? |

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

The arguments used in the function are the numbers that need to be multiplied. The `PRODUCT` function is useful when you need to multiply many cells together. To illustrate the same, let's consider the exmaple given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =PRODUCT(B1:E1) | ? |
| 2 | 22 | 2 | 5 | 31 | =PRODUCT(B2:E2,3) | ? |
| 3 | 8 | 50 | 5 | 2 | =8 * 50 * 5 * 2 | ? |
| 4 | 6 | 7 | 17  | 3 | =PRODUCT(C4,E4) | ? |
| 5 | 15  | 5 | 11 | 8 | =PRODUCT(B2:E2,B5:E5) | ? |

The result column will be updated as given below:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **Sr. Number** | **Value1** | **Value2** | **Value3** | **Value4** | **Formula** | **Result** |
| 1 | 13 | 3 | 21  | 3 | =PRODUCT(B1:E1) | 2457 |
| 2 | 22 | 2 | 5 | 31 | =PRODUCT(B2:E2,3) | 20460 |
| 3 | 8 | 50 | 5 | 2 | =8 * 50 * 5 * 2 | 4000 |
| 4 | 6 | 7 | 17  | 3 | =PRODUCT(C4,E4) | 21 |
| 5 | 15  | 5 | 11 | 8 | =PRODUCT(B2:E2,B5:E5) | 45012000 |
