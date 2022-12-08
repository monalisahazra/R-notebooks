If-Else
================
Monalisa Roy

## Read the data,load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
View(placement)

customer=read.csv("customer-churn",stringsAsFactors = T)
View(customer)
```

## Using the placement dataset, perform the following tasks.

-   Check the value of 95th row of status column.
-   if the value is “Placed”,then print “The student is placed from
    campus plament drives”.
-   if it is “Not PLaced”,then print “THe student is not placed from
    campus placement drives”.
-   if it’s “NA”, then print “The data of the student is not availabe”.

``` r
if(placement$status[95]=="Placed"){
  print("The student is placed from campus plament drives")
}else if(placement$status[95]=="Not Placed"){
  print("The student is not placed from campus placement drives")
}else{
  print("The data of the student is not availabe")
}
```

    ## [1] "The student is placed from campus plament drives"

## Check the value of 64th row of hsc_s column.

-   if it is “Science”,then print “The subject opted by the student is
    Science”.
-   if it is “Commerce”, then print “The subject opted by the student is
    Commerce”.
-   if it is “Arts”, then print “The subject opted by the student is
    Arts”

``` r
if(placement$hsc_s[64]=="Science"){
  print("The subject opted by the student is Science ")
}else if(placement$hsc_s[64]=="Commerce"){
  print("The subject opted by the student is Commerce")
    }else if(placement$hsc_s[64]=="Arts"){
      print("The subject opted by the student is Arts")
    
  
}else{
  print("The data of the student is not availabe")
}
```

    ## [1] "The subject opted by the student is Commerce"

## Check the 28th row of Payment method column:

-   if it’s “Credit card(automatic)”,then print “The customer is using
    credit card as their payment method”.
-   if it’s “Mailed check”, then print “The customer is using mailed
    check for payment”
-   if it’s “Electronic check”, then print “The customer is using
    electronic check for payment”

``` r
if(customer$PaymentMethod[28]=="Credit card(automatic)"){
  print("The customer is using credit card as their payment method ")
}else if(customer$PaymentMethod[28]=="Mailed check"){
  print("The customer is using mailed check for payment")
}else if(customer$PaymentMethod[28]=="Electronic check"){
  print("The customer is using electronic check for payment")
  
  
}else{
  print("The data of the customer is not availabe")
}
```

    ## [1] "The customer is using electronic check for payment"
