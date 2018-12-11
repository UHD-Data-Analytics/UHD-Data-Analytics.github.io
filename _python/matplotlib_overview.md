---
title: "Working with Matplotlib"
description: "Guide on using Matplotlib in Python including a few examples of plots"
collection: python
---

Working with Matplotlib
=======================

Matplotlib is probably the single most used Python package for
2D-graphics. It provides a very quick way to visualize data from Python
while also producing publication-quality figures in many formats.

### IPython and the pylab mode

IPython is an enhanced interactive Python shell that has lots of
interesting features including named inputs and outputs, access to shell
commands, improved debugging and many more. When we start it with the
command line argument -pylab (–pylab since IPython version 0.12), it
allows interactive matplotlib sessions that have Matlab/Mathematica-like
functionality.

### pyplot

pyplot provides a convenient interface to the matplotlib object-oriented
plotting library. It is modeled closely after Matlab(TM). Therefore, the
majority of plotting commands in pyplot have Matlab(TM) analogs with
similar arguments. Important commands are explained with interactive
examples.

#### SIMPLE PLOT


n this example, we want to draw the cosine and sine functions on the
same plot. We will first start with the default settings and enrich the
figure step by step to make it nicer. First step is to get the data for
the sine and cosine functions:

```python
    import numpy as np
    X = np.linspace(-np.pi, np.pi, 256,endpoint=True)
    C,S = np.cos(X), np.sin(X)
```

X is now a numpy array with 256 values ranging from -pi to pi
(included). C is the cosine (256 values) and S is the sine (256 values).

USING DEFAULTS Matplotlib comes with a set of default settings. We can
control the defaults of almost every property in matplotlib: figure size
and dpi, line width, color and style, axes, axis and grid properties,
text and font properties and so on. While matplotlib defaults are rather
good in most cases, you may want to modify some properties for specific
cases.

```python
    import numpy as np
    import matplotlib.pyplot as plt
    X = np.linspace(-np.pi, np.pi, 256, endpoint=True)
    C,S = np.cos(X), np.sin(X)
    plt.plot(X,C)
    plt.plot(X,S)
    plt.show()
```

![](./figure-markdown_strict/unnamed-chunk-2-1.png)

The plot() function plots our cosine and sine. The show() function shows
us our graphic.

### DEFAULTS OF Matplotlib

In the figure below we have listed all the figure settings that
influence the appearance of the plot. The settings have been explicitly
set to their default values.

```python
    # Imports
    import numpy as np
    import matplotlib.pyplot as plt
    # Create a new figure of size 8x6 points, using 100 dots per inch
    plt.figure(figsize=(8,6), dpi=80)
    # Create a new subplot from a grid of 1x1
    plt.subplot(111)
    X = np.linspace(-np.pi, np.pi, 256,endpoint=True)
    C,S = np.cos(X), np.sin(X)
    # Plot cosine using blue color with a continuous line of width 1 (pixels)
    plt.plot(X, C, color="blue", linewidth=1.0, linestyle="-")
    # Plot sine using green color with a continuous line of width 1 (pixels)
    plt.plot(X, S, color="green", linewidth=1.0, linestyle="-")
    # Set x limits
    plt.xlim(-4.0,4.0)
    # Set x ticks
    plt.xticks(np.linspace(-4,4,9,endpoint=True))
    # Set y limits
    plt.ylim(-1.0,1.0)
    # Set y ticks
    plt.yticks(np.linspace(-1,1,5,endpoint=True))
    # Save figure using 72 dots per inch
    # savefig("../figures/exercice_2.png",dpi=72)
    # Show result on screen
    plt.show()
```

![](./figure-markdown_strict/unnamed-chunk-3-1.png)

### CHANGING THE COLORS AND LINE WIDTHS

First step is to change the colors of cosine(blue) and sine(red). We
will also make their lines thicker and the figure size more horizontal.

```python
    plt.figure(figsize=(10,6), dpi=80)
    plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-")
    plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-")
```

### SETTING LIMITS

The current limits of the figurea are a bit too tight and we want to
make some space in order to clearly see all data points.

```python
    plt.xlim(X.min()*1.1, X.max()*1.1)
    plt.ylim(C.min()*1.1, C.max()*1.1)
```
### SETTING TICKS

Current ticks are not ideal because they do not show the interesting
values (+/-pi, +/-(pi/2)) for sine and cosine. We’ll change them such
that they show only these values.

```python
    plt.xticks( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi])
    plt.yticks([-1, 0, +1])
```

### SETTING TICK LABELS

Ticks are now properly placed but their labels are not very explicit. We
could assume that 3.142 is pi but it would be better to make it
explicit. When we set tick values, we can also provide a corresponding
label in the second argument list. Note that we’ll use latex to allow
for nice rendering of the label.

```python
    plt.xticks([-np.pi, -np.pi/2, 0, np.pi/2, np.pi],
           [r'$-\pi$', r'$-\pi/2$', r'$0$', r'$+\pi/2$', r'$+\pi$'])
    plt.yticks([-1, 0, +1],
           [r'$-1$', r'$0$', r'$+1$'])
```

### MOVING SPINES

Spines are the lines connecting the axis tick marks and noting the
boundaries of the data area. They can be placed at arbitrary positions
and until now, they were on the border of the axis. We’ll change that
since we want to have them in the middle. Since there are four of them
(top/bottom/left/right), we’ll discard the top and right by setting
their color to none and we’ll move the bottom and left ones to
coordinate 0 in data space coordinates.

```python
    ax = plt.gca()
    ax.spines['right'].set_color('none')
    ax.spines['top'].set_color('none')
    ax.xaxis.set_ticks_position('bottom')
    ax.spines['bottom'].set_position(('data',0))
    ax.yaxis.set_ticks_position('left')
    ax.spines['left'].set_position(('data',0))
```

### ADDING A LEGEND

Let’s add a legend in the upper left corner. This only requires adding
the keyword argument label (that will be used in the legend box) to the
plot commands.

```python
    plt.plot(X, C, color="blue", linewidth=2.5, linestyle="-", label="cosine")
    plt.plot(X, S, color="red",  linewidth=2.5, linestyle="-", label="sine")
    plt.legend(loc='upper left', frameon=False)
```

### ANNOTATE SOME POINTS

To annotate some interesting points we use the annotate command. We
chose the 2pi/3 value and we want to annotate both sine and cosine. We
will first draw a marker on the curve as well as a straight dotted line.
The, we will use the annotate command to display some text with an
arrow.

```python
    t = 2*np.pi/3
    plt.plot([t,t],[0,np.cos(t)], color ='blue', linewidth=1.5, linestyle="--")
    plt.scatter([t,],[np.cos(t),], 50, color ='blue')
    plt.annotate(r'$\sin(\frac{2\pi}{3})=\frac{\sqrt{3}}{2}$',
                 xy=(t, np.sin(t)), xycoords='data',
                 xytext=(+10, +30), textcoords='offset points', fontsize=16,
                 arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))
    plt.plot([t,t],[0,np.sin(t)], color ='red', linewidth=1.5, linestyle="--")
    plt.scatter([t,],[np.sin(t),], 50, color ='red')
    plt.annotate(r'$\cos(\frac{2\pi}{3})=-\frac{1}{2}$',
                 xy=(t, np.cos(t)), xycoords='data',
                 xytext=(-90, -50), textcoords='offset points', fontsize=16,
                 arrowprops=dict(arrowstyle="->", connectionstyle="arc3,rad=.2"))
```

### FEW MORE MODIFICATIONS

The tick labels are now hardly visible because of the blue and red
lines. We can make them bigger and we can also adjust their properties
such that they’ll be rendered on a semi-transparent white background.
This will allow us to see both the data and the labels.

```python
    for label in ax.get_xticklabels() + ax.get_yticklabels():
        label.set_fontsize(16)
        label.set_bbox(dict(facecolor='white', edgecolor='None', alpha=0.65 ))
```