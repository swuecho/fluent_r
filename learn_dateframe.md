data frames
================

creating data frame
-------------------

``` r
kids <- c("Jack", "Jill")
ages <- c(12, 10)
d <- data.frame(kids, ages, stringsAsFactors = FALSE)
d
```

    ##   kids ages
    ## 1 Jack   12
    ## 2 Jill   10

``` r
str(d)
```

    ## 'data.frame':    2 obs. of  2 variables:
    ##  $ kids: chr  "Jack" "Jill"
    ##  $ ages: num  12 10

accessing dataframe
-------------------

``` r
d[[1]]
```

    ## [1] "Jack" "Jill"

``` r
d$kids
```

    ## [1] "Jack" "Jill"

``` r
d[,1]
```

    ## [1] "Jack" "Jill"
