---
title: "Loops in R"
description: "Overview on how to write loops in R"
collection: r
---


# Loops in R
================


In this example, we will explore writing a simple "For Loop"" in R. Suppose you want to do several printouts of the following form: The year is \[year\] where \[year\] is equal to 2010, 2011, up to 2015. You can do this as follows:

print(paste("The year is", 2010)) "The year is 2010" print(paste("The year is", 2011)) "The year is 2011" print(paste("The year is", 2012)) "The year is 2012" print(paste("The year is", 2013)) "The year is 2013" print(paste("The year is", 2014)) "The year is 2014" print(paste("The year is", 2015)) "The year is 2015"

While this may be fine for smaller jobs, you can see how this way would get very messy (very quickly) for larger jobs. Furthermore, This violates the DRY principle, known in every programming language: Don’t Repeat Yourself, at all cost. In this case, by making use of a "for loop"" in R, you can automate the repetitive part like so:

``` r
for (year in c(2010,2011,2012,2013,2014,2015)){
  print(paste("The year is", year))
}
```

    ## [1] "The year is 2010"
    ## [1] "The year is 2011"
    ## [1] "The year is 2012"
    ## [1] "The year is 2013"
    ## [1] "The year is 2014"
    ## [1] "The year is 2015"

See how we did that? By using a for loop you only need to write down your code chunk once (instead of six times). The for loop then runs the statement once for each provided value (the different years we provided) and sets the variable (year in this case) to that value. You can even simplify the code even more: c(2010,2011,2012,2013,2014,2015) can also be written as 2010:2015; this creates the exact same sequence:

``` r
for (year in 2010:2015){
  print(paste("The year is", year))
}
```

    ## [1] "The year is 2010"
    ## [1] "The year is 2011"
    ## [1] "The year is 2012"
    ## [1] "The year is 2013"
    ## [1] "The year is 2014"
    ## [1] "The year is 2015"

As a last note on the for loop in R: in this case we made use of the variable year; but in fact any variable could be used here. To simplify our code even more, we could have used i, a commonly-used variable in for loops that stands for index like this:

``` r
for (i in 2010:2015){
  print(paste("The year is", i))
}
```

    ## [1] "The year is 2010"
    ## [1] "The year is 2011"
    ## [1] "The year is 2012"
    ## [1] "The year is 2013"
    ## [1] "The year is 2014"
    ## [1] "The year is 2015"

Congratulations! You just created your first For Loop In R! In this short tutorial you got acquainted with the for loop in R. It helps you understand underlying principles, and when prototyping a loop solution is easy to code and read.