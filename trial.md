## Introduction
In this guide, you will learn how to work with logical functions in Mcirosoft Excel 2019. There are various logical functions which are present in the Excel 2019 version as mentioned below:

- TRUE
- FALSE
- OR
- AND
- NOT
- XOR
- IF  
- IFERROR 
- IFNA 
- IFS
- SWITCH 

## Logical Functions
In this section, you will learn about each of these logical functions through various scenarios.

### The TRUE and FALSE Functions
We use the `TRUE` and `FALSE` functions when we want to showcase if a given condition is met or not. For instance, `5 < 3` is a right condition hence the `TRUE` function when used with the `IF` function (or similar) returns a `TRUE` value. Had the condition been wrong it would had resulted in the `FALSE` value.

Notice, that `TRUE` function is not the same as the `TRUE` value. The `TRUE` function doesn't hold any argument inside the round brackets.
We will give you a scenario to implement these funcitons when we are discussing `IF` function.

### The OR Function
A logical `OR` function follows the given truth table:


| Input A | Input B | Input C | Output |
| --- | --- | --- | --- |
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 1 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 1 |
| 1 | 1 | 0 | 1 |
| 1 | 1 | 1 | 1 |

In the above table you can also consider `0` as a `FALSE` value and `1` as a `TRUE` value. As you can observe if any input has a `TRUE` value then the output of the logical `OR` function is `TRUE`. However, if all the inputs are `FALSE` then the output becomes `FALSE`. 

Let us consider a scenario where you can learn how to implement the logical `OR` function in Excel. We take five students attendance who have registered for a workshop. The final attendance is marked only when student is present any one of the day. Here's the data:

| | A | B | C | D | E |
| --- | --- | --- | --- | --- | --- |
| | **Student list** | **Day 1** | **Day 2** | **Day 3** | **Attendance** |
| 1 | Student 1    | TRUE  | FALSE | TRUE  | ? |
| 2 | Student 2    | TRUE  | TRUE  | TRUE  | ? |
| 3 | Student 3    | TRUE  | FALSE | TRUE  | ? |
| 4 | Student 4    | TRUE  | TRUE  | FALSE | ? |
| 5 | Student 5    | FALSE | FALSE | FALSE | ? |

So, to fill the attendance, we provide the following logical `OR` formula with syntax:


```
=OR(logical1, logical2, ... )
```

Therefore, let us put the formula **`=OR(B2, C2, D2)`** in cell `E2` and then apply it in subsequent rows. This will result in the updated attendance as shown:


| | A | B | C | D | E |
| --- | --- | --- | --- | --- | --- |
| | **Student list** | **Day 1** | **Day 2** | **Day 3** | **Attendance** |
| 1 | Student 1    | TRUE  | FALSE | TRUE  | **TRUE** |
| 2 | Student 2    | TRUE  | TRUE  | TRUE  | **TRUE** |
| 3 | Student 3    | TRUE  | FALSE | TRUE  | **TRUE** |
| 4 | Student 4    | TRUE  | TRUE  | FALSE | **TRUE** |
| 5 | Student 5    | FALSE | FALSE | FALSE | **FALSE** |

### The AND Function
A logical `AND` function follows the given truth table:


| Input A | Input B | Input C | Output |
| --- | --- | --- | --- |
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 0 |
| 0 | 1 | 0 | 0 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 0 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

As mentioned in the `OR` function section, you can also consider `0` as a `FALSE` value and `1` as a `TRUE` value. As you can observe if any input has a `FALSE` value then the output of the logical `AND` function is `FALSE`. However, if all the inputs are `TRUE` then the output becomes `TRUE`. 

The syntax of the logical `AND` function is given below:


```
=AND(logical1, logical2, ... )
```

To learn how to implemet `AND` function in the Excel, let us take the same student attendance scenario but this time let us consider that if student is absent even a single day then he/she will be marked absent (`FALSE` value).

This time cell `E2` will hold the following formula: **`=AND(B2, C2, D2)`**. This will result in the following attendance sheet where only one student is marked present.


| | A | B | C | D | E |
| --- | --- | --- | --- | --- | --- |
| | **Student list** | **Day 1** | **Day 2** | **Day 3** | **Attendance** |
| 1 | Student 1    | TRUE  | FALSE | TRUE  | **FALSE** |
| 2 | Student 2    | TRUE  | TRUE  | TRUE  | **TRUE** |
| 3 | Student 3    | TRUE  | FALSE | TRUE  | **FALSE** |
| 4 | Student 4    | TRUE  | TRUE  | FALSE | **FALSE** |
| 5 | Student 5    | FALSE | FALSE | FALSE | **FALSE** |

### The NOT Function
The logical `NOT` function has the following truth table:

| Input | Output | 
| --- | --- |
| TRUE | FALSE |
| FALSE | TRUE |

As you can observe from the table, the `NOT` function inverts a given logical input. Let us take a scenario to understand how to use it in Excel.

You have a data of people likings which even includes their `Veg` and `Non-Veg` type inputs as shown in the below table. How can you select people who are `Non-Veg`?


| | A | B |
| --- | --- | --- |
| | **Food Preference** | **Result** |
| 1 | Veg | ? |
| 2 | Non-Veg | ? |

To implement the `NOT` function, here's the syntax:


```
=NOT(logical condition)
```

So, we can write a condition to check if people food preference is `Veg` and then later pass the result to the `NOT` function. To achieve this, you can write **`=NOT(A2="Veg")`** in the cell `B1` which will give you the following result:


| | A | B |
| --- | --- | --- |
| | **Food Preference** | **Result** |
| 1 | Veg | **FALSE** |
| 2 | Non-Veg | **TRUE** |


### The XOR Function
A logical `XOR` function follows the given truth table:


| Input A | Input B | Input C | Output |
| --- | --- | --- | --- |
| 0 | 0 | 0 | 0 |
| 0 | 0 | 1 | 1 |
| 0 | 1 | 0 | 1 |
| 0 | 1 | 1 | 0 |
| 1 | 0 | 0 | 1 |
| 1 | 0 | 1 | 0 |
| 1 | 1 | 0 | 0 |
| 1 | 1 | 1 | 1 |

To understand the above table, consider two inputs at a time and if there is same value then the result is `FALSE` (or `0`), next use this result of the first two inputs and take the third input and perform the same action. To illustrate it, let us take the last row which has `1` for all the inputs. Here, Input A and B has `1` and `1` respectively which gives `0`, now combine this `0` and Input C (`1`). As you can observe that this time you have different values hence the output is `1`.

To illustrate this in Excel, let us consider an example where a child is presented with three different food items. At a time, she is given choice between the two, she can't choose both, once the choice from the first two is made then the third item is presented for a final choice.


| | A | B | C | D |
| --- | --- | --- | --- | --- |
| | **Candy** | **Ice-cream** | **Chocolate** | **Result** |
| 1 | TRUE  | FALSE     | FALSE     | ?   |
| 2 | TRUE  | FALSE     | TRUE      | ?  |
| 3 | FALSE | FALSE     | FALSE     | ?  |
| 4 | TRUE  | TRUE      | TRUE      | ?   |

The syntax for the logical `XOR` in Excel is:


```
=XOR(logical1, logical2, ... )
```

To solve the given scenario, we can implement `XOR` function starting with **`=XOR(A2, B2, C2)`** formula in the cell `D2` and stretching it to the subsequent rows. This results in the given result:


| | A | B | C | D |
| --- | --- | --- | --- | --- |
| | **Candy** | **Ice-cream** | **Chocolate** | **Result** |
| 1 | TRUE  | FALSE     | FALSE     | TRUE   |
| 2 | TRUE  | FALSE     | TRUE      | FALSE  |
| 3 | FALSE | FALSE     | FALSE     | FALSE  |
| 4 | TRUE  | TRUE      | TRUE      | TRUE   |


