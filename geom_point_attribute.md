geom point attribute
================
Monalisa Roy

### Read the data, load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
library(ggplot2)
```

### Creating a scatter-plot

**Assigning ’hsc_p’column to x-axis and ’ssc_p’column to y-axis**

``` r
ggplot(data=placement,aes(x=hsc_p,y=ssc_p))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

**Mapping ‘gender’ to col aesthetic**

``` r
ggplot(data=placement,aes(x=hsc_p,y=ssc_p,col=gender))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

**Mapping ’workex’to col aesthetic**

``` r
ggplot(data=placement,aes(x=hsc_p,y=ssc_p,col=workex))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

**Mapping ’status to col aesthetic**

``` r
ggplot(data=placement,aes(x=hsc_p,y=ssc_p,col=status))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

**Add a title to the plot as’Comparing HSC & SSC Percentage’**

``` r
ggplot(data=placement,aes(x=hsc_p,y=ssc_p,col=status))+geom_point()+ggtitle("Comparing HSC & SSC Percentage")
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

### Creating a scatter-plot\*\*

**Assigning ’degree_p’column to the x-axis and ’mba_p’column to the
y-axis.**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

**Using ‘col’ as an aesthetic and assign it the column ‘status’**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p,col=status))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

**Using ‘col’ as an aesthetic and assign it the column
‘specialisation’**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p,col=specialisation))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

**Adding a title to the plot as ‘Understanding Degree & MBA
Percentage’**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p,col=specialisation))+geom_point()+ggtitle("Understanding Degree & MBA Percentage")
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

### Creating a scatter-plot:

**Assigning ’etest_p’column to the x-axis and ’salary’column to the
y-axis**

``` r
ggplot(data=placement,aes(x=etest_p,y=salary))+geom_point()
```

    ## Warning: Removed 67 rows containing missing values (`geom_point()`).

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

**Use ‘col’ as an aesthetic and assign it the column ‘workex’**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p,col=workex))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

**Using ‘col’ as an aesthetic and assign it the column ‘gender’**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p,col=gender))+geom_point()
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->

**Adding a title to the plot as’E-test & Salary’**

``` r
ggplot(data=placement,aes(x=degree_p,y=mba_p,col=gender))+geom_point()+ggtitle("E-test & Salary")
```

![](geom_point_attribute_files/figure-gfm/unnamed-chunk-14-1.png)<!-- -->
