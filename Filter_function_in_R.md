Filter function
================
Monalisa Roy

## Read the data,load libraries

``` r
library(dplyr)
```

    ## 
    ## Attaching package: 'dplyr'

    ## The following objects are masked from 'package:stats':
    ## 
    ##     filter, lag

    ## The following objects are masked from 'package:base':
    ## 
    ##     intersect, setdiff, setequal, union

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
```

### Extract the data of the students who studied Science(hsc_s)from Central board(hsc_b)and secured more than 70 percent(hsc_p)and store it in s_science.

``` r
filter(placement,hsc_s=="Science" & hsc_b=="Central" & hsc_p>70)->s_science
View(s_science)
```

### Extract the data of the students who are pursuing a degree in Commerce & Management(degree_t)and specialization in Mkt&Fin and store it in d_commerce.

``` r
filter(placement,degree_t=="Comm&Mgmt",specialisation=="Mkt&Fin")->d_commerce
View(d_commerce)
```

### Extract the data of the students whose score in MBA(mba_p)is greater than 75 with etest score greater than 70.

``` r
filter(placement,mba_p>75 & etest_p>70)->new_data
View(new_data)
```

### Extract the data of students with specialization as Mkt&Fin with etest score greater than 90

``` r
filter(placement,specialisation=="Mkt&Fin",etest_p>90)->new_data2
View(new_data2)
```

### Extract the dat of students who are either from Commerce or Science strem.

``` r
filter(placement,hsc_s=="Commerce" | hsc_s=="Science")->new_data4
View(new_data4)
```
