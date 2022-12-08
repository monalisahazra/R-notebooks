geom_histogram
================
Monalisa Roy

### Read the data, load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
library(ggplot2)
```

### Creating a histogram for ‘ssc_p’ column

``` r
ggplot(data = placement,aes(x=ssc_p))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

**Assigning a color ‘azure’ to the histogram**

``` r
ggplot(data = placement,aes(x=ssc_p))+geom_histogram(col="azure")
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

**Changing number of bins to 50**

``` r
ggplot(data = placement,aes(x=ssc_p))+geom_histogram(bins=50,col="azure")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

**Assigning a color ‘cornsilk4’to the’fill’ attribute in geom_histogram
function**

``` r
ggplot(data = placement,aes(x=ssc_p))+geom_histogram(bins=50,col="azure",fill="cornsilk4")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

**Giving it a title**

``` r
ggplot(data = placement,aes(x=ssc_p))+geom_histogram(bins=50,col="azure",fill="cornsilk4")+ggtitle("SSC Percentage")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

### Creating a histogram for ‘hsc_p’

``` r
ggplot(data = placement,aes(x=hsc_p))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

**Assigning a color ‘wheat3’ to the histogram**

``` r
ggplot(data = placement,aes(x=hsc_p))+geom_histogram(col="wheat3")
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

**Changing number of bins to 50**

``` r
ggplot(data = placement,aes(x=hsc_p))+geom_histogram(bins=50,col="wheat3")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

**Assigning a color ‘black’to the’fill’ attribute in geom_histogram
function**

``` r
ggplot(data = placement,aes(x=hsc_p))+geom_histogram(bins=50,fill="black",col="wheat3")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

**Giving it a title as ‘HSC Percentage’**

``` r
ggplot(data = placement,aes(x=hsc_p))+geom_histogram(bins=50,fill="black",col="wheat3")+ggtitle("HSC Percentage")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

### Creating a histogram as per the following condition

**Assigning ’degree_p’column to the x-axis**

``` r
ggplot(data = placement,aes(x=degree_p))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

**Setting the number of bins to 80**

``` r
ggplot(data = placement,aes(x=degree_p))+geom_histogram(bins=80)
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

**Assigning a color ‘violet’ to the bars**

``` r
ggplot(data = placement,aes(x=degree_p))+geom_histogram(bins=80,col="violet")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->

**Assigning a color ‘white’to the’fill’ attribute in geom_histogram
function**

``` r
ggplot(data = placement,aes(x=degree_p))+geom_histogram(bins=80,col="violet",fill="white")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-15-1.png)<!-- -->

**Giving it a title ‘Degree Percentage’**

``` r
ggplot(data = placement,aes(x=degree_p))+geom_histogram(bins=80,col="violet",fill="white")+ggtitle("Degree Percentage")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-16-1.png)<!-- -->

### Creating a histogram with condition

**Assign ’etest_p’column to the x-axis**

``` r
ggplot(data = placement,aes(x=etest_p))+geom_histogram()
```

    ## `stat_bin()` using `bins = 30`. Pick better value with `binwidth`.

![](geom_histogram_files/figure-gfm/unnamed-chunk-17-1.png)<!-- -->

**Setting the number of bins to 100**

``` r
ggplot(data = placement,aes(x=etest_p))+geom_histogram(bins = 100)
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-18-1.png)<!-- -->

**Assigning a color ‘white’ to the bars**

``` r
ggplot(data = placement,aes(x=etest_p))+geom_histogram(bins = 100,col="white")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-19-1.png)<!-- -->

**Assigning a color ‘black’to the’fill’ attribute in geom_histogram
function**

``` r
ggplot(data = placement,aes(x=etest_p))+geom_histogram(bins = 100,col="white",fill="black")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-20-1.png)<!-- -->

**Giving it a title as ‘E_test Percentage’**

``` r
ggplot(data = placement,aes(x=etest_p))+geom_histogram(bins = 100,col="white",fill="black")+ggtitle("E-test Percentage")
```

![](geom_histogram_files/figure-gfm/unnamed-chunk-21-1.png)<!-- -->
