Geom box plot
================
Monalisa Roy

### Read the data, load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
library(ggplot2)
```

### Creating a box-plot between ‘etest_p’ & ‘workex’.Map ’etest_p’to the y-axis and workex to the x-axis.

``` r
ggplot(data = placement,aes(x=workex,y=etest_p))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

**Assigning it a fill color of ‘wheat3’**

``` r
ggplot(data = placement,aes(x=workex,y=etest_p))+geom_boxplot(fill="wheat3")
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

**Assigning it a boundary color of ‘snow3’**

``` r
ggplot(data = placement,aes(x=workex,y=etest_p))+geom_boxplot(fill="wheat3",col="snow3")
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

**Give a title as ‘E-test & Workex’**

``` r
ggplot(data = placement,aes(x=workex,y=etest_p))+geom_boxplot(fill="wheat3",col="snow3")+ggtitle("E-test & Workex")
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

### Build a box-plot between ‘etest_p’& ‘gender’. Map ‘etest_p’to the y-axis and ’gender’ to the x-axis.

``` r
ggplot(data = placement,aes(x=gender,y=etest_p))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

**Assigning ’degree_t’to the fill aesthetic**

``` r
ggplot(data = placement,aes(x=gender,y=etest_p,fill=degree_t))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

**Assign ’hsc_s’to the fill aesthetic**

``` r
ggplot(data = placement,aes(x=gender,y=etest_p,fill=hsc_s))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

**Give a title as ‘E-test & Gender’**

``` r
ggplot(data = placement,aes(x=gender,y=etest_p,fill=hsc_s))+geom_boxplot()+ggtitle("E-test & Gender")
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

### Build a box-plot between ‘etest_p’& ‘specialisation’

``` r
ggplot(data = placement,aes(x=specialisation,y=etest_p))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

#Assigning ’ssc_b’to the fill aesthetic\*\*

``` r
ggplot(data = placement,aes(x=specialisation,y=etest_p,fill=ssc_b))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

**Assigning ’hsc_b’to the fill aesthetic**

``` r
ggplot(data = placement,aes(x=specialisation,y=etest_p,fill=hsc_b))+geom_boxplot()
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->

**Giving a title as ‘E-test & Specialisation’**

``` r
ggplot(data = placement,aes(x=specialisation,y=etest_p,fill=hsc_b))+geom_boxplot()+ggtitle("E-test & Specialisation")
```

![](geom_box_plots_files/figure-gfm/unnamed-chunk-13-1.png)<!-- -->
