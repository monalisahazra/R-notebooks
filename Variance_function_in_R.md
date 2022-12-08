Variance function
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

customer=read.csv("customer-churn",stringsAsFactors = T)
View(customer)
```

## Using customer churn dataset:

#### Calculate the variance of ’tenure’column and store it in var_tenure

``` r
var(customer$tenure)->var_tenure
var_tenure
```

    ## [1] 603.1681

#### Calculate the variance of ’MonthlyCharges’column and store it in var_MonthlyCharges

``` r
var(customer$MonthlyCharges)->var_MonthlyCharges
var_MonthlyCharges
```

    ## [1] 905.4109

#### Calculate the variance of ’TotalCharges’column and store it in var_TotalCharges

``` r
var(customer$TotalCharges)->var_TotalCharges
var_TotalCharges
```

    ## [1] NA

## Using student’s placement dataset:

#### Calculate the variance of percentage scored in senior secondary exams(ssc_p)and store it in var_ssc

``` r
var(placement$ssc_p)->var_ssc
var_ssc
```

    ## [1] 117.2284

#### Calculate the variance of percentage scored in senior secondary exams(hsc_p)and store it in var_hsc.

``` r
var(placement$hsc_p)->var_hsc
var_hsc
```

    ## [1] 118.7557

#### Calculate the variance of percentage score by students in their respective degree(degree_p)and store it in var_degree

``` r
var(placement$degree_p)->var_degree
var_degree
```

    ## [1] 54.1511
