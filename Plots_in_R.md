Plots in R
================
Monalisa Roy

## Read the data

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
View(placement)
```

### Create a plot to understand the distribution of degree_t column

``` r
plot(placement$degree_t)
```

![](Plots_in_R_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

### Create a plot to understand the distribution of hsc_s column

``` r
plot(placement$hsc_s)
```

![](Plots_in_R_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Create a plot for specialization column and give a heading as ‘Specialization of Candidate’

``` r
plot(placement$specialisation,main="Specialization of Candidate")
```

![](Plots_in_R_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

### Create a plot using ssc_b,give it a color of ‘aquamarine4’,and give a heading as ‘Type of Board’

``` r
plot(placement$ssc_b,col="aquamarine4",main="Type of Board")
```

![](Plots_in_R_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->
