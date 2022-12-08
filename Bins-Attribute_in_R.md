Bins Attribute in R
================
Monalisa Roy

## Read the data

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)
pharma=read.csv("Pharmacovigilance_audit_Data.csv",stringsAsFactors = T)
```

## Install packages

``` r
library(ggplot2)
```

## Create a histogram for ‘Age’ column using pharmacovigilance dataset.

### Set number of bins to 100

``` r
ggplot(data = pharma,aes(x=Age))+geom_histogram(bins = 100)
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Assign a color ‘azure’ to the histogram

``` r
ggplot(data = pharma,aes(x=Age))+geom_histogram(bins = 100,col="azure")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

### Assign a colour ‘white’ to the fill attribute in geom_histogram function.

``` r
ggplot(data = pharma,aes(x=Age))+geom_histogram(bins = 100,col="azure",fill="white")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

## Create a histogram for ‘PatientID’ column using pharmacovigilance dataset.

### Assign a color ‘wheat3’ to the histogram

``` r
ggplot(data = pharma,aes(x=PatientID))+geom_histogram(col="wheat3")
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

### Set number of bins to 50

``` r
ggplot(data = pharma,aes(x=PatientID))+geom_histogram(col="wheat3",bins = 50)
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

### Assign a colour ‘black’ to the fill attribute in geom_histogram function.

``` r
ggplot(data = pharma,aes(x=PatientID))+geom_histogram(col="wheat3",bins = 50,fill="black")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

## Create a histogram using customer churn dataset.

### Assign MonthlyCharges column to the x-axis

``` r
ggplot(data=customer,aes(x=MonthlyCharges))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

### Set the number of bins to 80

``` r
ggplot(data=customer,aes(x=MonthlyCharges))+geom_histogram(bins = 80)
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

### Assign a color ‘violet’ to the bars.

``` r
ggplot(data=customer,aes(x=MonthlyCharges))+geom_histogram(bins = 80,col="violet")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

### Assign a colour ‘white’ to the fill attribute in geom_histogram function.

``` r
ggplot(data=customer,aes(x=MonthlyCharges))+geom_histogram(bins = 80,col="violet",fill="white")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

## Create a histogram using customer churn dataset.

### Assign ‘tenure’ column to the x-axis.

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

### Set the number of bins to 50

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram(bins=50)
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->

### Assign a color ‘white’ to the bars.

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram(bins=50,col="white")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-15-1.png)<!-- -->

### Assign a colour ‘black’ to the fill attribute in geom_histogram function.

``` r
ggplot(data = customer,aes(x=tenure))+geom_histogram(bins=50,col="white",fill="black")
```

![](Bins-Attribute_in_R_files/figure-gfm/unnamed-chunk-16-1.png)<!-- -->
