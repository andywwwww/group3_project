# 
+
#A R package 
+Pull data off from the website Marketwatch  using selectorGadget and the rvest package.
+clean up the data just so R could read it to the comparison function using package “dplyr” and "rvest"
+
+
+##A Shiny App
+##Financial statement data and comparison
+

# stat297projectgroup3

The users would be able to compare data from two different companies using comparisons from line graphs and from side by side tables. This visualization would help users to make decisions such as what the overall trends of different aspects of the company’s finances are. +This can help them to make decisions such as choosing which company you’d want to buy stocks from.

## Getting Started

  ""  "" 

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

Install the R package from git first. Avalible in both zip file and git file with name "package-."
For zip, unzip it locally and run command

```
devtools::document()
```
and go to menu on the right to do
```
install and build.
```

For git files, copy all files with name "package-" into one directory and repeat the same command with zip.

![Caption for the picture.](/path/to/image.png)

End with an example of getting some data out of the system or using it for a little demo

## Running the tests

Explain how to run the automated tests for this system

### Break down into end to end tests

Explain what these tests test and why

```
Give an example
```

### And coding style tests

Explain what these tests test and why

```
Give an example
```

## Deployment

Add additional notes about how to deploy this on a live system

## Built With

* [Dropwizard](http://www.dropwizard.io/1.0.2/docs/) - The web framework used
* [Maven](https://maven.apache.org/) - Dependency Management
* [ROME](https://rometools.github.io/rome/) - Used to generate RSS Feeds

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Hat tip to anyone who's code was used
* Inspiration
* etc
