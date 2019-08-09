## Introduction
In this guide, you will learn how to work with financial functions in Microsoft Excel 2019. There are various financial functions which are present in the Excel 2019 version, as mentioned below:

- FV 
- FVSCHEDULE 
- PV
- NPV
- XNPV
- PMT
- PPMT
- RATE
- EFFECT

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

### The PMT Function
The PMT or denotes the periodical payment required to pay off for a particular period of time with a constant interest rate. Let’s have a look at how to calculate it in excel –


```
=PMT(Rate, Nper, PV, [FV], [Type])
```

The arguments stand for `Nper` (Number of periods), `PV` (Present Value), and `FV` (Future value).

To learn to implement the function in Excel, let's consider a case where we need to find the PMT for a person who need to pay an amount of USD 5000 in five years at an interest rate of 5%.

| A | B |
| --- | --- |
| **Details** | **In USD** | 
| Rate | 5% |
| Number of periods | 5.00 | 
| Present Value | 5000.00 |

To calculate PMT, we use the function as shown:


```
=PMT(B2, B3, B4)
```

which gives us the value as **-1154.87**. Note that we have not included the `FV` and `Type` value for our example.

### The PPMT Function
The PPMT function is a variation of the PMT function where the payment is calculated on the principal with a constant interest rate and constant periodic payments.

Here's the syntax:


```
=PPMT(Rate, Per, Nper, PV, [FV], [Type])
```

where all the arguments have the same meaning as that of the PMT function except `Per` which denotes the period for which the principal is to be calculated.

Let's consider the same example as that of PMT function and try to find out the PPMT for first, second and third years.

| Year | PPMT | Result |
| --- | --- | --- |
| First Year | `=PPMT(B2, 1, B3, B4)` | -904.87 | 
| Second Year | `=PPMT(B2, 2, B3, B4)` | -950.12 | 
| Third Year | `=PPMT(B2, 3, B3, B4)` | -997.62 |

### The RATE Function
The RATE function helps to answer the interest rate needed to pay off the loan in full for a given period of time.

Here's the syntax:


```
=RATE(NPER, PMT, PV, [FV], [Type], [Guess])
```

The new arguments stands for `NPER` (number of periods), `PMT` (amount paid per period), `Guess` (your guess on what should be the interest rate).

Let's consider an example of a person who has taken a loan of USD 50000 from a bank which he paid in 6 years with USD 10000 yearly. We need to calculate the interest rate in this situation.

Here's the data in tablular format:

| A | B |
| --- | --- |
| Years | 6 |
| PMT | -10000 |
| Loan | 50000 |

To implement the RATE function on the given table with a guess of rate as 2%, use:


```
=RATE(B2, B3, B4, 0, 0, 0.02)
```

which gives us the estimated rate as **5%**.

### The EFFECT Function
The EFFECT function is used to find the effective annual interest rate when you're given with the nominal interest rate and the times of compounding per year. The syntax for this function is given below:


```
=EFFECT(Nominal_Rate, N_COMP_YEAR)
```

To understand this with an example, consider a nominal interest rate of 10% and the number of compounding per year as 12, then we can find the effective annual interest rate as shown:

| A | B |
| --- | --- |
| Nominal rate | 10% |
| N_COMP_YEAR | 12 |


```
=EFFECT(B1, B2)
```

which gives us the result as **10%**.
