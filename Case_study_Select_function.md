Select function case study
================
Monalisa Roy

## Read the data,load libraries

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)

library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

## Extract the individual columns:

### Extract the 5th column and store it in ‘customer_5’

``` r
select(customer,5)->customer_5
View(customer_5)
```

### Extract the 15th column and store it in ‘customer_15’

``` r
select(customer,15)->customer_15
View(customer_15)
```

### Extract the column numbers 3,6,9,12,15 and 18 and store the result in ‘customer_3\_multiple’

``` r
select(customer,3,6,9,12,15,18)->customer_3_multiple
View(customer_3_multiple)
```

### Extract all the column number 10 to column number 20 and store the result in ‘c_10_20’

``` r
select(customer,10:20)->c_10_20
View(c_10_20)
```

### Extract all the columns which start with letter’P’and store it in customer_P

``` r
select(customer,starts_with("P"))->customer_P
View(customer_P)
```

### Extract all the columns which end with letter ‘s’ and store it in’customer_s’

``` r
select(customer,ends_with("s"))->customer_s
View(customer_s)
```
