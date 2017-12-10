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

Install the R package from git first. Available in both zip file and git file with name "package-."
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

## Running the tests
After having the package running, type the following in console
```
comparisonPlot(2,'wmt','aapl')
```
with code
```
apple<-create.data("aapl")[[2]]
variables<-create.data("aapl")[[3]][-1]
walmart<-create.data("wmt")[[2]]
```

### Break down into end to end tests

In the main comparison function,

```
comparisonPlot <- function(x,AAA,BBB)
```
  #AAA and BBB will be of form input$VAR, which will be a read in textInput() from ui
  #AAA and BBB must be character strings. the input syntax must acheive this

### And coding style tests

Explain what these tests test and why

```
Give an example
```

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
* etc
