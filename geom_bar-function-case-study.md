geom bar function case study
================
Monalisa Roy

### Read the data

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)
```

### Loading the relevant plotting library

-   We are going to use ggplot here. If it is not installed, then
    un-comment the line install(ggplot2)

``` r
#install(ggplot2)
library(ggplot2)
```

### Bar plot

-   We build a bar-plot for the ’PhoneService’column.

``` r
ggplot(data = customer,aes(x=PhoneService))+geom_bar()
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->

### Coloring a bar plot

-   We assign the fill color to be ‘pink’.

``` r
ggplot(data = customer,aes(x=PhoneService))+geom_bar(fill="pink")
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

### Coloring boundaries

-   We assign the boundary color to be “peru”.

``` r
ggplot(data = customer,aes(x=PhoneService))+geom_bar(fill="pink",col="peru")
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->

-   Creating a bar-plot for the ‘InternetService’ column.

``` r
ggplot(data = customer,aes(x=InternetService))+geom_bar()
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->
### Filling aesthetic

-   Assigning ‘InternetService’ to the fill aesthetic.

``` r
ggplot(data = customer,aes(x=InternetService,fill=InternetService))+geom_bar()
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-7-1.png)<!-- -->

-   Assigning ‘Contract’ to the fill aesthetic.

``` r
ggplot(data = customer,aes(x=InternetService,fill=Contract))+geom_bar()
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

### Changing position

-   We change the position of bars to ‘identity’

``` r
ggplot(data = customer,aes(x=InternetService,fill=Contract))+geom_bar(position = "identity")
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-9-1.png)<!-- -->

-   Building a bar-plot for ’TechSupport’column

``` r
ggplot(data = customer,aes(x=TechSupport))+geom_bar()
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-10-1.png)<!-- -->

-   Assigning ‘Churn’ to the fill aesthetic.

``` r
ggplot(data = customer,aes(x=TechSupport,fill=Churn))+geom_bar()
```

![](geom_bar-function-case-study_files/figure-gfm/unnamed-chunk-11-1.png)<!-- -->
