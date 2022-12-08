geom bar attribute
================
Monalisa Roy

### Read the data

``` r
pharma=read.csv("Pharmacovigilance_audit_Data.csv",stringsAsFactors = T)
View(pharma)
```

``` r
library(ggplot2)
```

### Building a bar_plot:

**Assign ’LocationID’column to x-axis**

``` r
ggplot(data = pharma,aes(x=LocationID))+geom_bar()
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

**Assigning ‘Issues’ to the fill attribute**

``` r
ggplot(data = pharma,aes(x=LocationID,fill=Issues))+geom_bar()
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

**Setting a title to ‘LocationID Plot’**

``` r
ggplot(data = pharma,aes(x=LocationID,fill=Issues))+geom_bar()+ggtitle( "LocationID Plot")
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

### Building a bar-plot for the ‘DrugID’ column\*\*

**Assigning the fill color to be ‘orange’**

``` r
ggplot(data = pharma,aes(x=DrugID,))+geom_bar(fill="orange")
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

**Assigning the boundary color to be ‘peru’**

``` r
ggplot(data = pharma,aes(x=DrugID))+geom_bar(fill="orange",col="peru")
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

**Setting title to ‘DrugID Plot’**

``` r
ggplot(data = pharma,aes(x=DrugID))+geom_bar(fill="orange",col="peru")+ggtitle("DrugID Plot")
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

### Building a bar-plot for the ’Gender’column assigned to x-axis.

**Assigning ‘DrugID’ to the fill aesthetic**

``` r
ggplot(data = pharma,aes(x=Gender,fill=DrugID))+geom_bar()
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

**Assign ‘Issues’ to the fill aesthetic**

``` r
ggplot(data = pharma,aes(x=Gender,fill=Issues))+geom_bar()
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

**Changing the position of the bars to ‘identity’**

``` r
ggplot(data = pharma,aes(x=Gender,fill=Issues))+geom_bar(position = "identity")
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->

**Setting title to ‘Gender Plot’**

``` r
ggplot(data = pharma,aes(x=Gender,fill=Issues))+geom_bar(position = "identity")+ggtitle("Gender Plot")
```

![](geom_bar_attribute_files/figure-gfm/unnamed-chunk-12-1.png)<!-- -->
