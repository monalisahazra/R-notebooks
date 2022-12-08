Fill-Attribute_in_R
================
Monalisa Roy

### Read the data

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
```

### Install packages

``` r
library(ggplot2)
```

### Build a bar-plot

### Assign ‘etest_p’ column to x-axis

``` r
ggplot(data = placement,aes(x=etest_p))+geom_bar(col="orange")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Assign ’specialisation’column to x-axis

``` r
ggplot(data = placement,aes(x=specialisation))+geom_bar(fill="cyan",col="orange")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

### Assign ‘workex’ to the fill attribute

``` r
ggplot(data = placement,aes(x=specialisation,fill=workex))+geom_bar(col="orange")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

### Build a bar-plot for the ‘degree_t’ column

### Assign the fill color to be ‘orange’

``` r
ggplot(data = placement,aes(x=degree_t))+geom_bar(fill="orange")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

### Assign the boundary color to be ‘peru’

``` r
ggplot(data = placement,aes(x=degree_t))+geom_bar(fill="orange",col="peru")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

### Build a bar-plot for the ’hsc_s’ column assigned to x-axis and then:

### Assign ‘hsc_b’ to the fill aesthetic

``` r
ggplot(data = placement,aes(x=hsc_s,fill=hsc_b))+geom_bar(col="purple")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

### Assign ‘degree_t’ to the fill aesthetic

``` r
ggplot(data = placement,aes(x=hsc_s,fill=degree_t))+geom_bar(col="cyan")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

### Change the position of bars to ‘identity’

``` r
ggplot(data = placement,aes(x=hsc_s,fill=degree_t))+geom_bar(position ="identity")
```

![](Fill-Attribute_in_R_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->
