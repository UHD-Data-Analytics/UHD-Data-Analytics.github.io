---
title: "If-Else Statements in Python"
description: "Overview and examples of the If-Else control flow logic in Python"
collection: python
---

# Python If/Else
==============

Decision making is required when we want to execute a code only if a
certain condition is satisfied.The if…elif…else statement is used in
Python for decision making.The syntax for the if else is as below:

```python
    if test expression: statement(s)
```
Here, the program evaluates the test expression and will execute
statement(s) only if the text expression is True.If the text expression
is False, the statement(s) is not executed.In Python, the body of the if
statement is indicated by the indentation. Body starts with an
indentation and the first unindented line marks the end.Python
interprets non-zero values as True. None and 0 are interpreted as False.
For example

```python
    x = 5
    if x > 0:
      print("x is greater than 0")
```
    ## x is greater than 0

In the example, the value of x is assigned as 5. And the condition is
checked that if the number is greater that zero, then only print the
“Positive number” otherwise it does not print.

Now, the else part is optional and is only evaluated if test\_expression
is FALSE.It is important to note that else must be in the same line as
the closing braces of the if statement.

```python
    x = -5
    if x > 0:
      print("Non-negative number")
    else:
      print("Negative number")
```

    ## Negative number

Here the if condition is false and the else statement is executed.

### Python IF –Elseif
------------------------

The elif is short for else if. It allows us to check for multiple
expressions.If the condition for if is False, it checks the condition of
the next elif block and so on.If all the conditions are False, body of
else is executed.Only one block among the several if…elif…else blocks is
executed according to the condition.The if block can have only one else
block. But it can have multiple elif blocks.The syntax is as below:

```python
    if test expression:
           Body of if
    elif test expression:
           Body of elif
    else: 
          Body of else
```

```python
    x = 0
    if x < 0:
      print("Negative number")
    elif x > 0:
      print("Non-negative number")
    else:
      print("Zero")
```

    ## Zero

Here initial two conditions are checked and and come out to be false and
else statement is executed and “Zero” is printed.

To see the more about the else if plese go to the link
<https://www.youtube.com/watch?v=qf0sfRZ0hHc> and this link
<https://www.youtube.com/watch?v=42MBMSOZgD4&list=PLQVvvaa0QuDe8XSftW-RAxdo6OmaeL85M&index=10>
