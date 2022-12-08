Class function
================
Monalisa Roy

## Read the data,load libraries

``` r
City_temp=read.csv("city_temperature.csv",stringsAsFactors = T)

placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
```

## Find the class of the following attribute:

### Region

``` r
class(City_temp$Region)
```

    ## [1] "factor"

### Country

``` r
class(City_temp$Country)
```

    ## [1] "factor"

### City

``` r
class(City_temp$City)
```

    ## [1] "factor"

### Month

``` r
class(City_temp$Month)
```

    ## [1] "integer"

### Day

``` r
class(City_temp$Day)
```

    ## [1] "integer"

### Year

``` r
class(City_temp$Year)
```

    ## [1] "integer"

### AvgTemperature

``` r
class(City_temp$AvgTemperature)
```

    ## [1] "numeric"

### OR in a single code we can find the class of different columns in the City_temp data.

``` r
sapply(City_temp, class)
```

    ##         Region        Country          State           City          Month 
    ##       "factor"       "factor"      "logical"       "factor"      "integer" 
    ##            Day           Year AvgTemperature 
    ##      "integer"      "integer"      "numeric"

``` r
lapply(City_temp,class)
```

    ## $Region
    ## [1] "factor"
    ## 
    ## $Country
    ## [1] "factor"
    ## 
    ## $State
    ## [1] "logical"
    ## 
    ## $City
    ## [1] "factor"
    ## 
    ## $Month
    ## [1] "integer"
    ## 
    ## $Day
    ## [1] "integer"
    ## 
    ## $Year
    ## [1] "integer"
    ## 
    ## $AvgTemperature
    ## [1] "numeric"

## After finding the class of the above attributes, convert them to the following data type:

### Vector to character.

### Gender

``` r
as.character(placement$gender)
```

    ##   [1] "M" "M" "M" "M" "M" "M" "F" "M" "M" "M" "M" "M" "F" "F" "M" "F" "M" "F"
    ##  [19] "F" "M" "M" "F" "F" "F" "M" "F" "M" "M" "M" "M" "F" "F" "F" "F" "M" "F"
    ##  [37] "M" "F" "F" "M" "F" "F" "M" "M" "F" "F" "F" "M" "M" "F" "F" "M" "F" "M"
    ##  [55] "F" "M" "M" "M" "M" "M" "M" "M" "F" "M" "M" "M" "M" "M" "F" "M" "M" "M"
    ##  [73] "M" "M" "M" "F" "F" "M" "M" "F" "F" "M" "M" "M" "M" "F" "M" "M" "F" "F"
    ##  [91] "F" "M" "F" "M" "M" "M" "F" "F" "F" "M" "F" "M" "F" "M" "M" "M" "M" "M"
    ## [109] "M" "M" "F" "M" "M" "F" "M" "F" "M" "M" "M" "M" "M" "F" "F" "M" "M" "F"
    ## [127] "F" "F" "M" "M" "M" "F" "M" "M" "F" "F" "F" "M" "F" "M" "M" "M" "M" "M"
    ## [145] "M" "M" "M" "M" "F" "M" "M" "M" "F" "M" "M" "M" "M" "M" "M" "M" "M" "M"
    ## [163] "M" "M" "F" "F" "M" "M" "F" "M" "F" "M" "M" "F" "M" "M" "F" "F" "M" "F"
    ## [181] "M" "M" "M" "M" "F" "F" "F" "M" "M" "F" "F" "M" "M" "F" "M" "M" "M" "F"
    ## [199] "F" "M" "M" "M" "M" "M" "F" "M" "M" "M" "F" "M" "M" "M" "M" "F" "M"

### ssc_b

``` r
as.character(placement$ssc_b)
```

    ##   [1] "Others"  "Central" "Central" "Central" "Central" "Others"  "Others" 
    ##   [8] "Central" "Central" "Central" "Central" "Central" "Central" "Central"
    ##  [15] "Central" "Central" "Central" "Central" "Central" "Others"  "Others" 
    ##  [22] "Others"  "Others"  "Others"  "Others"  "Others"  "Others"  "Others" 
    ##  [29] "Others"  "Central" "Central" "Central" "Central" "Others"  "Others" 
    ##  [36] "Central" "Central" "Central" "Others"  "Others"  "Central" "Others" 
    ##  [43] "Others"  "Others"  "Others"  "Central" "Others"  "Central" "Others" 
    ##  [50] "Others"  "Central" "Central" "Others"  "Others"  "Central" "Central"
    ##  [57] "Others"  "Central" "Central" "Central" "Central" "Central" "Others" 
    ##  [64] "Others"  "Others"  "Others"  "Others"  "Others"  "Central" "Central"
    ##  [71] "Others"  "Others"  "Others"  "Central" "Central" "Central" "Others" 
    ##  [78] "Others"  "Others"  "Central" "Others"  "Others"  "Central" "Others" 
    ##  [85] "Central" "Others"  "Others"  "Central" "Central" "Others"  "Others" 
    ##  [92] "Central" "Central" "Central" "Central" "Central" "Central" "Central"
    ##  [99] "Central" "Central" "Others"  "Central" "Others"  "Central" "Central"
    ## [106] "Central" "Others"  "Others"  "Central" "Central" "Central" "Others" 
    ## [113] "Others"  "Others"  "Central" "Others"  "Central" "Others"  "Central"
    ## [120] "Central" "Others"  "Central" "Central" "Others"  "Central" "Central"
    ## [127] "Others"  "Others"  "Central" "Central" "Central" "Others"  "Others" 
    ## [134] "Central" "Central" "Central" "Central" "Others"  "Others"  "Central"
    ## [141] "Central" "Central" "Central" "Others"  "Others"  "Others"  "Central"
    ## [148] "Central" "Central" "Central" "Central" "Central" "Others"  "Others" 
    ## [155] "Central" "Others"  "Central" "Central" "Others"  "Central" "Central"
    ## [162] "Others"  "Central" "Others"  "Central" "Central" "Others"  "Others" 
    ## [169] "Central" "Others"  "Others"  "Others"  "Others"  "Others"  "Others" 
    ## [176] "Others"  "Central" "Central" "Others"  "Central" "Central" "Central"
    ## [183] "Others"  "Central" "Others"  "Central" "Central" "Central" "Others" 
    ## [190] "Central" "Others"  "Others"  "Central" "Central" "Others"  "Central"
    ## [197] "Others"  "Others"  "Central" "Others"  "Others"  "Central" "Central"
    ## [204] "Others"  "Others"  "Others"  "Central" "Central" "Central" "Central"
    ## [211] "Others"  "Others"  "Others"  "Others"  "Central"

### hsc_b

``` r
as.character(placement$hsc_b)
```

    ##   [1] "Others"  "Others"  "Central" "Central" "Central" "Others"  "Others" 
    ##   [8] "Central" "Central" "Central" "Central" "Central" "Others"  "Central"
    ##  [15] "Central" "Central" "Central" "Central" "Central" "Others"  "Others" 
    ##  [22] "Others"  "Others"  "Others"  "Others"  "Central" "Others"  "Others" 
    ##  [29] "Others"  "Central" "Central" "Central" "Central" "Others"  "Others" 
    ##  [36] "Central" "Central" "Central" "Others"  "Others"  "Others"  "Others" 
    ##  [43] "Central" "Others"  "Others"  "Central" "Others"  "Central" "Others" 
    ##  [50] "Others"  "Central" "Central" "Others"  "Others"  "Others"  "Others" 
    ##  [57] "Others"  "Central" "Others"  "Others"  "Central" "Central" "Others" 
    ##  [64] "Others"  "Others"  "Others"  "Others"  "Others"  "Central" "Central"
    ##  [71] "Others"  "Others"  "Others"  "Others"  "Central" "Others"  "Central"
    ##  [78] "Others"  "Others"  "Central" "Others"  "Others"  "Central" "Others" 
    ##  [85] "Others"  "Others"  "Others"  "Central" "Central" "Others"  "Others" 
    ##  [92] "Central" "Central" "Central" "Central" "Others"  "Central" "Others" 
    ##  [99] "Central" "Others"  "Others"  "Central" "Others"  "Central" "Others" 
    ## [106] "Others"  "Others"  "Others"  "Central" "Others"  "Central" "Others" 
    ## [113] "Others"  "Others"  "Others"  "Others"  "Central" "Others"  "Central"
    ## [120] "Central" "Others"  "Others"  "Central" "Others"  "Central" "Central"
    ## [127] "Others"  "Others"  "Central" "Others"  "Others"  "Others"  "Others" 
    ## [134] "Others"  "Others"  "Others"  "Central" "Central" "Others"  "Central"
    ## [141] "Others"  "Central" "Others"  "Others"  "Others"  "Others"  "Others" 
    ## [148] "Central" "Central" "Central" "Central" "Central" "Central" "Others" 
    ## [155] "Others"  "Others"  "Central" "Central" "Others"  "Others"  "Central"
    ## [162] "Others"  "Others"  "Others"  "Central" "Others"  "Others"  "Others" 
    ## [169] "Central" "Others"  "Others"  "Others"  "Others"  "Others"  "Others" 
    ## [176] "Others"  "Others"  "Others"  "Others"  "Central" "Others"  "Others" 
    ## [183] "Others"  "Central" "Others"  "Central" "Central" "Central" "Others" 
    ## [190] "Others"  "Central" "Central" "Central" "Central" "Others"  "Central"
    ## [197] "Others"  "Others"  "Central" "Others"  "Others"  "Others"  "Central"
    ## [204] "Others"  "Others"  "Others"  "Central" "Others"  "Others"  "Central"
    ## [211] "Others"  "Others"  "Others"  "Others"  "Others"

### hsc_s

``` r
as.character(placement$hsc_s)
```

    ##   [1] "Commerce" "Science"  "Arts"     "Science"  "Commerce" "Science" 
    ##   [7] "Commerce" "Science"  "Commerce" "Commerce" "Commerce" "Commerce"
    ##  [13] "Science"  "Commerce" "Commerce" "Commerce" "Commerce" "Commerce"
    ##  [19] "Commerce" "Arts"     "Commerce" "Commerce" "Science"  "Science" 
    ##  [25] "Science"  "Commerce" "Commerce" "Commerce" "Commerce" "Commerce"
    ##  [31] "Commerce" "Science"  "Commerce" "Science"  "Science"  "Commerce"
    ##  [37] "Commerce" "Science"  "Science"  "Science"  "Commerce" "Commerce"
    ##  [43] "Science"  "Commerce" "Commerce" "Science"  "Science"  "Commerce"
    ##  [49] "Commerce" "Arts"     "Science"  "Commerce" "Commerce" "Science" 
    ##  [55] "Science"  "Science"  "Commerce" "Commerce" "Science"  "Science" 
    ##  [61] "Science"  "Commerce" "Science"  "Commerce" "Commerce" "Science" 
    ##  [67] "Science"  "Commerce" "Commerce" "Science"  "Science"  "Commerce"
    ##  [73] "Science"  "Commerce" "Commerce" "Commerce" "Arts"     "Science" 
    ##  [79] "Science"  "Science"  "Commerce" "Science"  "Commerce" "Science" 
    ##  [85] "Science"  "Commerce" "Commerce" "Science"  "Commerce" "Science" 
    ##  [91] "Commerce" "Commerce" "Science"  "Commerce" "Commerce" "Commerce"
    ##  [97] "Science"  "Commerce" "Commerce" "Commerce" "Commerce" "Commerce"
    ## [103] "Commerce" "Science"  "Science"  "Science"  "Science"  "Commerce"
    ## [109] "Commerce" "Science"  "Science"  "Science"  "Commerce" "Commerce"
    ## [115] "Science"  "Science"  "Commerce" "Science"  "Science"  "Commerce"
    ## [121] "Science"  "Science"  "Arts"     "Commerce" "Science"  "Commerce"
    ## [127] "Science"  "Science"  "Science"  "Commerce" "Commerce" "Science" 
    ## [133] "Commerce" "Commerce" "Commerce" "Science"  "Arts"     "Commerce"
    ## [139] "Science"  "Commerce" "Commerce" "Science"  "Science"  "Commerce"
    ## [145] "Arts"     "Science"  "Science"  "Commerce" "Arts"     "Arts"    
    ## [151] "Science"  "Commerce" "Science"  "Science"  "Science"  "Commerce"
    ## [157] "Science"  "Commerce" "Science"  "Commerce" "Science"  "Commerce"
    ## [163] "Commerce" "Science"  "Commerce" "Commerce" "Commerce" "Science" 
    ## [169] "Commerce" "Science"  "Commerce" "Commerce" "Commerce" "Science" 
    ## [175] "Science"  "Science"  "Commerce" "Commerce" "Science"  "Science" 
    ## [181] "Commerce" "Science"  "Arts"     "Commerce" "Commerce" "Science" 
    ## [187] "Commerce" "Science"  "Commerce" "Commerce" "Commerce" "Science" 
    ## [193] "Commerce" "Arts"     "Commerce" "Commerce" "Science"  "Science" 
    ## [199] "Commerce" "Commerce" "Commerce" "Science"  "Science"  "Commerce"
    ## [205] "Commerce" "Commerce" "Science"  "Commerce" "Science"  "Commerce"
    ## [211] "Commerce" "Science"  "Commerce" "Commerce" "Science"

### status

``` r
as.character(placement$status)
```

    ##   [1] "Placed"     "Placed"     "Placed"     "Not Placed" "Placed"    
    ##   [6] "Not Placed" "Not Placed" "Placed"     "Placed"     "Not Placed"
    ##  [11] "Placed"     "Placed"     "Not Placed" "Placed"     "Not Placed"
    ##  [16] "Placed"     "Placed"     "Not Placed" "Not Placed" "Placed"    
    ##  [21] "Placed"     "Placed"     "Placed"     "Placed"     "Placed"    
    ##  [26] "Not Placed" "Placed"     "Placed"     "Placed"     "Not Placed"
    ##  [31] "Placed"     "Not Placed" "Placed"     "Placed"     "Not Placed"
    ##  [36] "Placed"     "Not Placed" "Placed"     "Placed"     "Placed"    
    ##  [41] "Placed"     "Not Placed" "Not Placed" "Placed"     "Placed"    
    ##  [46] "Not Placed" "Not Placed" "Placed"     "Placed"     "Not Placed"
    ##  [51] "Placed"     "Not Placed" "Not Placed" "Placed"     "Placed"    
    ##  [56] "Placed"     "Placed"     "Placed"     "Placed"     "Placed"    
    ##  [61] "Placed"     "Placed"     "Placed"     "Not Placed" "Placed"    
    ##  [66] "Not Placed" "Placed"     "Placed"     "Not Placed" "Placed"    
    ##  [71] "Placed"     "Placed"     "Placed"     "Placed"     "Placed"    
    ##  [76] "Not Placed" "Placed"     "Placed"     "Placed"     "Not Placed"
    ##  [81] "Placed"     "Placed"     "Not Placed" "Placed"     "Placed"    
    ##  [86] "Placed"     "Placed"     "Not Placed" "Placed"     "Placed"    
    ##  [91] "Placed"     "Not Placed" "Placed"     "Not Placed" "Placed"    
    ##  [96] "Placed"     "Placed"     "Not Placed" "Placed"     "Not Placed"
    ## [101] "Not Placed" "Placed"     "Placed"     "Placed"     "Placed"    
    ## [106] "Not Placed" "Not Placed" "Placed"     "Placed"     "Not Placed"
    ## [111] "Placed"     "Not Placed" "Placed"     "Placed"     "Placed"    
    ## [116] "Placed"     "Placed"     "Placed"     "Placed"     "Placed"    
    ## [121] "Not Placed" "Placed"     "Placed"     "Placed"     "Placed"    
    ## [126] "Placed"     "Placed"     "Placed"     "Placed"     "Placed"    
    ## [131] "Not Placed" "Placed"     "Placed"     "Placed"     "Placed"    
    ## [136] "Placed"     "Not Placed" "Placed"     "Placed"     "Placed"    
    ## [141] "Placed"     "Not Placed" "Placed"     "Placed"     "Not Placed"
    ## [146] "Placed"     "Placed"     "Placed"     "Placed"     "Not Placed"
    ## [151] "Placed"     "Placed"     "Placed"     "Placed"     "Placed"    
    ## [156] "Not Placed" "Placed"     "Placed"     "Not Placed" "Not Placed"
    ## [161] "Placed"     "Not Placed" "Placed"     "Placed"     "Placed"    
    ## [166] "Not Placed" "Placed"     "Not Placed" "Not Placed" "Not Placed"
    ## [171] "Not Placed" "Placed"     "Placed"     "Not Placed" "Placed"    
    ## [176] "Not Placed" "Placed"     "Placed"     "Placed"     "Not Placed"
    ## [181] "Placed"     "Not Placed" "Not Placed" "Placed"     "Not Placed"
    ## [186] "Placed"     "Not Placed" "Placed"     "Not Placed" "Not Placed"
    ## [191] "Not Placed" "Placed"     "Placed"     "Placed"     "Not Placed"
    ## [196] "Placed"     "Placed"     "Placed"     "Not Placed" "Placed"    
    ## [201] "Placed"     "Not Placed" "Placed"     "Placed"     "Placed"    
    ## [206] "Placed"     "Not Placed" "Placed"     "Not Placed" "Placed"    
    ## [211] "Placed"     "Placed"     "Placed"     "Placed"     "Not Placed"

### workex

``` r
as.character(placement$workex)
```

    ##   [1] "No"  "Yes" "No"  "No"  "No"  "Yes" "No"  "Yes" "No"  "No"  "Yes" "Yes"
    ##  [13] "No"  "No"  "No"  "Yes" "Yes" "No"  "No"  "Yes" "No"  "No"  "No"  "Yes"
    ##  [25] "No"  "Yes" "Yes" "No"  "Yes" "No"  "No"  "No"  "No"  "Yes" "No"  "No" 
    ##  [37] "No"  "No"  "No"  "No"  "No"  "Yes" "No"  "No"  "Yes" "No"  "No"  "Yes"
    ##  [49] "No"  "No"  "No"  "No"  "No"  "No"  "No"  "No"  "No"  "No"  "No"  "No" 
    ##  [61] "Yes" "No"  "No"  "No"  "No"  "No"  "No"  "No"  "No"  "Yes" "No"  "No" 
    ##  [73] "No"  "No"  "No"  "No"  "No"  "Yes" "No"  "No"  "Yes" "Yes" "No"  "Yes"
    ##  [85] "Yes" "Yes" "No"  "No"  "No"  "Yes" "No"  "No"  "No"  "No"  "No"  "Yes"
    ##  [97] "Yes" "No"  "No"  "No"  "Yes" "No"  "Yes" "Yes" "Yes" "No"  "No"  "No" 
    ## [109] "No"  "Yes" "No"  "No"  "No"  "No"  "No"  "No"  "Yes" "No"  "Yes" "Yes"
    ## [121] "No"  "Yes" "Yes" "Yes" "Yes" "No"  "Yes" "No"  "Yes" "Yes" "No"  "Yes"
    ## [133] "Yes" "Yes" "Yes" "No"  "No"  "No"  "Yes" "Yes" "Yes" "No"  "Yes" "No" 
    ## [145] "No"  "No"  "No"  "No"  "No"  "Yes" "Yes" "No"  "No"  "Yes" "Yes" "Yes"
    ## [157] "Yes" "No"  "No"  "No"  "Yes" "No"  "Yes" "No"  "No"  "No"  "Yes" "Yes"
    ## [169] "Yes" "No"  "No"  "Yes" "No"  "No"  "Yes" "No"  "No"  "Yes" "No"  "No" 
    ## [181] "Yes" "No"  "Yes" "No"  "No"  "No"  "No"  "Yes" "No"  "No"  "No"  "No" 
    ## [193] "Yes" "Yes" "No"  "Yes" "Yes" "No"  "No"  "No"  "No"  "No"  "No"  "No" 
    ## [205] "Yes" "No"  "No"  "Yes" "No"  "No"  "No"  "No"  "Yes" "No"  "No"

### specialisation

``` r
as.character(placement$specialisation)
```

    ##   [1] "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin"
    ##   [8] "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin"
    ##  [15] "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&HR" 
    ##  [22] "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR" 
    ##  [29] "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR" 
    ##  [36] "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&HR" 
    ##  [43] "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&Fin"
    ##  [50] "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&HR" 
    ##  [57] "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin"
    ##  [64] "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin"
    ##  [71] "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin"
    ##  [78] "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin"
    ##  [85] "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&Fin"
    ##  [92] "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin"
    ##  [99] "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR" 
    ## [106] "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&HR" 
    ## [113] "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR" 
    ## [120] "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin"
    ## [127] "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR" 
    ## [134] "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin"
    ## [141] "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR" 
    ## [148] "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin"
    ## [155] "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR" 
    ## [162] "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin"
    ## [169] "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin"
    ## [176] "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR" 
    ## [183] "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin"
    ## [190] "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin" "Mkt&HR" 
    ## [197] "Mkt&Fin" "Mkt&HR"  "Mkt&HR"  "Mkt&HR"  "Mkt&Fin" "Mkt&HR"  "Mkt&HR" 
    ## [204] "Mkt&HR"  "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&Fin"
    ## [211] "Mkt&Fin" "Mkt&Fin" "Mkt&Fin" "Mkt&HR"  "Mkt&HR"

### Check the class of placement data and convert it to character data type.

``` r
sapply(placement,class)
```

    ##          sl_no         gender          ssc_p          ssc_b          hsc_p 
    ##      "integer"       "factor"      "numeric"       "factor"      "numeric" 
    ##          hsc_b          hsc_s       degree_p       degree_t         workex 
    ##       "factor"       "factor"      "numeric"       "factor"       "factor" 
    ##        etest_p specialisation          mba_p         status         salary 
    ##      "numeric"       "factor"      "numeric"       "factor"      "integer"

``` r
as.character(placement)
```

    ##  [1] "1:215"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              
    ##  [2] "c(2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 1, 1, 2, 1, 2, 1, 1, 2, 2, 1, 1, 1, 2, 1, 2, 2, 2, 2, 1, 1, 1, 1, 2, 1, 2, 1, 1, 2, 1, 1, 2, 2, 1, 1, 1, 2, 2, 1, 1, 2, 1, 2, 1, 2, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 2, 1, 1, 2, 2, 1, 1, 2, 2, 2, 2, 1, 2, 2, 1, 1, 1, 2, 1, 2, 2, 2, 1, 1, 1, 2, 1, 2, 1, 2, 2, 2, 2, 2, 2, 2, 1, 2, 2, 1, 2, 1, 2, 2, 2, 2, 2, 1, 1, 2, 2, 1, 1, 1, 2, 2, 2, 1, 2, 2, 1, 1, 1, 2, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 1, 1, 2, \n2, 1, 2, 1, 2, 2, 1, 2, 2, 1, 1, 2, 1, 2, 2, 2, 2, 1, 1, 1, 2, 2, 1, 1, 2, 2, 1, 2, 2, 2, 1, 1, 2, 2, 2, 2, 2, 1, 2, 2, 2, 1, 2, 2, 2, 2, 1, 2)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ##  [3] "c(67, 79.33, 65, 56, 85.8, 55, 46, 82, 73, 58, 58, 69.6, 47, 77, 62, 65, 63, 55, 63, 60, 62, 79, 69.8, 77.4, 76.5, 52.58, 71, 63, 76.76, 62, 64, 67, 61, 87, 62, 69, 51, 79, 73, 81, 78, 74, 49, 87, 77, 76, 70.89, 63, 63, 50, 75.2, 54.4, 40.89, 80, 74, 60.4, 63, 68, 74, 52.6, 74, 84.2, 86.5, 61, 80, 54, 83, 80.92, 69.7, 73, 82, 75, 84.86, 64.6, 56.6, 59, 66.5, 64, 84, 69, 69, 81.7, 63, 84, 70, 83.84, 62, 59.6, 66, 84, 85, 52, 60.23, 52, 58, 73, 76, 70.5, 69, 54, 45, 63, 77, 73, 69, 59, 61.08, 82, 61, \n52, 69.5, 51, 58, 73.96, 65, 73, 68.2, 77, 76, 60.8, 58, 64, 66.5, 74, 67, 84, 79, 72, 80.4, 76.7, 62, 74.9, 67, 73, 77.44, 72, 47, 67, 82, 77, 65, 66, 85, 77.67, 52, 89.4, 62, 70, 77, 44, 71, 65, 75.4, 49, 53, 51.57, 84.2, 66.5, 67, 52, 87, 55.6, 74.2, 63, 67.16, 63.3, 62, 67.9, 48, 59.96, 63.4, 80, 73, 52, 73.24, 63, 59, 73, 68, 77.8, 65, 62, 52, 65, 56.28, 88, 52, 78.5, 61.8, 54, 64, 67, 65.2, 60, 52, 66, 72, 83.96, 67, 69, 69, 54.2, 70, 55.68, 74, 61, 41, 83.33, 43, 62, 80.6, 58, 67, 74, 62)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     
    ##  [4] "c(2, 1, 1, 1, 1, 2, 2, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 1, 1, 1, 1, 2, 2, 1, 1, 1, 2, 2, 1, 2, 2, 2, 2, 1, 2, 1, 2, 2, 1, 1, 2, 2, 1, 1, 2, 1, 1, 1, 1, 1, 2, 2, 2, 2, 2, 2, 1, 1, 2, 2, 2, 1, 1, 1, 2, 2, 2, 1, 2, 2, 1, 2, 1, 2, 2, 1, 1, 2, 2, 1, 1, 1, 1, 1, 1, 1, 1, 1, 2, 1, 2, 1, 1, 1, 2, 2, 1, 1, 1, 2, 2, 2, 1, 2, 1, 2, 1, 1, 2, 1, 1, 2, 1, 1, 2, 2, 1, 1, 1, 2, 2, 1, 1, 1, 1, 2, 2, 1, 1, 1, 1, 2, 2, 2, 1, 1, 1, 1, 1, 1, 2, 2, 1, 2, 1, 1, 2, 1, 1, 2, 1, 2, 1, 1, 2, \n2, 1, 2, 2, 2, 2, 2, 2, 2, 1, 1, 2, 1, 1, 1, 2, 1, 2, 1, 1, 1, 2, 1, 2, 2, 1, 1, 2, 1, 2, 2, 1, 2, 2, 1, 1, 2, 2, 2, 1, 1, 1, 1, 2, 2, 2, 2, 1)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ##  [5] "c(91, 78.33, 68, 52, 73.6, 49.8, 49.2, 64, 79, 70, 61, 68.4, 55, 87, 47, 75, 66.2, 67, 66, 67, 65, 76, 60.8, 60, 97.7, 54.6, 79, 67, 76.5, 67, 73.5, 53, 81, 65, 51, 78, 44, 76, 58, 68, 77, 63.16, 39, 87, 73, 64, 71.98, 60, 62, 37, 73.2, 61.12, 45.83, 70, 60, 66.6, 71.4, 76, 62, 65.58, 70, 73.4, 64.2, 70, 73, 47, 74, 78.5, 47, 73, 61, 70.29, 67, 83.83, 64.8, 62, 70.4, 80, 90.9, 62, 62, 63, 67, 79, 63, 89.83, 63, 51, 62, 75, 90, 57, 69, 62, 62, 78, 70, 62.5, 73, 82, 57, 72, 61, 78, 63, 64, 50, 90, \n82, 63, 70, 54, 61, 79, 68, 63, 72.8, 75, 80, 68.4, 40, 67, 66.8, 59, 71, 73, 61, 60, 73.4, 89.7, 65, 57, 68, 64, 92, 56, 59, 63, 64, 70, 64.8, 64, 60, 64.89, 50, 65.66, 63, 74, 86, 58, 58.66, 65, 60.5, 59, 63, 74.66, 69.4, 62.5, 63, 49, 74, 51, 87.6, 67, 72.5, 78.33, 62, 62, 51, 42.16, 67.2, 80, 58, 52, 50.83, 62, 60, 97, 56, 64, 71.5, 60.33, 65, 77, 62.83, 72, 64, 65.5, 47, 77.6, 70.2, 61, 61.4, 63, 55, 76, 63, 53, 70, 65, 60, 63, 63, 61.33, 73, 62, 42, 78, 60, 72, 82, 60, 67, 66, 58)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 
    ##  [6] "c(2, 2, 1, 1, 1, 2, 2, 1, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 1, 1, 1, 1, 2, 2, 1, 1, 1, 2, 2, 2, 2, 1, 2, 2, 1, 2, 1, 2, 2, 1, 1, 2, 2, 2, 2, 2, 1, 2, 2, 1, 1, 2, 2, 2, 2, 2, 2, 1, 1, 2, 2, 2, 2, 1, 2, 1, 2, 2, 1, 2, 2, 1, 2, 2, 2, 2, 1, 1, 2, 2, 1, 1, 1, 1, 2, 1, 2, 1, 2, 2, 1, 2, 1, 2, 2, 2, 2, 1, 2, 1, 2, 2, 2, 2, 2, 1, 2, 1, 1, 2, 2, 1, 2, 1, 1, 2, 2, 1, 2, 2, 2, 2, 2, 2, 2, 1, 1, 2, 1, 2, 1, 2, 2, 2, 2, 2, 1, 1, 1, 1, 1, 1, 2, 2, 2, 1, 1, 2, 2, 1, 2, 2, 2, 1, 2, 2, \n2, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 1, 2, 1, 1, 1, 2, 2, 1, 1, 1, 1, 2, 1, 2, 2, 1, 2, 2, 2, 1, 2, 2, 2, 1, 2, 2, 1, 2, 2, 2, 2, 2)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ##  [7] "c(2, 3, 1, 3, 2, 3, 2, 3, 2, 2, 2, 2, 3, 2, 2, 2, 2, 2, 2, 1, 2, 2, 3, 3, 3, 2, 2, 2, 2, 2, 2, 3, 2, 3, 3, 2, 2, 3, 3, 3, 2, 2, 3, 2, 2, 3, 3, 2, 2, 1, 3, 2, 2, 3, 3, 3, 2, 2, 3, 3, 3, 2, 3, 2, 2, 3, 3, 2, 2, 3, 3, 2, 3, 2, 2, 2, 1, 3, 3, 3, 2, 3, 2, 3, 3, 2, 2, 3, 2, 3, 2, 2, 3, 2, 2, 2, 3, 2, 2, 2, 2, 2, 2, 3, 3, 3, 3, 2, 2, 3, 3, 3, 2, 2, 3, 3, 2, 3, 3, 2, 3, 3, 1, 2, 3, 2, 3, 3, 3, 2, 2, 3, 2, 2, 2, 3, 1, 2, 3, 2, 2, 3, 3, 2, 1, 3, 3, 2, 1, 1, 3, 2, 3, 3, 3, 2, 3, 2, 3, 2, 3, 2, 2, 3, 2, 2, 2, \n3, 2, 3, 2, 2, 2, 3, 3, 3, 2, 2, 3, 3, 2, 3, 1, 2, 2, 3, 2, 3, 2, 2, 2, 3, 2, 1, 2, 2, 3, 3, 2, 2, 2, 3, 3, 2, 2, 2, 3, 2, 3, 2, 2, 3, 2, 2, 3)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ##  [8] "c(58, 77.48, 64, 52, 73.3, 67.25, 79, 66, 72, 61, 60, 78.3, 65, 59, 50, 69, 65.6, 64, 64, 70, 66, 85, 72.23, 64.74, 78.86, 50.2, 66, 66, 67.5, 58, 73, 65, 66.4, 81, 52, 72, 57, 65.6, 66, 64, 80, 65, 65, 68, 81, 72, 65.6, 57, 68, 52, 68.4, 56.2, 53, 72, 69, 65, 61.4, 74, 68, 72.11, 72, 66.89, 67.4, 64, 75, 57, 66, 67, 72.7, 66, 62, 71, 78, 71.72, 70.2, 77.5, 71.93, 65, 64.5, 66, 69, 67, 74, 68, 70, 77.2, 64, 60, 73, 69, 82, 50.8, 66, 54, 64, 65, 76, 61, 65, 63, 58, 68, 68, 73, 65, 58, 54, 83, 69, \n65, 72, 61, 61, 67, 69, 66, 66.6, 73, 78, 64.6, 59, 69.6, 69.3, 73, 64.33, 73, 75.5, 69, 77.72, 66, 60, 62, 64, 77, 72, 69, 64, 72, 73, 59, 69.5, 60, 73.43, 70.67, 61, 71.25, 66, 65, 56, 55, 58, 75, 84, 65, 60, 59.9, 65, 60.9, 64, 58, 65, 57.5, 77.25, 64, 63.35, 74, 60, 67, 58, 61.26, 60, 72, 56, 55, 64.27, 65, 56, 79, 68, 64.2, 62.8, 64.21, 57, 69, 59.79, 78, 61, 67, 54.38, 69.2, 61, 72, 64.8, 56, 56.3, 72, 77.5, 91, 65, 57, 65, 58, 66, 56.87, 73, 65, 60, 61, 65, 65, 77.6, 72, 73, 58, 53)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              
    ##  [9] "c(3, 3, 1, 3, 1, 3, 1, 3, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 3, 3, 3, 1, 1, 1, 1, 1, 1, 3, 1, 1, 2, 1, 1, 3, 1, 3, 1, 1, 2, 1, 1, 3, 1, 1, 1, 2, 1, 1, 1, 3, 1, 1, 1, 1, 1, 3, 1, 1, 3, 1, 1, 1, 1, 1, 3, 3, 3, 1, 1, 1, 1, 1, 1, 3, 3, 3, 1, 1, 1, 3, 3, 1, 1, 2, 1, 3, 1, 1, 1, 1, 1, 1, 1, 1, 1, 3, 1, 1, 1, 3, 1, 3, 3, 1, 1, 3, 3, 3, 1, 1, 1, 1, 1, 3, 3, 1, 1, 3, 1, 1, 2, 1, 3, 1, 3, 1, 1, 2, 1, 1, 1, 1, 1, 1, 3, 1, 1, 1, 3, 1, 1, 3, 1, 1, 2, 1, 3, 1, 3, 3, 1, 1, 3, 1, 3, 1, 3, 1, 1, 3, 1, 1, 1, \n3, 1, 3, 1, 1, 1, 3, 3, 3, 1, 1, 3, 3, 1, 3, 2, 1, 1, 2, 1, 3, 1, 1, 1, 1, 1, 2, 1, 1, 3, 3, 2, 1, 1, 1, 3, 1, 1, 1, 1, 1, 1, 1, 1, 3, 1, 1, 1)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ## [10] "c(1, 2, 1, 1, 1, 2, 1, 2, 1, 1, 2, 2, 1, 1, 1, 2, 2, 1, 1, 2, 1, 1, 1, 2, 1, 2, 2, 1, 2, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 2, 1, 1, 2, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 2, 2, 1, 2, 2, 2, 1, 1, 1, 2, 1, 1, 1, 1, 1, 2, 2, 1, 1, 1, 2, 1, 2, 2, 2, 1, 1, 1, 1, 2, 1, 1, 1, 1, 1, 1, 2, 1, 2, 2, 1, 2, 2, 2, 2, 1, 2, 1, 2, 2, 1, 2, 2, 2, 2, 1, 1, 1, 2, 2, 2, 1, 2, 1, 1, 1, 1, 1, 1, 2, 2, 1, 1, 2, 2, 2, 2, 1, 1, 1, 2, 1, 2, 1, 1, 1, 2, \n2, 2, 1, 1, 2, 1, 1, 2, 1, 1, 2, 1, 1, 2, 1, 2, 1, 1, 1, 1, 2, 1, 1, 1, 1, 2, 2, 1, 2, 2, 1, 1, 1, 1, 1, 1, 1, 2, 1, 1, 2, 1, 1, 1, 1, 2, 1, 1)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ## [11] "c(55, 86.5, 75, 66, 96.8, 55, 74.28, 67, 91.34, 54, 62, 60, 62, 68, 76, 72, 60, 60, 68, 50.48, 50, 95, 55.53, 92, 97.4, 76, 94, 68, 73.35, 77, 52, 64, 50.89, 88, 68.44, 71, 64, 58, 53.7, 93, 60, 65, 63, 95, 89, 58, 68, 78, 64, 65, 65, 67, 71.2, 87, 78, 71, 68, 80, 74, 57.6, 60, 61.6, 59, 68.5, 61, 89.69, 68.92, 68.71, 79, 70, 89, 95, 95.5, 86, 84.27, 74, 61, 69, 86.04, 75, 67, 86, 82, 84, 55, 78.74, 67, 75, 58, 62, 92, 67, 72, 72, 53.88, 95.46, 66, 93.91, 70, 50, 56.39, 78, 57.5, 85, 55, 85, 71, \n80, 84, 86, 57.2, 60, 58, 72.15, 53.7, 89, 96, 80, 97, 82.66, 73, 55.67, 80.4, 60, 64, 75, 70, 55.5, 81.2, 90, 84, 80, 74.4, 65, 94, 55.6, 78, 56, 96, 58, 56, 60, 60, 89, 60, 72, 85, 83, 57, 64.25, 56, 83, 98, 86, 70, 56.15, 80, 93.4, 60, 62, 75, 57.63, 75.2, 75, 53.04, 80, 63, 58.1, 60, 54.48, 58.06, 63.79, 84, 67, 64, 87.5, 55, 89, 73, 75.5, 57, 63, 75, 60, 60, 82, 55, 95, 57, 95.65, 50, 72, 93.4, 80, 59, 84, 78, 59.32, 88, 73, 87.55, 79, 61.28, 66, 80, 62, 97, 88.56, 92.66, 67, 91, 74, 59, 70, \n89)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 
    ## [12] "c(2, 1, 1, 2, 1, 1, 1, 1, 1, 1, 2, 1, 2, 1, 2, 1, 1, 1, 2, 1, 2, 1, 2, 1, 1, 1, 1, 2, 1, 1, 2, 2, 2, 1, 2, 2, 1, 2, 2, 1, 1, 2, 1, 2, 1, 2, 2, 1, 1, 2, 2, 2, 2, 2, 2, 2, 1, 1, 1, 1, 1, 1, 1, 2, 1, 2, 2, 1, 2, 1, 1, 1, 1, 1, 1, 2, 1, 1, 1, 2, 2, 1, 1, 1, 1, 1, 1, 2, 2, 2, 1, 2, 1, 2, 1, 1, 1, 1, 1, 1, 2, 2, 1, 2, 2, 2, 1, 2, 1, 2, 2, 2, 2, 1, 2, 1, 1, 1, 2, 1, 2, 2, 1, 2, 2, 1, 1, 2, 2, 1, 1, 1, 2, 2, 1, 2, 1, 2, 1, 1, 1, 2, 1, 1, 1, 2, 2, 1, 1, 2, 1, 1, 1, 1, 1, 2, 2, 1, 1, 2, 2, 2, 1, 1, 1, 1, 2, \n1, 2, 2, 2, 1, 2, 2, 1, 2, 2, 1, 2, 2, 1, 2, 1, 2, 2, 2, 1, 1, 1, 1, 1, 1, 1, 2, 1, 2, 1, 2, 2, 2, 1, 2, 2, 2, 1, 1, 1, 1, 2, 1, 1, 1, 1, 2, 2)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ## [13] "c(58.8, 66.28, 57.8, 59.43, 55.5, 51.58, 53.29, 62.14, 61.29, 52.21, 60.85, 63.7, 65.04, 68.63, 54.96, 64.66, 62.54, 67.28, 64.08, 77.89, 56.7, 69.06, 68.81, 63.62, 74.01, 65.33, 57.55, 57.69, 64.15, 51.29, 56.7, 58.32, 62.21, 72.78, 62.77, 62.74, 51.45, 55.47, 56.86, 62.56, 66.72, 69.76, 51.21, 62.9, 69.7, 66.53, 71.63, 54.55, 62.46, 56.11, 62.98, 62.65, 65.49, 71.04, 65.56, 52.71, 66.88, 63.59, 57.99, 56.66, 57.24, 62.48, 59.69, 59.5, 58.78, 57.1, 58.46, 60.99, 59.24, 68.07, 65.45, 66.94, 68.53, \n59.75, 67.2, 67, 64.27, 57.65, 59.42, 67.99, 62.35, 70.2, 60.44, 66.69, 62, 76.18, 57.03, 59.08, 64.36, 62.36, 68.03, 62.79, 59.47, 55.41, 54.97, 62.16, 64.44, 69.03, 57.31, 59.47, 64.95, 60.44, 61.31, 65.83, 58.23, 55.3, 65.69, 73.52, 58.31, 56.09, 54.8, 60.64, 53.94, 63.08, 55.01, 60.5, 70.85, 67.05, 70.48, 64.34, 58.81, 71.49, 71, 56.7, 61.26, 73.33, 68.2, 58.4, 76.26, 68.55, 64.15, 60.78, 53.49, 60.98, 67.13, 65.63, 61.58, 60.41, 71.77, 54.43, 56.94, 61.9, 61.29, 60.39, 58.52, 63.23, 55.14, 62.28, \n64.08, 58.54, 61.3, 58.87, 65.25, 62.48, 53.2, 65.99, 52.72, 55.03, 61.87, 60.59, 72.29, 62.72, 66.06, 66.46, 65.52, 74.56, 52.38, 75.71, 58.79, 65.48, 69.28, 66.04, 52.64, 59.32, 66.23, 60.69, 57.9, 70.81, 68.07, 72.14, 56.6, 60.02, 59.81, 61.82, 57.29, 71.43, 62.93, 64.86, 56.13, 66.94, 62.5, 61.01, 57.34, 56.63, 64.74, 58.95, 54.48, 69.71, 71.96, 55.8, 52.81, 58.44, 60.11, 58.3, 67.69, 56.81, 53.39, 71.55, 62.92, 56.49, 74.49, 53.62, 69.72, 60.23, 60.22)"
    ## [14] "c(2, 2, 2, 1, 2, 1, 1, 2, 2, 1, 2, 2, 1, 2, 1, 2, 2, 1, 1, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 1, 2, 1, 2, 2, 1, 2, 1, 2, 2, 2, 2, 1, 1, 2, 2, 1, 1, 2, 2, 1, 2, 1, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 2, 1, 2, 1, 2, 2, 1, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 1, 2, 2, 1, 2, 2, 2, 2, 1, 2, 2, 2, 1, 2, 1, 2, 2, 2, 1, 2, 1, 1, 2, 2, 2, 2, 1, 1, 2, 2, 1, 2, 1, 2, 2, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 1, 2, 2, 2, 2, 1, 2, 2, 1, 2, 2, 2, 2, 1, 2, 2, 2, 2, 2, 1, 2, 2, 1, 1, 2, 1, 2, 2, 2, 1, 2, \n1, 1, 1, 1, 2, 2, 1, 2, 1, 2, 2, 2, 1, 2, 1, 1, 2, 1, 2, 1, 2, 1, 1, 1, 2, 2, 2, 1, 2, 2, 2, 1, 2, 2, 1, 2, 2, 2, 2, 1, 2, 1, 2, 2, 2, 2, 2, 1)"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           
    ## [15] "c(270000, 200000, 250000, NA, 425000, NA, NA, 252000, 231000, NA, 260000, 250000, NA, 218000, NA, 200000, 300000, NA, NA, 236000, 265000, 393000, 360000, 300000, 360000, NA, 240000, 265000, 350000, NA, 250000, NA, 278000, 260000, NA, 300000, NA, 320000, 240000, 411000, 287000, NA, NA, 300000, 200000, NA, NA, 204000, 250000, NA, 200000, NA, NA, 450000, 216000, 220000, 240000, 360000, 268000, 265000, 260000, 300000, 240000, NA, 240000, NA, 275000, 275000, NA, 275000, 360000, 240000, 240000, 218000, \n336000, NA, 230000, 500000, 270000, NA, 240000, 300000, NA, 300000, 300000, 400000, 220000, NA, 210000, 210000, 300000, NA, 230000, NA, 260000, 420000, 300000, NA, 220000, NA, NA, 380000, 300000, 240000, 360000, NA, NA, 200000, 300000, NA, 250000, NA, 250000, 280000, 250000, 216000, 300000, 240000, 276000, 940000, NA, 250000, 236000, 240000, 250000, 350000, 210000, 250000, 400000, 250000, NA, 360000, 300000, 250000, 250000, 200000, NA, 225000, 250000, 220000, 265000, NA, 260000, 300000, NA, 400000, \n233000, 300000, 240000, NA, 690000, 270000, 240000, 340000, 250000, NA, 255000, 300000, NA, NA, 300000, NA, 285000, 500000, 250000, NA, 240000, NA, NA, NA, NA, 290000, 300000, NA, 500000, NA, 220000, 650000, 350000, NA, 265000, NA, NA, 276000, NA, 252000, NA, 280000, NA, NA, NA, 264000, 270000, 300000, NA, 275000, 250000, 260000, NA, 265000, 300000, NA, 240000, 260000, 210000, 250000, NA, 300000, NA, 216000, 400000, 275000, 295000, 204000, NA)"
