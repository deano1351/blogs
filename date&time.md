## Introduction
In this guide, you will learn how to work with time and date functions in Microsoft Excel 2019. There are various time and date
functions which are present in the Excel 2019 version as mentioned below:

- DATE 
- DATEVALUE
- DAY
- DAYS
- DAYS360
- EDATE
- EOMONTH
- HOUR
- ISOWEEKNUM 
- MINUTE
- MONTH 

## Time and Date Functions
In this section, you will learn about each of these time and date functions through various scenarios.

### The DATE Function
The `DATE` function gives the sequential serial number that represents a particular date. We use `DATE` function when we take three different values and merge them to form a date.

The `DATE` function has the following syntax:


```
=DATE(YEAR, MONTH, DAY)
```
The `DATE` function has 3 arguments as `YEAR`, `MONTH` and `DAY`. All of the three arguments in the function are **REQUIRED**. 

- DAY
`DAY` argument represents day of the month from 1 - 31. If you use a value more than 31 for this argument, it will be added to the first days of the month given as the second argumet. For an instance if you use 32 in third argument **`=DATE(2005, 11, 32)`** in excel, it will give output as **`02-12-2005`**.

- MONTH
`MONTH` argument represents the month of the year from 1 - 12. If you use a value more than 12 for this argument, it will be added to the first months of the year given as the first argumet. For an instance if you use 16 in second argument **`=DATE(2005, 16, 2)`** in excel, it will give output as **`02-04-2006`**.

- YEAR
`YEAR` argument can contain one to four digits. It is always better to use four digits as argument in function to avoid any kind of confusion as Microsoft Excel for Windows uses the 1900 date system by default. So, if you use one digit in first argument **`=DATE(1, 11, 2)`** in excel, it will give output as **`02-11-1901`**. So it is always a good practice to four digits in the first arguemnt. 

Let us consider a scenario where you can learn how to implement the `DATE` function in Excel. Consider the example given below.

| A | B | C | D | E |
| --- | --- | --- | --- | --- |
| **SR. NO.** | **YEAR** | **MONTH** | **DAY** | **RESULT** |
| 1 | 2019 | 08  | 19 | ? |
| 2 | 2019 | 11 | 5 | ? |
| 3 | 2019 | 10 | 5 | ? |

Therefore, let us put the formula **`=DATE(B1, C1, D1)`** in cell `E1` and then apply it in subsequent rows. The result will be updated as shown below:

| A | B | C | D | E |
| --- | --- | --- | --- | --- |
| **SR. NO.** | **YEAR** | **MONTH** | **DAY** | **RESULT** |
| 1 | 2019 | 08  | 19 | 19-08-2019 |
| 2 | 2019 | 11 | 5 | 05-11-2019 |
| 3 | 2019 | 10 | 5 | 05-10-2019 |

### The DATEVALUE Function
`DATEVALUE` function is used to convert date available as text to a serial number and that will be recognized as a date by an Excel. 

The `DATEVALUE` function has the following syntax:


```
=DATEVALUE(DATE_TEXT)
```
`DATE_TEXT` is a **REQUIRED** argument in the `DATEVALUE` function.
Let us consider a scenario where you can learn how to implement the `DATEVALUE` function in Excel. Consider the example given below.

| A | B | C |
| --- | --- | --- |
| **SR. NO.** | **DATE_TEXT** | **RESULT** |
| 1 | "05-11-2019" | =DATEVALUE("05-11-2019")|
| 2 | "18-08-2019" | =DATEVALUE("18-08-2019") |
| 3 | "19-08-2019" | =DATEVALUE("19-08-2019") |

The result will be updated as shown below:

| A | B | C |
| --- | --- | --- |
| **SR. NO.** | **DATE_TEXT** | **RESULT** |
| 1 | "05-11-2019" | 43774 |
| 2 | "18-08-2019" | 43695 |
| 3 | "19-08-2019" | 43696 |

To avoid  any possible error, right click on the cell containing `DATE_TEXT` and select `Format Cells...` -> `text` under Number tab -> `OK`.

### The DAY Function
The `DAY` function returns day of the given date or serial number and it ranges from 1-31.
The `DAY` function has the following syntax:


```
=DAY(DATE/SERIAL NUMBER)
```

Let us consider a scenario where you can learn how to implement the `DAY` function in Excel. You can consider the example given in `DATEVALUE` function and find the day of the serial number given as output in that example.

| A | B | C | D |
| --- | --- | --- | --- |
| **SR. NO.** | **DATE_TEXT** | **RESULT** | **DAY** |
| 1 | "05-11-2019" | 43774 | ? |
| 2 | "18-08-2019" | 43695 | ? |
| 3 | "19-08-2019" | 43696 | ? |

Therefore, let us put the formula **`=DAY(C1)`** in cell `D1` and then apply it in subsequent rows. The result will be updated as shown below:

| A | B | C | D |
| --- | --- | --- | --- |
| **SR. NO.** | **DATE_TEXT** | **RESULT** | **DAY** |
| 1 | "05-11-2019" | 43774 | 5 |
| 2 | "18-08-2019" | 43695 | 18 |
| 3 | "19-08-2019" | 43696 | 19 |

### The DAYS Function
The `DAYS` function is used to calculate the days between two given dates.
The `DAYS` function has the following syntax:


```
=DAYS(end_date, start_date)
```
Let us consider a scenario where you can learn how to implement the `DAYS` function in Excel.  Consider the example given below.


| A | B | C | D |
| --- | --- | --- | --- |
| **SR. NO.** | **END_DATE** | **START_DATE** | **DAY** |
| 1 | 19-08-2019 | 18-08-2019 | ? |
| 2 | 05-11-2019 | 05-11-2018 | ? |
| 3 | 18-07-2019 | 18-06-2019 | ? |

Therefore, let us put the formula **`=DAYS(B1,C1)`** in cell `D1` and then apply it in subsequent rows. It will calculate the days between the **END_DATE** and **START_DATE** and the result in **DAY** will be updated as shown below:


| A | B | C | D |
| --- | --- | --- | --- |
| **SR. NO.** | **END_DATE** | **START_DATE** | **DAY** |
| 1 | 19-08-2019 | 18-08-2019 | 1 |
| 2 | 05-11-2019 | 05-11-2018 | 365 |
| 3 | 18-07-2019 | 18-06-2019 | 30 |

