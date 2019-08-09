## Introduction
In this guide, you will learn about various statistical functions which are available in Excel 2019. By the end of this guide, you'll become familiar with some important statistical functions with examples. Later, you can explore the rest of the functions using the Excel provided documentation.

The functions which we are going to learn in this guide are mentioned below:
- AVERAGE
- AVERAGEIF
- MEDIAN
- PERMUT

## Statistical Functions
In this section, we will list out the above stated functions:

### The AVERAGE Function
Let us start with the most commonly used function, the AVERAGE. It gives us the average of `n` numbers by summing them up and dividing by the total numbers summed up. It is not necessary that only two numbers need to be averaged as that's what most of the beginners believe. Here's the syntax for the function:


```
=AVERAGE(n1, n2, n3 ... nn)
```

To elaborate this function with an example, consider the given tabular data which consists of three students' marks data and you need to find the average marks:

| A | B | C | D |
| --- | --- | --- | --- |
| **Subject 1** | **Subject 2** | **Subject 3** | **Result** |
| 26 | 38 | 78 | ? |
| 65 | 78 | 11 | ? |
| 12 | 88 | 50 | ? |

To find the average marks for each student, you need to deploy the given formula in **D1** and then stretch it all the way down for rest of the two, `=AVERAGE(A1, B1, C1)`, resulting in the following answer:

| A | B | C | D |
| --- | --- | --- | --- |
| **Subject 1** | **Subject 2** | **Subject 3** | **Result** |
| 26 | 38 | 78 | 47.33 |
| 65 | 78 | 11 | 51.33 |
| 12 | 88 | 50 | 50 |


### The AVERAGEIF Function
Now, in the above example, consider we only need to average those subject marks where student has scored more than 50. Such result can't be calculated using the `AVERAGE` function, therefore, a need of a new function, the `AVERAGEIF` function. The syntax is given below:


```
=AVERAGEIF(range, criteria, [average_range])
```

Now, let us form a tabular data of a student whose marks in four out of five subjects are known and we need to find the average marks considering only those subjects where she has scored more than 50.

| A | B |
| --- | --- |
| **Subjects** | **Marks** |
| Subject 1 | 26 |
| Subject 2 | 65 |
| Subject 3 | 12 |
| Subject 4 |  |
| Subject 5 | 78 |

Now, in any new cell, you can write the given formula to arrive at the result:


```
=AVERAGEIF(B1:B5, ">50")
```

which gives us the result as **71.5** by avoiding marks of the subjects 1, 3 and 4. 

### The MEDIAN Function
The `AVERAGE` function at the back-end uses the mean concept in calculation which has a disadvantage if their is an anomaly in the data. For example, consider a case where three doctors report their number of patients analyzed in five consecutive days as shown:


| A | B | C | D | E |
| --- | --- | --- | --- | --- | 
| **Day 1** | **Day 2** | **Day 3** | **Day 4** | **Day 5** |
| 8 | 12 | 16 | 10 | 87 |
| 12 | 15 | 10 | 11 | 9 |
| 8 | 4 | 1 | 0 | 2 |

So, if we try to average out the number of patients then the anomaly (87) for first doctor can bring skewness in the result, hence, in such scenarios we prefer to use median whose syntax in Excel is shown below:


```
=MEDIAN(n1, n2, n3 ... nn)
```

To apply the median on the table, you can proceed as `=MEDIAN(A1, B1, C1, D1, E1)` which results in the answer as **12** which if compared with the `=AVERAGE(A1, B1, C1, D1, E1)` with answer **26.6 = 27** makes more sense.

### The PERMUT Function
Permutation is one of the widely used concept in the realm of statistics. You can perform the permutation on a given data using the given syntax in Excel:


```
=PERMUT(n, n_chosen)
```

To understand what permutation is and how you can implement it in Excel, consider a case of three athletes of which only two need to be selected for a marathon. Permutation helps in answering this question without counting all the possibilities by hand. If we represent this case in a tablular format, it looks like this:

| A | B |
| --- | --- |
| **Number of athletes** | **To be chosen** |
| 3 | 2 |

You can implement the `PERMUT` function as shown:


```
=PERMUT(A1, B1)
```

which gives the answer as **6** stating that there are six possibilities to choose two athletes from a group of three.

### The COUNTBLANK Function
The COUNTBLANK function returns the number of blank cells in a given specified range of cells. This can be a very useful function when you need to know how many values are missing in a data.

The syntax for the COUNTBLANK function is given below:


```
=COUNTBLANK(range_of_cells)
```

To implement it in Excel, consider the given tabular data:

| A |
| --- |
| **Values** |
| 9 |
|  |
| 5 |
|  |
|  |
| 8 |
| 7 |

So, if you implement `=COUNTBLANK(A1:A7)` it counts the number of blank values. The result of the formula is **3** which represents the one blank value between **9** and **5** along with two blank values between **5** and **8**.

### The COUNTIF Function
Let us assume you need to calculate the number of people whose marks are above a cut-off decided at value 88. To do this, we can use the `COUNTIF` function whose syntax is given below:


```
=COUNTIF(range_of_cells)
```

To illustrate the scenario, consider the given tabular data:

| A |
| --- |
| **Marks** |
| 50 |
| 90 |
|  |
| 23 |
| 65 |
| 98 |
| 55 |

On the given tabular data, implement the following formula:


```
=COUNTIF(A1:A7, ">88")
```
which results in the value **2** for the values 90 and 98. Note that the function has also ignored the blank cell.
