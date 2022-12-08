Sample and Count function Case Study
================
Monalisa Roy

### Read the data,load libraries

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)
View(customer)

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

#### Extract 333 random records from the customer_churn dataframe and store the result in ‘customer_333’

``` r
sample_n(customer,333)->customer_333
View(customer_333)
```

#### Extract 1000 random records from the customer_churn dataframe and store the result in ‘customer_1000’

``` r
sample_n(customer,1000)->customer_1000
View(customer_1000)
```

#### Randomly extract 23% of the records from the customer_churn dataframe and store the result in’customer_23_percent’.

``` r
sample_frac(customer,0.23)->customer_23_percent
View(customer_23_percent)
```

#### Get the count of different level from the ’PaymentMethod’columnn.

``` r
count(customer,PaymentMethod,sort=TRUE)
```

    ##               PaymentMethod    n
    ## 1          Electronic check 2365
    ## 2              Mailed check 1612
    ## 3 Bank transfer (automatic) 1544
    ## 4   Credit card (automatic) 1522

## or

``` r
count_(customer,"PaymentMethod",sort = TRUE)
```

    ## Warning: `count_()` was deprecated in dplyr 0.7.0.
    ## ℹ Please use `count()` instead.
    ## ℹ See vignette('programming') for more help
    ## ℹ The deprecated feature was likely used in the dplyr package.
    ##   Please report the issue at <https://github.com/tidyverse/dplyr/issues>.

    ##               PaymentMethod    n
    ## 1          Electronic check 2365
    ## 2              Mailed check 1612
    ## 3 Bank transfer (automatic) 1544
    ## 4   Credit card (automatic) 1522

#### Get the count of different levels from the ‘Churn’ column.

``` r
count(customer,Churn,sort=TRUE)
```

    ##   Churn    n
    ## 1    No 5174
    ## 2   Yes 1869
