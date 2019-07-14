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

Let us consider a scenario where you can learn how to implement the `DATE` function in Excel.


