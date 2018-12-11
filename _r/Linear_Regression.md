---
title: "Linear Regression in R"
description: "Overview of how to use linear regression in R"
collection: r
---

# Linear Regression Example in R
==============================

In data analytics we come across the term “Regression” very frequently.
Before we continue to focus topic i.e. “Linear Regression” lets first
know what we mean by Regression. Regression is a statistical way to
establish a relationship between a dependent variable and a set of
independent variable(s). e.g., if we say that

Age = 5 + Height \* 10 + Weight \* 13

Here we are establishing a relationship between Height & Weight of a
person with his/ Her Age. This is a very basic example of Regression.

### Simple Linear Regression

#### Introduction

Least Square “Linear Regression” is a statistical method to regress the
data with dependent variable having continuous values whereas
independent variables can have either continuous or categorical values.
In other words “Linear Regression” is a method to predict dependent
variable (Y) based on values of independent variables (X). It can be
used for the cases where we want to predict some continuous quantity.
E.g., Predicting traffic in a retail store, predicting a user’s dwell
time or number of pages visited on Dezyre.com etc.

#### Prerequisites

To start with Linear Regression, you must be aware of a few basic
concepts of statistics:

-   Correlation (r) – Explains the relationship between two variables,
    possible values -1 to +1
-   Variance (σ2)– Measure of spread in your data
-   Standard Deviation (σ) – Measure of spread in your data (Square root
    of Variance)

### Normal distribution

-   Residual (error term) – {Actual value – Predicted value}

#### Assumptions of Linear Regression:

Not a single size fits or all, the same is true for Linear Regression
as well. In order to fit a linear regression line data should satisfy
few basic but important assumptions. If your data doesn’t follow the
assumptions, your results may be wrong as well as misleading.

1.  Linearity & Additive: There should be a linear relationship between
    dependent and independent variables and the impact of change in
    independent variable values should have additive impact on dependent
    variable.
2.  Normality of error distribution: Distribution of differences between
    Actual & Predicted values (Residuals) should be normally
    distributed.
3.  Homoscedasticity: Variance of errors should be constant versus,

-   Time
-   The predictions
-   Independent variable values

1.  Statistical independence of errors: The error terms (residuals)
    should not have any correlation among themselves. E.g., In case of
    time series data there shouldn’t be any correlation between
    consecutive error terms

There are several types of linear regression analyses available to
researchers.

##### A. Simple linear regression
- 1 dependent variable (interval or ratio)
- 1 independent variable (interval or ratio or dichotomous)

##### B. Multiple linear regression

-   1 dependent variable (interval or ratio)
-   2+ independent variables (interval or ratio or dichotomous)

##### C. Logistic regression

-   1 dependent variable (dichotomous)
-   2+ independent variable(s) (interval or ratio or dichotomous)

##### D. Ordinal regression

-   1 dependent variable (ordinal)
-   1+ independent variable(s) (nominal or dichotomous)

##### E.Multinominal regression

-   1 dependent variable (nominal)
-   1+ independent variable(s) (interval or ratio or dichotomous)

##### F. Discriminant analysis

-   1 dependent variable (nominal)
-   1+ independent variable(s) (interval or ratio)

------------------------------------------------------------------------

When selecting the model for the analysis, an important consideration is
model fitting. Adding independent variables to a linear regression model
will always increase the explained variance of the model (typically
expressed as R²). However, overfitting can occur by adding too many
variables to the model, which reduces model generalizability. Occam’s
razor describes the problem extremely well – a simple model is usually
preferable to a more complex model. Statistically, if a model includes a
large number of variables, some of the variables will be statistically
significant due to chance alone.
