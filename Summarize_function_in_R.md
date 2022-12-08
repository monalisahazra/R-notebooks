Summarize function
================
Monalisa Roy

## Read the data,load libraries

``` r
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

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
View(placement)
```

## Using summerize()function calculate the following for etest column.

-   Median
-   Variance
-   Standard Deviation

``` r
summarise(placement,median=median(etest_p),var=var(etest_p),sd=sd(etest_p))
```

    ##   median     var       sd
    ## 1     71 176.251 13.27596

## Calculate the following for MBA percentage(mba_p)of students:

-   Median
-   Variance
-   Standard Deviation

``` r
summarise(placement,median=median(mba_p))
```

    ##   median
    ## 1     62

``` r
summarise(placement,var=var(mba_p))
```

    ##        var
    ## 1 34.02838

``` r
summarise(placement,sd=sd(mba_p))
```

    ##         sd
    ## 1 5.833385

## Calculate the median of hsc_p and group it w.r.t ’Salary’column.

``` r
group_by(placement,salary)->new_data
summarise(new_data,hsc_median=median(hsc_p))
```

    ## # A tibble: 46 × 2
    ##    salary hsc_median
    ##     <int>      <dbl>
    ##  1 200000       74.1
    ##  2 204000       63  
    ##  3 210000       67.5
    ##  4 216000       63  
    ##  5 218000       85.4
    ##  6 220000       66.6
    ##  7 225000       63  
    ##  8 230000       69.7
    ##  9 231000       79  
    ## 10 233000       63  
    ## # … with 36 more rows
    ## # ℹ Use `print(n = ...)` to see more rows

## Calculate variance of ssc_p and group it w.r.t ’salary’column.

``` r
group_by(placement,salary)->new_data1
summarise(new_data1,ssc_var=var(ssc_p))
```

    ## # A tibble: 46 × 2
    ##    salary ssc_var
    ##     <int>   <dbl>
    ##  1 200000    36.1
    ##  2 204000    60.5
    ##  3 210000    58.9
    ##  4 216000    44.3
    ##  5 218000    76.9
    ##  6 220000    56.3
    ##  7 225000    NA  
    ##  8 230000    19.7
    ##  9 231000    NA  
    ## 10 233000    NA  
    ## # … with 36 more rows
    ## # ℹ Use `print(n = ...)` to see more rows

-   There are some salaries that occur only once, hence the variance is
    NA.
-   The following removes the NA values

``` r
na.omit(summarise(new_data1,ssc_var=var(ssc_p)))
```

    ## # A tibble: 22 × 2
    ##    salary ssc_var
    ##     <int>   <dbl>
    ##  1 200000    36.1
    ##  2 204000    60.5
    ##  3 210000    58.9
    ##  4 216000    44.3
    ##  5 218000    76.9
    ##  6 220000    56.3
    ##  7 230000    19.7
    ##  8 236000    21.1
    ##  9 240000    46.3
    ## 10 250000    51.3
    ## # … with 12 more rows
    ## # ℹ Use `print(n = ...)` to see more rows

-   or

``` r
na.omit(summarise(group_by(placement,salary),ssc_var=var(ssc_p)))
```

    ## # A tibble: 22 × 2
    ##    salary ssc_var
    ##     <int>   <dbl>
    ##  1 200000    36.1
    ##  2 204000    60.5
    ##  3 210000    58.9
    ##  4 216000    44.3
    ##  5 218000    76.9
    ##  6 220000    56.3
    ##  7 230000    19.7
    ##  8 236000    21.1
    ##  9 240000    46.3
    ## 10 250000    51.3
    ## # … with 12 more rows
    ## # ℹ Use `print(n = ...)` to see more rows

## Calculate standard deviation of etest_p and group it w.r.t.’Salary’

-   Keeping the rows without NA in the std dev. column

``` r
na.omit(summarise(group_by(placement,salary),etest_p_sd=sd(etest_p)))
```

    ## # A tibble: 22 × 2
    ##    salary etest_p_sd
    ##     <int>      <dbl>
    ##  1 200000      12.9 
    ##  2 204000       5.66
    ##  3 210000       9.71
    ##  4 216000      11   
    ##  5 218000      12.7 
    ##  6 220000       7.26
    ##  7 230000       7.78
    ##  8 236000      21.2 
    ##  9 240000      16.2 
    ## 10 250000      14.2 
    ## # … with 12 more rows
    ## # ℹ Use `print(n = ...)` to see more rows

-   If we want to keep the NA values

``` r
summarise(group_by(placement,salary),etest_p_sd=sd(etest_p))
```

    ## # A tibble: 46 × 2
    ##    salary etest_p_sd
    ##     <int>      <dbl>
    ##  1 200000      12.9 
    ##  2 204000       5.66
    ##  3 210000       9.71
    ##  4 216000      11   
    ##  5 218000      12.7 
    ##  6 220000       7.26
    ##  7 225000      NA   
    ##  8 230000       7.78
    ##  9 231000      NA   
    ## 10 233000      NA   
    ## # … with 36 more rows
    ## # ℹ Use `print(n = ...)` to see more rows
