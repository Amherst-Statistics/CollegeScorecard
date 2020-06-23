# CollegeScorecard
Data from the DOE College Scorecard 

Install via:

`devtools::install_github("Amherst-Statistics/CollegeScorecard")`

then access via:

```
list.files(system.file("extdata", package = "CollegeScorecard"))
```

```
filename <- paste(system.file("extdata", package = "CollegeScorecard"), 
                  "MERGED2016_17_PP.csv.bz2", sep = "/")
cs2016 <- readr::read_csv(filename)
```

Last updated June 23, 2020 using data from 2018-2019.
