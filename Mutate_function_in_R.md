Mutate function
================
Monalisa Roy

### Read the data,load libraries

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)

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

#### Add a column named ‘Age’ and assign a random value in customer churn dataset that lies within a range using sample()function based in the following conditions:

**If the customer is a senior citizen (SeniorCitizen==1),then the age
assigned to the customer lies between 56 and 100.** **If the customer is
not a senior citizen (SeniorCitizen==0),then the age assigned to the
customer lies between 16:55.**

``` r
mutate(customer,ifelse(SeniorCitizen==1,sample(56:100),sample(16:55)))->Age
View(Age)
```

#### Create a column named ‘Customer_Category’ based on the following condition.

**The customers whose monthly charges are less than 45 will be named as
’Low Paying’customers.** **The customers whose monthly charges are less
than 90 will be named as ’Medium Paying’customers.** **The customers
whose monthly charges are greater than 90 will be named as ’High
Paying’customers.**

``` r
mutate(customer,(LowPaying=MonthlyCharges<45),(MediumPaying=MonthlyCharges<90),(HighPaying=MonthlyCharges>90))->customer_category
View(customer_category)
```

#### Create a column named ‘Security’ based on the following condition.

**The customers who have opted for ‘Online Security’ will be marked as
‘Secure’.** **The customers who have not opted for ‘Online Security’
will be marked as ‘Not Secure’.**

``` r
mutate(customer,ifelse(OnlineSecurity=="Yes","Secure","Not Secure"))->Security
View(Security)
```
