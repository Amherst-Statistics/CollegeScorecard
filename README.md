
![R-CMD-check](https://github.com/Amherst-Statistics/CollegeScorecard/workflows/R-CMD-check/badge.svg)
![Render
README](https://github.com/Amherst-Statistics/CollegeScorecard/workflows/Render%20README/badge.svg)

# CollegeScorecard

Collated data from the United States Department of Education (DOE)
College Scorecard project

### Installation

`devtools::install_github("Amherst-Statistics/CollegeScorecard")`

### List files

``` r
list.files(system.file("extdata", package = "CollegeScorecard"))
```

    ##  [1] "Crosswalks.zip"                            
    ##  [2] "CW2000.xlsx"                               
    ##  [3] "CW2001.xlsx"                               
    ##  [4] "CW2002.xlsx"                               
    ##  [5] "CW2003.xlsx"                               
    ##  [6] "CW2004.xlsx"                               
    ##  [7] "CW2005.xlsx"                               
    ##  [8] "CW2006.xlsx"                               
    ##  [9] "CW2007.xlsx"                               
    ## [10] "CW2008.xlsx"                               
    ## [11] "CW2009.xlsx"                               
    ## [12] "CW2010.xlsx"                               
    ## [13] "CW2011.xlsx"                               
    ## [14] "CW2012.xlsx"                               
    ## [15] "CW2013.xlsx"                               
    ## [16] "CW2014.xlsx"                               
    ## [17] "CW2015.xlsx"                               
    ## [18] "CW2016.xlsx"                               
    ## [19] "CW2017.xlsx"                               
    ## [20] "CW2018.xlsx"                               
    ## [21] "CW2019.xlsx"                               
    ## [22] "CW2020.xlsx"                               
    ## [23] "CW2021.csv"                                
    ## [24] "CW2021.xlsx"                               
    ## [25] "data.yaml"                                 
    ## [26] "FieldOfStudyData1415_1516_PP.csv.bz2"      
    ## [27] "FieldOfStudyData1516_1617_PP.csv.bz2"      
    ## [28] "FieldOfStudyData1718_1819_PP.csv.bz2"      
    ## [29] "FieldOfStudyData1819_1920_PP.csv.bz2"      
    ## [30] "MERGED1996_97_PP.csv.bz2"                  
    ## [31] "MERGED1997_98_PP.csv.bz2"                  
    ## [32] "MERGED1998_99_PP.csv.bz2"                  
    ## [33] "MERGED1999_00_PP.csv.bz2"                  
    ## [34] "MERGED2000_01_PP.csv.bz2"                  
    ## [35] "MERGED2001_02_PP.csv.bz2"                  
    ## [36] "MERGED2002_03_PP.csv.bz2"                  
    ## [37] "MERGED2003_04_PP.csv.bz2"                  
    ## [38] "MERGED2004_05_PP.csv.bz2"                  
    ## [39] "MERGED2005_06_PP.csv.bz2"                  
    ## [40] "MERGED2006_07_PP.csv.bz2"                  
    ## [41] "MERGED2007_08_PP.csv.bz2"                  
    ## [42] "MERGED2008_09_PP.csv.bz2"                  
    ## [43] "MERGED2009_10_PP.csv.bz2"                  
    ## [44] "MERGED2010_11_PP.csv.bz2"                  
    ## [45] "MERGED2011_12_PP.csv.bz2"                  
    ## [46] "MERGED2012_13_PP.csv.bz2"                  
    ## [47] "MERGED2013_14_PP.csv.bz2"                  
    ## [48] "MERGED2014_15_PP.csv.bz2"                  
    ## [49] "MERGED2015_16_PP.csv.bz2"                  
    ## [50] "MERGED2016_17_PP.csv.bz2"                  
    ## [51] "MERGED2017_18_PP.csv.bz2"                  
    ## [52] "MERGED2018_19_PP.csv.bz2"                  
    ## [53] "MERGED2019_20_PP.csv.bz2"                  
    ## [54] "MERGED2020_21_PP.csv.bz2"                  
    ## [55] "MERGED2021_22_PP.csv.bz2"                  
    ## [56] "Most-Recent-Cohorts-Field-of-Study.csv.bz2"
    ## [57] "Most-Recent-Cohorts-Institution.csv.bz2"

### Example from 2016

``` r
filename <- paste(system.file("extdata", package = "CollegeScorecard"), 
                  "MERGED2016_17_PP.csv.bz2", sep = "/")
cs2016 <- readr::read_csv(filename)
head(cs2016$MALE_WDRAW_ORIG_YR4_RT)
```

    ## [1] "0.371237458194" "0.238558909445" "0.620253164557" "0.233564013841"
    ## [5] "0.425641025641" "0.148696985181"

``` r
summary(readr::parse_number(cs2016$MALE_WDRAW_ORIG_YR4_RT))
```

    ##    Min. 1st Qu.  Median    Mean 3rd Qu.    Max.    NA's 
    ##   0.032   0.222   0.354   0.357   0.496   0.814    3245

Last updated Sat Aug 26 13:25:47 2023 GMT incorporating data from
2021-2022.
