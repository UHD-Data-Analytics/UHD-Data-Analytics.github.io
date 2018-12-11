---
layout: default
---

# How to contribute to this website:

* * *

You are free to to request the website holder to add your own content to this site. Please follow these instructions so your content will meet the requirements to post correctly:

### Exporting from jupyter or Rstudio

To export from jupyter, you can just select the download as markdown option under File:

![](assets/contributions/jupyterexport.png)

To knit your .rmd file, just make sure you have the front matter have:
```
---
output: md_document
---
```

For your page itself, make sure the exported markdown has the following front matter at the top of the page like so:


![](assets/contributions/frontmatter.png)

the title, description, and collection are all VERY IMPORTANT so that the page can pick up the contents properly and add links to the page.

It is also suggested to check your code outputs, and potentially wrap them in the triple accepts and then add the language it's written in like this:

````
```r
# here is some r code.
```
````

All of your image outputs should be in a folder labeled the same as your markdown file (try not to use any spaces for either).

Then you can relabel the markdown embedded images like so:

```
![](assets/contributions/imagename.png)
```

This way the `.` will pick up the folder automatically if it's labeled the same as the markdown file.

Now with a github account you can fork the website to your own github:

![](assets/contributions/forkme.png)

Then you can navigate to the folder you want to add your content, and click upload file:

![](assets/contributions/uploadfile.png)

and then drag the files into the box and commit the changes to your local forked version of the website

![](assets/contributions/dragfile.png)

Now you are ready to make a pull request. First you click the pull request button on the left here:

![](assets/contributions/pullrequest.png)

Then we can make sure it's able to merge and then create the pull request:

![](assets/contributions/pullrequest2.png)

Add some comments, submit, and now the pull request is active!

![](assets/contributions/pullrequest3.png)


### Accepting a pull request

The site master can now check your pull request, by clicking on the pull request title:

![](assets/contributions/acceptrequest1.png)

Check to see any conflicts, and if they feel comfortable with the content, they can merge the pull request:

![](assets/contributions/acceptrequest2.png)

And a full merged request looks like this:

![](assets/contributions/acceptrequest3.png)


If your front matter was displayed correctly, your content will be added as a link to the site!
