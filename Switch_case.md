Switch Case
================
Monalisa Roy

### Read the data,load libraries

``` r
customer=read.csv("customer-churn",stringsAsFactors = T)
View(customer)

placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)
View(placement)
```

### Using switch case, check 67th row of hsc_s column from placement data:

**if it’s “Science”, then add 5 extra marks in degree_p score.** **if
it’s “Commerce”,then add 3 extra marks in degree_p score.**

``` r
switch(as.character(placement$hsc_s[67]),"Science"=placement$degree_p[67]+5,"Commerce"=placement$degree_p[67]+3)->placement$degree_p[67]

View(customer)
```

### Check 74th row of ssc_b column in the placement dataset:

**if it’s “Others”,then add 3 as grace marks in hsc_p for the 74th
row.** **if it’s “Central”,then add 5 as grace marks in hsc_p for the
74th row.**

``` r
switch(as.character(placement$ssc_b[74]),"Others"=placement$hsc_p[74]+3,"Central"=placement$hsc_p[74]+5)->placement$hsc_p[74]
View(customer)
```

### Using switch case, check 4th row of contract column from customer churn data:

**If it is “One Year”, then give a 20% discount in total charges.** **If
it is “Month-to-month”, then give a discount of 5% in total charges.**

``` r
switch(as.character(customer$Contract[4]),"One year"=customer$TotalCharges[4]*0.8,"Month-to-month"=customer$TotalCharges[4]*0.95)->customer$TotalCharges[4]
View(customer)
```

###Check 14th row of Internet Service column in the customer churn
datasset: **If the customer is using “Fiber optic”, then give a discount
of 15% in total charges.** **If it is “DSL”, then give a discount of 10%
in total charges.**

``` r
switch(as.character(customer$InternetService[14]),"Fiber optic"=customer$TotalCharges[14]*0.85,"DSL"=customer$TotalCharges[14]*0.9)->customer$TotalCharges[14]
View(customer)
```
