## Introduction
In this guide, you will learn how to work with financial Functions in Excel Microsoft Excel 2019. There are various financial functions which are present in the Excel 2019 version, as mentioned below:

- FV 
- FVSCHEDULE 
## Financial Functions
In this section, you will learn about each of these financial functions through various scenarios.

### The FV Function
The `FV` function gives us the future value of a particular investment which has a constant interest rate and payment can be periodic, constant payments, or a single lump sum payment.

The `FV` function has the following syntax:


```
=FV(rate,nper,pmt,[pv],[type])
```
The arguments used in this function are mentioned below:

- rate = `required`, It is the interest rate/period.
- nper = `required`, Number of payment periods.
- pmt = `required`,  payment made per period.
- pv = `optional`, present value. If pv is omitted, it is assumed to be 0 (zero), and you must include the pmt argument in the function.
- type = `optional`, The number 0 or 1 and indicates when payments are due. If type is omitted, it is assumed to be 0(zero)( zero means it is asssumed that the payment has been made at the end of the period and one means it is asssumed that the payment has been made at the beginning of the period).

Let us consider a scenario where you can learn how to implement the `FV` function in Excel. Let's consider that 5 member of a group have made some investments in different banks in 2019. The payment has been made yearly ever since. The interest rate for each of them is different. What would be the FV for each of those members in 2024?

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
| members | rate | nper | pmt | pv    | type | function   |
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

- principal = `required`, It is the present value or the investment 
- Schedule = `required`, It is an array of interest rates that will be applied.


Let us consider a scenario where you can learn how to implement the `FVSCHEDULE` function in Excel. Let's consider that 5 member of a group have made some investments in different banks in 2019. The payment has been made yearly ever since. The interest rate for each of them is different every year. What would be the FV for each of those members in 2022?

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