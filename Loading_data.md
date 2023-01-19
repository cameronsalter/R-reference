Loading data
================
Cameron Salter
16/01/2023

# Exploring directories

``` r
getwd()
```

    ## [1] "D:/MY FILES/Projects/Public/R-reference"

``` r
cat("\n")
```

``` r
dir() # List files in directory. Equivalently: list.files()
```

    ## [1] "Data"              "docs"              "Loading_data.html"
    ## [4] "Loading_data.Rmd"  "README.md"         "Test"

``` r
# Setting a dir
setwd("Test") # both relative and abs. paths work
getwd()
```

    ## [1] "D:/MY FILES/Projects/Public/R-reference/Test"

``` r
setwd("..") # Move up dir. tree
getwd()
```

    ## [1] "D:/MY FILES/Projects/Public"

# Loading in data

<https://readr.tidyverse.org/#cheatsheet>

``` r
library(readr) # readr - load in tabulated data
library(readxl) # readxl - load in xlsx files 
```

``` r
data_csv <- readr::read_csv('Data/dummy_data_csv.csv') # also read_tsv(), read_delim(), ...
```

    ## Rows: 4 Columns: 3
    ## ── Column specification ────────────────────────────────────────────────────────
    ## Delimiter: ","
    ## dbl (3): x, y, z
    ## 
    ## ℹ Use `spec()` to retrieve the full column specification for this data.
    ## ℹ Specify the column types or set `show_col_types = FALSE` to quiet this message.

``` r
data_csv
```

    ## # A tibble: 4 × 3
    ##       x     y     z
    ##   <dbl> <dbl> <dbl>
    ## 1     1     1     2
    ## 2     1     2     2
    ## 3     2     2     2
    ## 4     2     2     3

``` r
data_excel <- readxl::read_excel('Data/dummy_data_excel.xlsx') 
data_excel
```

    ## # A tibble: 4 × 3
    ##       x     y     z
    ##   <dbl> <dbl> <dbl>
    ## 1     1     1     2
    ## 2     1     2     2
    ## 3     2     2     2
    ## 4     2     2     3
