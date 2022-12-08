Standard Deviation
================
Monalisa Roy

### Read the data,load libraries

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

customer=read.csv("customer-churn",stringsAsFactors = T)
```

## Using the customer churn dataset:

### Calculate the standard deviation of ’tenure’column and store it in sd_tenure.

``` r
sd(customer$tenure)->sd_tenure
sd_tenure
```

    ## [1] 24.55948

### Calculate the standard deviation of ’MonthlyCharges’column and store it in sd_MonthlyCharges

``` r
sd(customer$MonthlyCharges)->sd_MonthlyCharges
sd_MonthlyCharges
```

    ## [1] 30.09005

### Calculate the standard deviation of ’TotalCharges’column and store it in sd_TotalCharges.

``` r
na.omit(customer)->customer
sd(customer$TotalCharges)->Sd_TotalCharges
Sd_TotalCharges
```

    ## [1] 2266.771

#### Using student’s placement dataset:

## Calculate the standard deviation of etest and store it in sd_etest.

``` r
sd(placement$etest_p)->sd_etest
sd_etest
```

    ## [1] 13.27596

## Calculate the standard deviation of salary and store it in sd_salary.

``` r
na.omit(placement)->placement
sd(placement$salary)->sd_salary
sd_salary
```

    ## [1] 93457.45

## Calculate the standard deviation of percentage score by students in MBA(mba_p)and store it in sd_mba.

``` r
sd(placement$mba_p)->sd_mba
sd_mba
```

    ## [1] 5.884583
