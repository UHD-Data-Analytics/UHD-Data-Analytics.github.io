---
title: "Introduction to Julia"
description: "Quick Overview on Basic Julia functions"
collection: julia
---

# Introduction to Julia

This is curated from lecture notes on quantecon.org.

### Using Packages

```julia
using LinearAlgebra, Statistics, Compat
```

### Plotting in Julia

```julia
using Plots
gr(fmt=:png) # setting for easier display in jupyter notebooks

n = 100
ϵ = randn(n)
plot(1:n, ϵ)
```

![](./plot1.png)

### Arrays:

```julia
ϵ[1:5]
```
```
5-element Array{Float64,1}:
 -0.5563748011324748 
  1.0086062002662834 
 -0.25949551453379965
 -1.0171126481937203 
 -1.0206506194582479 
```

```julia
M = [1 2; 3.5 4];
typeof(M)
```
```
Array{Float64}
```

### For Loops

Using the counter method:

```julia

n = 100
ϵ = zeros(n)
for i in 1:n
    ϵ[i] = randn()
end
```

Using the index of an array:

```julia
n = 100
ϵ = zeros(n)
for i in eachindex(ϵ)
    ϵ[i] = randn()
end
```

Looping directly over the array:

```julia
ϵ_sum = 0.0 # careful to use 0.0 here, instead of 0
m = 5
for ϵ_val in ϵ[1:m]
    ϵ_sum = ϵ_sum + ϵ_val
end
ϵ_mean = ϵ_sum / m
```

### User defined Functions

```julia
function generatedata(n)
    ϵ = zeros(n)
    for i in eachindex(ϵ)
        ϵ[i] = (randn())^2 # squaring the result
    end
    return ϵ
end

data = generatedata(10)
plot(data)
```
![](./plot2.png)

#### One line function

```julia
# direct solution with broadcasting, and small user-defined function
n = 100
f(x) = x^2

x = randn(n)
plot(f.(x), label="x^2")
plot!(x, label="x") # layer on the same plot
```

![](./plot3.png)
