str\_reverse\_bench
================
Hao
November 8, 2016

``` r
reverse_str_r <- function(str) {
    chars <- strsplit(str, "")[[1]]
    return(paste(rev(chars), collapse=''))
}
```

``` r
library(microbenchmark)
library(echo)
```

``` r
str <- "abcdefgh"
str <-paste(replicate(2,str), collapse = "")
microbenchmark(
  reverse_str_r(str), str_reverse(str)
)
```

    ## Unit: microseconds
    ##                expr    min      lq     mean  median      uq    max neval
    ##  reverse_str_r(str) 10.464 11.5845 13.18125 12.3465 14.0985 42.484   100
    ##    str_reverse(str)  3.661  3.9270  6.39678  5.1255  6.2725 93.247   100
