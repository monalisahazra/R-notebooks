Array
================
Monalisa Roy

## Read the data,load libraries

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)

placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
```

## Create an array as per the given data:

### An array named array_total_charges that contains the first 10 values from the total charges column.

``` r
array(data=customer$TotalCharges[1:10],dim = 10)->array_total_charges
array_total_charges
```

    ##  [1]   29.85 1889.50  108.15 1840.75  151.65  820.50 1949.40  301.90 3046.05
    ## [10] 3487.95

### An array named array_monthly_charges that contains the first 5 values from the monthly charges column.

``` r
array(data=customer$MonthlyCharges[1:5],dim = 5)->array_monthly_charges
array_monthly_charges
```

    ## [1] 29.85 56.95 53.85 42.30 70.70

## Create an array using placement dataset that comprises of:

### Data of first 15 values from salary column.

``` r
array(data = placement$salary[1:15],dim=15)->array_salary
array_salary
```

    ##  [1] 270000 200000 250000     NA 425000     NA     NA 252000 231000     NA
    ## [11] 260000 250000     NA 218000     NA

### Data of first 5 values from mba_p column.

``` r
array(data = placement$mba_p[1:5],dim = 5)->array_mba_p
array_mba_p
```

    ## [1] 58.80 66.28 57.80 59.43 55.50

### Data of first 10 values from e_test column.

``` r
array(data = placement$etest_p[1:10],dim = 10)->array_etest_p
array_etest_p
```

    ##  [1] 55.00 86.50 75.00 66.00 96.80 55.00 74.28 67.00 91.34 54.00
