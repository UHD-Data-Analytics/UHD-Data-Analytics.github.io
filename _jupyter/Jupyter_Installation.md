---
title: "Jupyter Installation"
description: "Quick guide on how to install the Jupyter environment"
collection: jupyter
---

Jupyter Installation
====================

#### Step 0: The browser

Step “zero” consists in installing a modern standard-compliant browser.
Either Mozilla Firefox or Google Chrome will work well. Try to avoid MS
Explorer.

#### Step 1: Installation

The easiest way to install the Jupyter Notebook App is installing a
scientific python distribution which also includes scientific python
packages. The most common distribution is called Anaconda:

Download Anaconda Distribution, Python 3, 64 bits.
<https://www.anaconda.com/download/> Install it using the default
settings for a single user.

#### Step 2: Launching Jupyter Notebook App

The Jupyter Notebook App can be launched by clicking on the Jupyter
Notebook icon installed by Anaconda in the start menu (Windows) or by
typing in a terminal (cmd on Windows):

`jupyter notebook`

This will launch a new browser window (or a new tab) showing the
Notebook Dashboard, a control panel that allows (among other things) to
select which notebook to open.

#### Quickstart Guide

When started, the Jupyter Notebook App can access only files within its
start-up folder (including any sub-folder). No configuration is
necessary if you place your notebooks in your home folder or subfolders.
Otherwise, you need to choose a Jupyter Notebook App start-up folder
which will contain all the notebooks.

![Homepage](./homepage.png)

See below for platform-specific instructions on how to start Jupyter
Notebook App in a specific folder.

#### Change Jupyter Notebook startup folder (Windows)

Copy the Jupyter Notebook launcher from the menu to the desktop. Right
click on the new launcher and change the Target field, change
%USERPROFILE% to the full path of the folder which will contain all the
notebooks.

Double-click on the Jupyter Notebook desktop launcher (icon shows
\[IPy\]) to start the Jupyter Notebook App. The notebook interface will
appear in a new browser window or tab. A secondary terminal window (used
only for error logging and for shut down) will be also opened.

#### Change Jupyter Notebook startup folder (Mac OS)

To launch Jupyter Notebook App:

Click on spotlight, type terminal to open a terminal window. Enter the
startup folder by typing cd /some\_folder\_name. Type jupyter notebook
to launch the Jupyter Notebook App The notebook interface will appear in
a new browser window or tab.

#### Shut down the Jupyter Notebook App

Closing the browser (or the tab) will not close the Jupyter Notebook
App. To completely shut it down you need to close the associated
terminal.

In more detail, the Jupyter Notebook App is a server that appears in
your browser at a default address (<http://localhost:8888>). Closing the
browser will not shut down the server. You can reopen the previous
address and the Jupyter Notebook App will be redisplayed.

You can run many copies of the Jupyter Notebook App and they will show
up at a similar address (only the number after “:”, which is the port,
will increment for each new copy). Since with a single Jupyter Notebook
App you can already open many notebooks, we do not recommend running
multiple copies of Jupyter Notebook App.

#### Close a notebook: kernel shut down

When a notebook is opened, its “computational engine” (called the
kernel) is automatically started. Closing the notebook browser tab, will
not shut down the kernel, instead the kernel will keep running until is
explicitly shut down.

To shut down a kernel, go to the associated notebook and click on menu
File -&gt; Close and Halt. Alternatively, the Notebook Dashboard has a
tab named Running that shows all the running notebooks (i.e. kernels)
and allows shutting them down (by clicking on a Shutdown button).

### Executing a notebook

Download the notebook you want to execute and put it in your notebook
folder (or a sub-folder of it).

Then follow these steps:

#### Launch the Jupyter Notebook App (see previous section).

-   In the Notebook Dashboard navigate to find the notebook: clicking on
    its name will open it in a new browser tab.
-   Click on the menu Help -&gt; User Interface Tour for an overview of
    the Jupyter Notebook App user interface.
-   You can run the notebook document step-by-step (one cell a time) by
    pressing shift + enter.
-   You can run the whole notebook in a single step by clicking on the
    menu Cell -&gt; Run All.
-   To restart the kernel (i.e. the computational engine), click on the
    menu Kernel -&gt; Restart. This can be useful to start over a
    computation from scratch (e.g. variables are deleted, open files are
    closed, etc.).
