list and hash
================

``` r
library(hash)
```

    ## hash-2.2.6 provided by Decision Patterns

``` r
h <- hash( keys=letters, values=1:26 )
h <- hash( letters, 1:26)
h$a
```

    ## [1] 1

``` r
h$a <- 5
h$a
```

    ## [1] 5

``` r
as.list(h)
```

    ## $f
    ## [1] 6
    ## 
    ## $g
    ## [1] 7
    ## 
    ## $h
    ## [1] 8
    ## 
    ## $i
    ## [1] 9
    ## 
    ## $j
    ## [1] 10
    ## 
    ## $k
    ## [1] 11
    ## 
    ## $l
    ## [1] 12
    ## 
    ## $m
    ## [1] 13
    ## 
    ## $n
    ## [1] 14
    ## 
    ## $o
    ## [1] 15
    ## 
    ## $p
    ## [1] 16
    ## 
    ## $q
    ## [1] 17
    ## 
    ## $r
    ## [1] 18
    ## 
    ## $s
    ## [1] 19
    ## 
    ## $t
    ## [1] 20
    ## 
    ## $u
    ## [1] 21
    ## 
    ## $v
    ## [1] 22
    ## 
    ## $w
    ## [1] 23
    ## 
    ## $x
    ## [1] 24
    ## 
    ## $y
    ## [1] 25
    ## 
    ## $z
    ## [1] 26
    ## 
    ## $a
    ## [1] 5
    ## 
    ## $b
    ## [1] 2
    ## 
    ## $c
    ## [1] 3
    ## 
    ## $d
    ## [1] 4
    ## 
    ## $e
    ## [1] 5

``` r
#TODO: list usage in R
all_unique_char <- function (str) {
  chars <- strsplit(str, "")[[1]]
  list_of_chars <- list()
  for (char in chars) {
    list_of_chars[[char]] <- list_of_chars[[char]] +1
    print(list_of_chars[[char]])
  }
  return(list_of_chars)
}
str = "notunique"
class(str)
```

    ## [1] "character"

``` r
all_unique_char(str)
```

    ## numeric(0)
    ## numeric(0)
    ## numeric(0)
    ## numeric(0)
    ## numeric(0)
    ## numeric(0)
    ## numeric(0)
    ## numeric(0)
    ## numeric(0)

    ## $n
    ## numeric(0)
    ## 
    ## $o
    ## numeric(0)
    ## 
    ## $t
    ## numeric(0)
    ## 
    ## $u
    ## numeric(0)
    ## 
    ## $i
    ## numeric(0)
    ## 
    ## $q
    ## numeric(0)
    ## 
    ## $e
    ## numeric(0)

TODO: write up a blog about Rcpp
--------------------------------

``` cpp
#include <Rcpp.h>

// [[Rcpp::export]]
int fibonacci(const int x) {
    if (x == 0 || x == 1) return(x);
    return (fibonacci(x - 1)) + fibonacci(x - 2);
}
```
