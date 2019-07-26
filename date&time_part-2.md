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

### The NETWORKDAYS.INTL Function
The `NETWORKDAYS.INTL` function is very similar to the `NETWORKDAYS` function. This function also gives the total number of workdays between two dates but has a parameter that avails you the option to select the day/days that you want to select as weekend which makes it different than the `NETWORKDAYS` function.

The `NETWORKDAYS.INTL` function has the following syntax:


```
=NETWORKDAYS.INTL(start_date, end_date, [weekend], [holidays])
```

The first argument `start_date` and the second argument `end_date` are **required** arguments in the function whereas the third argument `weekend` and the fourth argument `holidays` are optional. The value of the third argument `weekend` represents the following days.

| **weekened_value** | **weekend_days** |
| --- | --- |
| 1 or omitted | Saturday, Sunday |
| 2 | Sunday, Monday |
| 3 | Monday, Tuesday |
| 4 | Tuesday, Wednesday |
| 5 | Wednesday, Thursday |
| 6 | Thursday, Friday |
| 7 | Friday, Saturday |
| 11 | Sunday only |
| 12 | Monday only |
| 13 | Tuesday only |
| 14 | Wednesday only |
| 15 | Thursday only |
| 16 | Friday only |
| 17 | Saturday only |

Let us consider a scenario where you can learn how to implement the `NETWORKDAYS.INTL` function in Excel. Consider the example given below:


| A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- |
| **Sr. No.** | **Start_Date** | **End_Date** | **Weekend** | **Holiday** | **WorkDays** |
| 1 | 23-Jul-19 | 30-Jul-19 | 1 |   | =NETWORKDAYS.INTL(B1,C1,D1) |
| 2 | 01-Jan-19 | 31-Jan-2019 | 2 | 26-Jan-2019 | =NETWORKDAYS.INTL(B2,C2,D2,E2) |
| 3 | 24-Jul-19 | 23-Aug-2019 | 3 | 15-Aug-2019 | =NETWORKDAYS.INTL(B3,C3,D3,E3) |

The result will be updated as shown below:

| A | B | C | D | E | F |
| --- | --- | --- | --- | --- | --- |
| **Sr. No.** | **Start_Date** | **End_Date** | **Weekend** | **Holiday** | **WorkDays** |
| 1 | 23-Jul-19 | 30-Jul-19 | 1 |   | 6 |
| 2 | 01-Jan-19 | 31-Jan-2019 | 2 | 26-Jan-2019 | 22 |
| 3 | 24-Jul-19 | 23-Aug-2019 | 3 | 15-Aug-2019 | 22 |

### The NOW Function
The `NOW` function provides us the serial number of current date and time. If the cell format is `General`, the output of the function is adjusted as per your regional date and time setting.

The `NOW` function has the following syntax:


```
=NOW()
```

The `NOW` function has no argumnets.
Let us consider a scenario where you can learn how to implement the `NOW` function in Excel. Consider the example given below:

| **FUNCTION** | **OUTPUT** | **DETAILS** |
| --- | --- | --- |
| =NOW() | 25-07-2019 23:54 | return current date and time |
| =NOW() + 2 | 27-07-2019 23:54 | return date and time two days in future |
| =NOW() - 0.5 | 27-07-2019 11:54 | Returns the date and time 12 hours ago (-0.5 days ago) |

### The SECOND Function
The `SECOND` function return seconds of a given time value/serial number and it ranges between 0-59.

The `SECOND` function has the following syntax:


```
=SECOND(time_value/ serial_number)
```

Let us consider a scenario where you can learn how to implement the `SECOND` function in Excel. Consider the example given below:

| A | B | C |
| --- | --- | --- |
| **Sr. No.** | **Time** | **Function** | 
| 1 | 15:45:20 PM | =SECOND(B1) |
| 2| 16:28 PM | =SECOND(B2) |
| 3 | 12:20:30 PM | =SECOND(B3) |

The result will be updated as shown below:

| A | B | C |
| --- | --- | --- |
| **Sr. No.** | **Time** | **Function** | 
| 1 | 15:45:20 PM | 20 |
| 2| 16:28 PM | 0 |
| 3 | 12:20:30 PM | 30 |

### The TIME Function
The `TIME` function return us the serial number for a given time and it ranges from  0 (zero) to 0.99988426, which represents the times from 0:00:00 (12:00:00 AM) to 23:59:59 (11:59:59 P.M.).

The `TIME` function has the following syntax:


```
=TIME(hour, minute, second)
```
Let us consider a scenario where you can learn how to implement the `TIME` function in Excel. Consider the example given below:

| A | B | C | D | E |
| --- | --- | --- | --- | --- |
| **Sr. No.** | **Hour** | **Minute** | **Second** | **Output** |
| 1 | 12 | 30 | 45 | =TIME(A1,B1,C1) |
| 2 | 12 | 0 | 0 | =TIME(A2,B2,C2) |
| 3 | 14 | 24 | 34 | =TIME(A3,B3,C3) | 

The result will be updated as shown below:

| A | B | C | D | E |
| --- | --- | --- | --- | --- |
| **Sr. No.** | **Hour** | **Minute** | **Second** | **Output** |
| 1 | 12 | 30 | 45 | 0.521354167 |
| 2 | 12 | 0 | 0 | 0.5 |
| 3 | 14 | 24 | 34 | 0.600393519 | 

### The TIMEVALUE Function

The `TIMEVALUE` function Returns the serial number of the text formatted time and ranges from 0 (zero) to 0.99988426, which represents times from 0:00:00 (12:00:00 AM) to 23:59:59 (11:59:59 P.M.).

The `TIMEVALUE` function has the following syntax:


```
=TIMEVALUE(time_text)
```
Let us consider a scenario where you can learn how to implement the `TIMEVALUE` function in Excel. Consider the example given below:

| A | B | C |
| --- | --- | --- |
| **Sr. No.** | **Function** | **Output** | 
| 1 | =TIMEVALUE("01:30 AM") | ? |
| 2 | =TIMEVALUE("04:30 AM") | ? |
| 3 | =TIMEVALUE("04:30 PM") | ? |

The result will be updated as shown below:

| A | B | C |
| --- | --- | --- |
| **Sr. No.** | **Function** | **Output** | 
| 1 | =TIMEVALUE("01:30 AM") | 0.0625 |
| 2| =TIMEVALUE("04:30 AM") | 0.1875 |
| 3 | =TIMEVALUE("04:30 PM") | 0.6875 |

### The TODAY Function
The `TODAY` funcion returns current date if the cell was formatted as general before writing function in it. If the cell is formatted as number, it will return serial nunmber.

The `TODAY` function has the following syntax:


```
=TODAY()
```
The `TODAY` function has no argument. 
Let us consider a scenario where you can learn how to implement the `TODAY` function in Excel. Consider the example given below:

| A | B | C |
| --- | --- | --- |
| **Sr. No.** | **Function** | **Output** | 
| 1 | =TODAY() | ? |
| 2| =TOADY() + 30 | ? |
| 3 | =TODAY() -30 | ? |

The result will be updated as shown below:

| A | B | C |
| --- | --- | --- |
| **Sr. No.** | **Function** | **Output** | 
| 1 | =TODAY() | 26-07-2019 |
| 2| =TOADY() + 30 | 25-08-2019 |
| 3 | =TODAY() - 30 | 26-06-2019 |

### The WEEKDAY Function
The `WEEKDAY` function returns day of the week for a given date as input. The day of the week is returned as as an integer, ranging from 1 (Sunday) to 7 (Saturday), by default.

The `WEEKDAY` function has the following syntax:


```
=WEEKDAY(serial_number/date,[return_type])
```
First argument in the function is `required` whereas the second argument is optional and is a number that determines the type of return value. Consider the table given below for second argument.

| Return_type | Number returned |
| --- | --- |
| 1 or omitted | Numbers 1 (Sunday) through 7 (Saturday). Behaves like previous versions of Microsoft Excel. |
| 2 | Numbers 1 (Monday) through 7 (Sunday). |
| 3 | Numbers 0 (Monday) through 6 (Sunday). |
| 11 | Numbers 1 (Monday) through 7 (Sunday). |
| 12 | Numbers 1 (Tuesday) through 7 (Monday). |
| 13 | Numbers 1 (Wednesday) through 7 (Tuesday). |
| 14 | Numbers 1 (Thursday) through 7 (Wednesday). |
| 15 | Numbers 1 (Friday) through 7 (Thursday). |
| 16 | Numbers 1 (Saturday) through 7 (Friday). |
| 17 | Numbers 1 (Sunday) through 7 (Saturday). |

Let us consider a scenario where you can learn how to implement the `WEEKDAY` function in Excel. Consider the example given below:

| A | B | C | D |
| --- | --- | --- | --- |
| **Sr. No.** | **Date** | **Function** | **Output** | 
| 1 | 26-Jul-19 | =weekday(A1) | ? |
| 2| 26-Jul-19 | =weekday(A2,2) | ? |
| 3 | 26-Jul-19 | =weekday(A3,3) | ? |

The result will be updated as shown below:

| A | B | C | D |
| --- | --- | --- | --- |
| **Sr. No.** | **Date** | **Function** | **Output** | 
| 1 | 26-Jul-19 | =weekday(A1) | 6 |
| 2| 26-Jul-19 | =weekday(A2,2) | 5 |
| 3 | 26-Jul-19 | =weekday(A3,3) | 4 |
