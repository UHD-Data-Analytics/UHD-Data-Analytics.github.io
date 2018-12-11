---
title: "R Plot Function Basics"
description: "Overview of plotting in R and a few examples of plots"
collection: r
---

R Plot Function Basics
======================

### The Basics of the R Plot Function:

The most used plotting function in R programming is the plot() function.
It is a generic function, meaning, it has many methods which are called
according to the type of object passed to plot(). In the simplest case,
we can pass in a vector and we will get a scatter plot of magnitude vs
index. But generally, we pass in two vectors and a scatter plot of these
points are plotted.

For example, the command plot(c(1,2),c(3,5)) would plot the points (1,3)
and (2,5). Here is a more concrete example where we plot a sine function
form range -pi to pi.
```r
    x <- seq(-pi,pi,0.1)  #Here we ask R to create the data points we will be graphing
    plot(x, sin(x)) # here, we simply as R to graph our data
```

![](./figure-markdown_strict/unnamed-chunk-1-1.png)

### Adding Titles and Labeling Axes:

We can add a title to our plot with the parameter main. Similarly, xlab
and ylab can be used to label the x-axis and y-axis respectively.
```r
    plot(x, sin(x), main="The Sine Function", ylab="sin(x)")
```

![](./figure-markdown_strict/unnamed-chunk-2-1.png)

### Changing Color and Plot Type:

We can see above that the plot is of circular points and black in color.
This is the default color in R. However, we can change the “plot type”
(meaning the dots used to label our data points on x and y axis) with
the argument type. It accepts the following strings and has the given
effect: “p” - points “l” - lines “b” - both points and lines “c” - empty
points joined by lines “o” - overplotted points and lines “s” and “S” -
stair steps “h” - histogram-like vertical lines “n” - does not produce
any points or lines

Lets change our plot type to “l”, so that we see only lines and no
points.
```r
    plot(x, sin(x), main="The Sine Function", ylab="sin(x)", type="l")
```
![](./figure-markdown_strict/unnamed-chunk-3-1.png)

To take our graph a step further, we can define the color using “col”.
Lets add blue to our simple plot.
```r
    plot(x, sin(x), main="The Sine Function",ylab="sin(x)",type="l", col="blue")
```
![](./figure-markdown_strict/unnamed-chunk-4-1.png)

### Overlaying Plots Using legend() function

Calling plot() multiple times will have the effect of plotting the
current graph on the same window replacing the previous one. However,
sometimes we wish to overlay the plots in order to compare the results.
This is made possible with the functions lines() and points() to add
lines and points respectively, to the existing plot.

```r
    # the code below was put on different lines for visual purposes...
    plot(x, sin(x),
    main="Overlaying Graphs",
    ylab="",
    type="l",
    col="blue")
    lines(x,cos(x), col="red")
    legend("topleft",
    c("sin(x)","cos(x)"),
    fill=c("blue","red")
    )
```
![](./figure-markdown_strict/unnamed-chunk-5-1.png)
