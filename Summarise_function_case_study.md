Summarise function Case Study
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

#### Get the median, variance,standaerd deviation for the ’tenure’column.

``` r
summarise(customer,median=median(tenure),var=var(tenure),sd=sd(tenure))
```

    ##   median      var       sd
    ## 1     29 603.1681 24.55948

#### Get the median, variance,standaerd deviation for the ’MonthlyCharges’column.

``` r
summarise(customer,median=median(MonthlyCharges),var=var(MonthlyCharges),sd=sd(MonthlyCharges))
```

    ##   median      var       sd
    ## 1  70.35 905.4109 30.09005

#### Get the standard deviation of ‘tenure’ and group it w.r.t ’PaymentMethod’column.

``` r
group_by(customer,PaymentMethod)->grouped
summarise(grouped,sd=sd(tenure))
```

    ## # A tibble: 4 × 2
    ##   PaymentMethod                sd
    ##   <fct>                     <dbl>
    ## 1 Bank transfer (automatic)  23.2
    ## 2 Credit card (automatic)    23.3
    ## 3 Electronic check           22.4
    ## 4 Mailed check               21.2

#### Get the median of ‘MonthlyCharges’ and group it w.r.t ’Contract’column.

``` r
group_by(customer,Contract)->grouped_1
summarise(grouped_1,median=median(MonthlyCharges))
```

    ## # A tibble: 3 × 2
    ##   Contract       median
    ##   <fct>           <dbl>
    ## 1 Month-to-month   73.2
    ## 2 One year         68.8
    ## 3 Two year         64.4

#### Get the variance of ‘TotalCharges’ and group it w.r.t’InternetService’column

``` r
group_by(customer,InternetService)->grouped_2
summarise(grouped_2,var=var(TotalCharges))
```

    ## # A tibble: 3 × 2
    ##   InternetService      var
    ##   <fct>              <dbl>
    ## 1 DSL                  NA 
    ## 2 Fiber optic     6606031.
    ## 3 No                   NA
