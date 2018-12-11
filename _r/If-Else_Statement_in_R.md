---
title: "If-Else Statements in R"
description: "An overview on how to write if and else statements in R"
collection: r
---

# If/Else Statement in R
======================




Decision making is an important part of programming. This can be
achieved in R programming using the conditional “if…else” statement.

Let’s start out with the simple “IF”" statement in R. The basics of the
IF command are as follows:

```r
if (test_expression) { statement }
````

Here we are saying: If the ‘test_expression’ is TRUE, the ‘statement’
gets executed. But, if it’s FALSE, nothing happens. The test_expression
can be a logical or numeric vector, but only the first element is taken
into consideration. For example, let run this code:

```r
    x <- 5
    if(x > 0){
    print("Greater than zero")
    }
```
    [1] "Greater than zero"

Obviously, 5 is greater than 0, so our code prints “Greater than zero”

To take it a step further, we can add an “Else” statement to our “If”"
statement. The syntax of if…else statement is:

```r
if (test_expression) { statement1 } else { statement2 }
```

The “Else’ part is optional, and is only run if our”test\_expression’ is
FALSE. It is important to note that “else”" must be in the same line as
the closing braces of the if statement. For example:

```r
    x <- -5
    if(x > 0){
    print("Non-negative number")
    } else {
    print("Negative number")
    }
```
    [1] "Negative number"

The above conditional can also be written in a single line as follows:

```r
    if(x > 0) print("Non-negative number") else print("Negative number")
```
    [1] "Negative number"

As you can see,when using R, sometimes you need your function to do
something if a condition is true and something else if it is not.
Understanding the basics of if/else statements will allow you to write
more complex if/else ladder statments where multiple else statements can
be executed.
