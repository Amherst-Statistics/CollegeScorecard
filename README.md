
![R-CMD-check](https://github.com/Amherst-Statistics/CollegeScorecard/workflows/R-CMD-check/badge.svg)
![Render
README](https://github.com/Amherst-Statistics/CollegeScorecard/workflows/Render%20README/badge.svg)

# CollegeScorecard

Data from the US Department of Education College Scorecard project

### Installation

`devtools::install_github("Amherst-Statistics/CollegeScorecard")`

### List files

``` r
list.files(system.file("extdata", package = "CollegeScorecard"))
```

    ##  [1] "CW2000.xlsx"                      "CW2001.xlsx"                     
    ##  [3] "CW2002.xlsx"                      "CW2003.xlsx"                     
    ##  [5] "CW2004.xlsx"                      "CW2005.xlsx"                     
    ##  [7] "CW2006.xlsx"                      "CW2007.xlsx"                     
    ##  [9] "CW2008.xlsx"                      "CW2009.xlsx"                     
    ## [11] "CW2010.xlsx"                      "CW2011.xlsx"                     
    ## [13] "CW2012.xlsx"                      "CW2013.xlsx"                     
    ## [15] "CW2014.xlsx"                      "CW2015.xlsx"                     
    ## [17] "CW2016.xlsx"                      "CW2017.xlsx"                     
    ## [19] "CW2018.xlsx"                      "data.yaml"                       
    ## [21] "FieldOfStudyData1415_1516_PP.csv" "FieldOfStudyData1516_1617_PP.csv"
    ## [23] "MERGED1996_97_PP.csv.bz2"         "MERGED1997_98_PP.csv.bz2"        
    ## [25] "MERGED1998_99_PP.csv.bz2"         "MERGED1999_00_PP.csv.bz2"        
    ## [27] "MERGED2000_01_PP.csv.bz2"         "MERGED2001_02_PP.csv.bz2"        
    ## [29] "MERGED2002_03_PP.csv.bz2"         "MERGED2003_04_PP.csv.bz2"        
    ## [31] "MERGED2004_05_PP.csv.bz2"         "MERGED2005_06_PP.csv.bz2"        
    ## [33] "MERGED2006_07_PP.csv.bz2"         "MERGED2007_08_PP.csv.bz2"        
    ## [35] "MERGED2008_09_PP.csv.bz2"         "MERGED2009_10_PP.csv.bz2"        
    ## [37] "MERGED2010_11_PP.csv.bz2"         "MERGED2011_12_PP.csv.bz2"        
    ## [39] "MERGED2012_13_PP.csv.bz2"         "MERGED2013_14_PP.csv.bz2"        
    ## [41] "MERGED2014_15_PP.csv.bz2"         "MERGED2015_16_PP.csv.bz2"        
    ## [43] "MERGED2016_17_PP.csv.bz2"         "MERGED2017_18_PP.csv.bz2"        
    ## [45] "MERGED2018_19_PP.csv.bz2"

### Example from 2016

``` r
filename <- paste(system.file("extdata", package = "CollegeScorecard"), 
                  "MERGED2016_17_PP.csv.bz2", sep = "/")
cs2016 <- readr::read_csv(filename)
summary(cs2016$MALE_WDRAW_ORIG_YR4_RT)
```

    ##    Length     Class      Mode 
    ##      7238 character character

``` r
summary(readr::parse_number(cs2016$MALE_WDRAW_ORIG_YR4_RT))
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
    ##   0.032   0.222   0.354   0.357   0.496   0.814    3245

Last updated Wed Jun 24 00:21:36 2020 using data from 2018-2019.
