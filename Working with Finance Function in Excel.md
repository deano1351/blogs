## Introduction
In this guide, you will learn how to work with financial Functions in Excel Microsoft Excel 2019. There are various financial functions which are present in the Excel 2019 version, as mentioned below:

- FV 

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
- type = `optional`, The number 0 or 1 and indicates when payments are due. If type is omitted, it is assumed to be 0( 0 means it is asssumed that the payment has been made at the end of the period).
