Calculating Mean
================
Monalisa Roy

## Read the data,load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)

customer=read.csv("customer-churn",stringsAsFactors = T)
```

## Calculate the mean of the following columns from customer churn dataset.

-   Tenure
-   MonthlyCharges
-   TotalCharges

``` r
mean(customer$tenure)
```

    ## [1] 32.37115

``` r
mean(customer$MonthlyCharges)
```

    ## [1] 64.76169

``` r
na.omit(customer)->customer
mean(customer$TotalCharges)
```

    ## [1] 2283.3

### or

``` r
na.omit(customer)->customer
colMeans(customer[,c(6,19,20)])
```

    ##         tenure MonthlyCharges   TotalCharges 
    ##       32.42179       64.79821     2283.30044

## Calculate the mean of the following columns from the placement dataset:

``` r
na.omit(placement)->placement

colMeans(placement[,c(3,5,8,11,13,15)])
```

    ##        ssc_p        hsc_p     degree_p      etest_p        mba_p       salary 
    ##     71.72149     69.92655     68.74054     73.23804     62.57939 288655.40541
