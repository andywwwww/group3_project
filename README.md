# stat297projectgroup3

The users would be able to compare data from two different companies using comparisons from line graphs and from side by side tables. This visualization would help users to make decisions such as what the overall trends of different aspects of the company’s finances are. +This can help them to make decisions such as choosing which company you’d want to buy stocks from.

## Getting Started

Our Project consists of a R package, a Shiny App that works with financial statment and compare two companies statement.

## Data

Pull data off from the website Marketwatch  using selectorGadget and the rvest package.
clean up the data just so R could read it to the comparison function using package “dplyr” and "rvest"
![A couple sample data points that the user could choose from.](http://personal.psu.edu/jxw505/OTHERS/data.png)
(The link sometimes is iffy. Image is available at http://personal.psu.edu/jxw505/OTHERS/data.png)

### Prerequisites

Make sure to have the following packages:

dplyr
plotly
stringi
rvest

If not, run the following command in console:
```
install.packages(dplyr)
install.packages(plotly)
install.packages(stringi)
install.packages(rvest)
```

### Installing

Install the R package from git first, this will require an installation of the package "devtools". Available in both zip file and git file with name "package-."
For zip, unzip it locally and run command

```
devtools::document()
```
and go to menu on the right to do
```
install and build.
```

For git files, copy all files with name "package-" into one directory and repeat the same command with zip.

![If the package works, it should look like this.](http://personal.psu.edu/jxw505/OTHERS/test.PNG)
(The link sometimes is iffy. Image is available at http://personal.psu.edu/jxw505/OTHERS/test.PNG)

## Running in the console:

example 1:
After having the package running, type the following in console,
```
comparisonPlot(2,'wmt','aapl')
```
This will output a plot with the walmart and apple's "Cash Only" (asset) dollar values over the past 5 years.


example 2:
Internally, this function above (before cleaning the data sets down to the prompted variable and graphing) will effectively do the following,
```
apple<-create.data("aapl")[[2]]
variables<-create.data("aapl")[[3]][+1] 
walmart<-create.data("wmt")[[2]] 

#or, to refer to the syntax used, 
#AA<-create.data("AAA")[[2]]
#BB<-create.data("BBB")[[2]]
#variables<-create.data("AAA")[[3]][+1]
```

example 3:
This comparisonPlot() function uses another function in our package, the create.data() function.
This function takes one argument, the stock ticker, which must be a character string. It returns a list of 3 objects. Giving,
```
#all of these will return TRUE
class(create.data('wmt')[[1]])=="data.frame"
class(create.data('wmt')[[2]])=="matrix"
#we use the matrix to create the plots in our comparison function because it retains the row names given to it, and graphing these
#row names doesnt introduce any problems
```



## Running in Shiny:
Internally, heres how our functions work in shiny.


In the main comparison function,
```
comparisonPlot <- function(x,AAA,BBB)
```
  #AAA and BBB will be of form input$VAR, which will be a read in textInput() from ui
  #AAA and BBB must be character strings. the input syntax must acheive this
  #Furthermore, the AAA and BBB variables will be stock tickers, and this function will only work if these stock tickers (and their
  #corresponding companies' balance sheets) are on the website from which we import this data, Marketwatch.com 
  #




## Deployment

Add additional notes about how to deploy this on a live system


## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Ryan Voyack** - *Initial work* - (https://github.com/ryanvoyack)
* **Marshall Malino** - *Initial work* - (https://github.com/spearman666)
* **Andrea Wan** - *Initial work* - (https://github.com/andywwwww)

See also the list of [contributors](https://github.com/andywwwww/group3_project/graphs/contributors) who participated in this project.

## License

This project is licensed under General License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Inspiration
from Justin Lee(https://github.com/munsheet)
from Stéphane Guerrier(https://github.com/stephaneguerrier)
