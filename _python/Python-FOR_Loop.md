---
title: "For Loops in Python"
description: "Overview and examples of a for loop in Python"
collection: python
---

# Python FOR LOOP
===============

The for loop in Python is used to iterate over a sequence (list, tuple,
string) or other iterable objects. Iterating over a sequence is called
traversal.The syntax of the FOR loop is as shown below:

```python
    for val in sequence:  
```
### Body of for

Here, val is the variable that takes the value of the item inside the
sequence on each iteration.Loop continues until we reach the last item
in the sequence. The body of for loop is separated from the rest of the
code using indentation.

```python
    # Program to find the sum of all numbers stored in a list
    # List of numbers
    numbers = [6, 5, 3, 8, 4, 2, 5, 4, 11]
    # variable to store the sum
    sum = 0
    # iterate over the list
    for val in numbers:
        sum = sum+val
    # Output: The sum is 48
    print("The sum is {sum}".format(sum=sum))
```

    The sum is 48


In this example, each number is picked up from the list and added in the
variable sum.Therfore the sum variable has final sum 48.

For video tutorial please follow the link
<https://www.youtube.com/watch?v=zFvoXxeoosI>
