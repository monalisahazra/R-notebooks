Median function
================
Monalisa Roy

### Read the data,load libraries

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

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
```

## Using customer churn dataset

### Calculate the median of ’tenure’column and store it in med_tenure

``` r
median(customer$tenure)->med_tenure
med_tenure
```

    ## [1] 29

### Calculate the median of ’MonthlyCharges’column and store it in med_MonthlyCharges.

``` r
median(customer$MonthlyCharges)->med_MonthlyCharges
med_MonthlyCharges
```

    ## [1] 70.35

### Calculate the median of ’TotalCharges’column and store it in med_TotalCharges.

``` r
median(customer$TotalCharges)->med_TotalCharges
na.omit(customer)->customer
med_TotalCharges
```

    ## [1] NA

## Using Student Placement dataset.

### Calculate the median of percentage scored in senior secondary exams(ssc_p) and store it in med_ssc

``` r
median(placement$ssc_p)->med_ssc
med_ssc
```

    ## [1] 67

### Calculate the median of scores in higher secondary exams(hsc_p) and store it in med_hsc

``` r
median(placement$hsc_p)->med_hsc
med_hsc
```

    ## [1] 65

### Calculate the median of percentage score by students in their respective degree(degree_p)and store it in med_degree.

``` r
median(placement$degree_p)->med_degree
med_degree
```

    ## [1] 66
