Data visualization – Histogram
================
Monalisa Roy

## Plotting histograms

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)
View(customer)


library(ggplot2)
```

### Histogram for the’tenure’ column

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

### Coloring with ‘mediumspringgreen’

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram(fill="mediumspringgreen")
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Boundary color

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram(fill="mediumspringgreen",col="azure")
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->
### Altering the number of the bins to be 100.

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram(fill="mediumspringgreen",col="azure",bins = 100)
```

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

### Histogram for the’MonthlyCharges’ column.

``` r
ggplot(data = customer,aes(x=MonthlyCharges))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

### ‘PaymentMethod’ to the fill aesthetic.

``` r
ggplot(data = customer,aes(x=MonthlyCharges,fill=PaymentMethod))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

### Assigning ‘OnlineBackup’ to the fill aesthetic.

``` r
ggplot(data = customer,aes(x=MonthlyCharges,fill=OnlineBackup))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

### Building a histogram for the ’TotalCharges’column

``` r
ggplot(data=customer,aes(x=TotalCharges))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

    ## Warning: Removed 11 rows containing non-finite values (`stat_bin()`).

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

### ‘gender’ to the fill aesthetic.

``` r
ggplot(data=customer,aes(x=TotalCharges,fill=gender))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

    ## Warning: Removed 11 rows containing non-finite values (`stat_bin()`).

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

### Assigning ‘InternetService’ to the fill aesthetic.

``` r
ggplot(data=customer,aes(x=TotalCharges,fill=InternetService))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

    ## Warning: Removed 11 rows containing non-finite values (`stat_bin()`).

![](geom_histogram_case_study_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->
