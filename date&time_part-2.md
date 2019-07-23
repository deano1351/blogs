## Introduction
In this guide, you will learn how to work with rest of the time and date functions in Microsoft Excel 2019 that were left in the first part of the guide. There are various time and date functions which are present in the Excel 2019 version, as mentioned below:

- NETWORKDAYS
- NETWORKDAYS.INTL
- NOW
- SECOND
- TIME
- TIMEVALUE
- TODAY
- WEEKDAY
- WEEKNUM
- WORKDAY
- WORKDAY.INTL
- YEAR
- YEARFRAC
 
## Time and Date Functions
In this section, you will learn about each of these time and date functions through various scenarios.

### The NETWORKDAYS Function
The `NETWORKDAYS` function gives the total number of workdays if you provide a start date and an end date. It excludes the weekends and dates that were identified as holidays while returning the ouput.

The `NETWORKDAYS` function has the following syntax:


```
=NETWORKDAYS(start_date, end_date, [holidays])
```

The arguments `start_date` and `end_date` are **required** arguments in the function. These two arguments reprsent the start date and the end date. The third argument in the function is optional. It can be a range of cells containing dates in `DATE` format or an array constant of the serial numbers as the dates in `DATE` format.

Let us consider a scenario where you can learn how to implement the `NETWORKDAYS` function in Excel. Consider the example given below:

| A | B | C | D | E |
| --- | --- | --- | --- | --- |
| **Sr. No.** | **Start_Date** | **End_Date** | **Holiday** | **WorkDays** |
| 1 | 23-Jul-19 | 30-Jul-19 |   | =NETWORKDAYS(B1,C1) |
| 2 | 01-Jan-19 | 31-Jan-2019 | 26-Jan-2019 | =NETWORKDAYS(B2,C2,D2) |
| 3 | 24-Jul-19 | 23-Aug-2019 | 15-Aug-2019 | =NETWORKDAYS(B3,C3,D3) |

The result will be updated as shown below:

| A | B | C | D | E |
| --- | --- | --- | --- | --- |
| **Sr. No.** | **Start_Date** | **End_Date** | **Holiday** | **WorkDays** |
| 1 | 23-Jul-19 | 30-Jul-19 |   | 6 |
| 2 | 01-Jan-19 | 31-Jan-2019 | 26-Jan-2019 | 23 |
| 3 | 24-Jul-19 | 23-Aug-2019 | 15-Aug-2019 | 22 |

