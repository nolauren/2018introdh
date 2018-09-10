### Step 1: Download R

The next step is to download and install R for your computer (most of you should
already have done this). To do so, following the following link and proceed with
the prompts:

- [https://cran.r-project.org/](https://cran.r-project.org/)

Once downloaded, install the dmg or exe file as you would any software.


![](https://statsmaths.github.io/stat209-f18/assets/img/cran01.jpeg)


For macOS, just download the newest version of R:

![](https://statsmaths.github.io/stat209-f18/assets/img/cran02.jpeg)

For Windows, first select base:

![](https://statsmaths.github.io/stat209-f18/assets/img/cran03.jpeg)

And then download top newest version of R:

![](https://statsmaths.github.io/stat209-f18/assets/img/cran04.jpeg)

One you have the .pkg (macOS) or .exe (Windows) file, install this on your computer according to the default settings.

### Step 2: R Studio

The files we just downloaded are the core R language files doing all the hard work of processing data. 
Next, we’ll install a helpful GUI frontend that make calling R easier.

![](https://statsmaths.github.io/stat209-f18/assets/img/rstudio01.jpeg)

Scroll down to the DOWNLOAD RSTUDIO DESKTOP button and click on it.

![](https://statsmaths.github.io/stat209-f18/assets/img/rstudio02.jpeg)

Scroll down again to the Installers for Supported Platforms. The Windows link gives you an exe:

![](https://statsmaths.github.io/stat209-f18/assets/img/rstudio03.jpeg)


And the macOS link gives a dmg:
![](https://statsmaths.github.io/stat209-f18/assets/img/rstudio04.jpeg)

Now, install R or RStudio as you would any other program. It should link automatically to the version of R you just installed.

Mac users: make sure you drag the icon into the Applications folder.



### Step 3: Install R packages

Now, we need to install several add-ons to the R language. We can do this from
within R. Open the program. Then, copy and paste the following lines one by one
into the R terminal:

```{r}
install.packages("topicmodels")
install.packages("tidytext")
install.packages("dplyr")
install.packages("jsonlite")
```

It may ask you some questions and I'll help you answer those. Note that this may
take a few minutes as each of these packages requires other packages, none of 
which you have yet.

Notice that I don't have to run these lines on my machine. These only has to be
run once and then they are installed for good.
