## Introduction
In this guide, you will learn how to work with financial functions in Microsoft Excel 2019. There are various financial functions which are present in the Excel 2019 version, as mentioned below:

- FV 
- FVSCHEDULE 
- PV

## Financial Functions
In this section, you will learn about each of these financial functions through various scenarios.

### The FV Function
The `FV` function gives us the future value of a particular investment which has a constant interest rate and payment can be periodic, constant payments, or a single lump sum payment.

The `FV` function has the following syntax:


```
=FV(rate,nper,pmt,[pv],[type])
```

The arguments used in this function are mentioned below:

- rate = `required`, it is the interest rate/period.
- nper = `required`, number of payment periods.
- pmt = `required`,  payment made per period.
- pv = `optional`, present value. If **pv** is omitted, it is assumed to be 0 (zero), and you must include the **pmt** argument in the function.
- type = `optional`, the number 0 or 1 and indicates when payments are due. If type is omitted, it is assumed to be 0 (zero means it is asssumed that the payment has been made at the end of the period and 1 means it is asssumed that the payment has been made at the beginning of the period).

Let us consider a scenario where you can learn how to implement the `FV` function in Excel. Let's consider that five members of a group have made some investments in different banks in 2019. The payment has been made yearly ever since. The interest rate for each one of them is different. What would be the `FV` for each of those members in 2024?

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **members** | **rate** | **nper** | **pmt** | **pv** | **type** | **updated FV amount** |
| Pam | 10% | 5 | 1  | -1000 | 0 | ? |
| Rambo | 12% | 5 | 1 | -1000 | 0 | ? |
| Rita | 8% | 5 | 1 | -1000 | 1 | ? |
| Sam | 6% | 5 | 1  | -1000 | 0 | ? |
| Tina | 15%  | 5 | 1 | -1000 | 1 | ? |

In order to calculate the value, let us put the formula **`=fv(B1, C1, D1,E1,F1)`** in cell `G1` and then apply it in subsequent rows. This will give result as the updated amount as shown:

|    A    |  B   |  C   |  D  |   E   |  F   |     G      |
| --- | --- | --- | --- | --- | --- | --- |
| **members** | **rate** | **nper** | **pmt** | **pv** | **type** | **updated FV amount** |
| Pam | 10% | 5 | 1  | -1000 | 0 | ₹ 1,604.40 |
| Rambo | 12% | 5 | 1 | -1000 | 0 | ₹ 1,755.99 |
| Rita | 8% | 5 | 1 | -1000 | 1 | ₹ 1,462.99 |
| Sam | 6% | 5 | 1  | -1000 | 0 | ₹ 1,332.59 |
| Tina | 15%  | 5 | 1 | -1000 | 1 | ₹ 2,003.60 |

### The FVSCHEDULE Function
The `FVSCHEDULE` function helps us to calculate the future value of an investment with the interest rate that varies. 

The `FVSCHEDULE` function has the following syntax:


```
=FVSCHEDULE(principal, schedule)
```

The arguments used in this function are mentioned below:

- principal = `required`, it is the present value or the investment 
- schedule = `required`, it is an array of interest rates that will be applied.

Let us consider a scenario where you can learn how to implement the `FVSCHEDULE` function in Excel. Let's consider that five members of a group have made some investments in different banks in 2019. The payment has been made yearly ever since. The interest rate for each of them is different every year. What would be the FV for each of those member in 2022?

| A | B | C | D | E | F | 
| --- | --- | --- | --- | --- | --- |
| **members** | **rate of first year** | **rate of second year** | **rate of third year** | **principal** | **future value** |
| Pam | 10% | 11% | 13% | 1000 | ? |
| Rambo | 12% | 13% | 15% | 1000 | ? |
| Rita | 8% | 7% | 10% | 1000 | ? |
| Sam | 6% | 12% | 16% | 1000 | ? |
| Tina | 15% | 16% | 12% | 1000 | ? |

In order to calculate the value, let us put the formula **`=FVSCHEDULE(E1, B1:D1)`** in cell `F1` and then apply it in subsequent rows. This will give result as the updated amount as shown:

| A | B | C | D | E | F | 
| --- | --- | --- | --- | --- | --- |
| **members** | **rate of first year** | **rate of second year** | **rate of third year** | **principal** | **future value** |
| Pam | 10% | 11% | 13% | 1000 | 1379.73 |
| Rambo | 12% | 13% | 15% | 1000 | 1455.44 |
| Rita | 8% | 7% | 10% | 1000 | 1271.16 |
| Sam | 6% | 12% | 16% | 1000 | 1377.152 |
| Tina | 15% | 16% | 12% | 1000 | 1494.08 |

### The PV Function
The `PV` function helps us to calculate present value of an investment based on a constant interest rate.

The `PV` function has the following syntax:


```
=PV(rate, nper, pmt, [fv], [type])
```

The arguments used here are very similar to the ones that are used in the `FV` function explained above. 

Let us consider a scenario where you can learn how to implement the `PV` function in Excel. Let's consider that five members of a group have made some investments in different banks in 2019. The payment has been made yearly ever since. The interest rate for each of them is different. If we have the FV amount made in 2024, what was the investment amount in 2019?

| A | B | C | D | E | F | G |
| --- | --- | --- | --- | --- | --- | --- |
| **members** | **rate** | **nper** | **pmt** | **fv** | **type** | **pv amount** |
| Pam | 10% | 5 | 1  | ₹ 1,604.40 | 0 | ? |
| Rambo | 12% | 5 | 1 | ₹ 1,755.99 | 0 | ? |
| Rita | 8% | 5 | 1 | ₹ 1,462.99 | 1 | ? |
| Sam | 6% | 5 | 1  | ₹ 1,332.59 | 0 | ? |
| Tina | 15%  | 5 | 1 | ₹ 2,003.60 | 1 | ? |


In order to calculate the value, let us put the formula **`=fv(B1, C1, D1,E1,F1)`** in cell `G1` and then apply it in subsequent rows. This will  result as the present value as shown:

| A | B | C | D | E | F | G |
| --- | --- | --- | --- | --- | --- | --- |
| **members** | **rate** | **nper** | **pmt** | **fv** | **type** | **pv amount** |
| Pam | 10% | 5 | 1  | ₹ 1,604.40 | 0 | ₹ -1,000.00 |
| Rambo | 12% | 5 | 1 | ₹ 1,755.99 | 0 | ₹ -1,000.00 |
| Rita | 8% | 5 | 1 | ₹ 1,462.99 | 1 | ₹ -1,000.00 |
| Sam | 6% | 5 | 1  | ₹ 1,332.59 | 0 | ₹ -1,000.00 |
| Tina | 15%  | 5 | 1 | ₹ 2,003.60 | 1 | ₹ -1,000.00 |

### The NPV Function
The NPV or Net Present Value is the sum total of positive and negative cash flows over the years. In other words, it calculates the net present value of an investment at a given discount rate and a series of negative values (future payments) and positive values (income).

It's syntax is given below:


```
NPV = (Rate, Value 1, [Value 2], [Value 3]…)
```

To understand the function, let us consider a case of an individual who did an initial investment of USD 5000 at an annual discount rate of 0.5% along with five corresponding year returns as 2000, 1500, 1500, 1800, and 1800 respectively.


| A | B |
| --- | --- |
| **Details** | **In USD**  |
| Rate | 5% |
| Initial Investment | 5000.00 |
| First-year return  | 2000.00 |
| Second-year return | 1500.00 |
| Third-year return  | 1500.00 |
| Fourth-year return | 1800.00 |
| Fifth-year return  | 1800.00 |

To implement the NPV function use the following:


```
=NPV(B2,B4:B8)-B3
```

which gives an output of **USD 2452.27**.


### The XNPV Function
The XNPV function is quite similar to the NPV function except that here we provide dates for each return. The syntax is given below:


```
=XNPV(Rate, Values, Dates)
```

Let us take the above example but this time we also mention dates corresponding to each value:

| A | B | C |
| --- | --- | --- |
| **Details** | **In USD**  | **Dates** |
| Rate | 5% |   |
| Initial Investment | -5000.00 | 01 January 2000 |
| First-year return  | 2000.00 | 01 February 2001 |
| Second-year return | 1500.00 | 01 February 2002 |
| Third-year return  | 1500.00 | 01 April 2003 |
| Fourth-year return | 1800.00 | 01 August 2004 |
| Fifth-year return  | 1800.00 | 01 September 2005 |

Now, to implement the `XNPV` function, you need to make sure that the initial investment value is present in the negative format and then pass the values in the function as given below:


```
=XNPV(B2,B3:B8, C3:C8)
```

which gives the value of **USD 233547**.
