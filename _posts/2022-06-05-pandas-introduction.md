---
layout: post
author: Ethan Guyant
title:  Data Manipulation - Pandas
categories: Python
description: An overview of various data manipulation functions and methods utilizing pandas dataframes.
---
### Contents
[Introduction to Pandas](#introduction-to-pandas)  

---

<br>


## Introduction to Pandas
Pandas is a fast, powerful, flexible and easy to use open source data analysis and manipulation tool, built on top of the Python programming language ([pandas](https://pandas.pydata.org/)). Pandas excels at working with tabular which can be stored using pandas DataFrames. 

Below is an example DataFrame that will be used through out this post.

```python
>>> type(df)
<class 'pandas.core.frame.DataFrame'>
>>> df
  Col A  Col B  Col C
0     A      1    9.0
1     A      2    8.0
2     A      3    7.0
3     B      4    NaN
4     B      5    6.0
5     C      6    5.0
```
### Dataframes are composed of three components:
* Values: the `.values` attribute contains the data values in a 2D NumPy array
```python
>>> df.values
array([['A', 1, 9.0],
       ['A', 2, 8.0],
       ['A', 3, 7.0],
       ['B', 4, nan],
       ['B', 5, 6.0],
       ['C', 6, 5.0]], dtype=object)
```
* Column Labels: the `.columns` attribute contains the column names of the DataFrame
```python
>>> df.columns
Index(['Col A', 'Col B', 'Col C'], dtype='object')
```
* Index: the `.index` attribute contains row number or now names
```python
>>> df.index
RangeIndex(start=0, stop=6, step=1)
```