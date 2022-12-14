If-Else
================
Monalisa Roy

## Read the data,load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)

pharma=read.csv("Pharmacovigilance_audit_Data.csv",stringsAsFactors = T)

City_temp=read.csv("city_temperature.csv",stringsAsFactors = T)
```

## Using the placement dataset, perform the following tasks:

-   Check the value of 12th row of degree_t column, if the value is
    “Comm&Mgmt”,and then print “The student is of the stream Commerce
    and Management”.
-   Check the value of 23rd row of specialisation column, if the value
    is “Mkt&HR,then print”The specialisation of student is Marketing and
    Human Resource”
-   Check the 39th row of status column, if the value is “Placed”, then
    print “The student is placed from campus”

``` r
if(placement$degree_t[12]=="Comm&Mgmt"){
  print("The student is of the stream Commerce and Management")
}else if(placement$specialisation[23]=="Mkt&HR"){
  print("The specialisation of student is Marketing and Human Resource")
}else if(placement$status[39]=="Placed"){
  print("The student is placed from campus")
}else{
  print("No data available")
} 
```

    ## [1] "The student is of the stream Commerce and Management"

## Using the pharmacovigilance dataset, perform the following tasks:

-   Check the value of 37th row of Issues column, if the value is
    “Medication history documenting error”, then print “The patient’s
    medical record is missing”.

-   Check the value of 180th row of Issues column, if the value is
    “Unclear Route”, then print “The patient is having an unclear route
    of transmission”

-   Check the 220th row of Location ID column, if the value is
    “Location3”,then print “The location ID of the patient is
    Location3.”

``` r
if(pharma$Issues[37]=="Medication history documenting error"){
  print("The patient’s medical record is missing")
}else if(pharma$Issues[180]=="unclear route"){
  print("The patient is having an unclear route of transmission")
    
}else if(pharma$LocationID[220]=="Location3"){
  print("The location ID of the patient is Location3")
} 
```

    ## [1] "The patient is having an unclear route of transmission"

## Using the city temperature dataset, perform the following tasks:

-   Check the value of 11th row of Region column, if the value is
    “Africa”, then print “The region for which we are calculating
    average temperature is Africa”.
-   Check the value of row number 79961 of city column, if the value is
    “Conakry”, then print “The city for which we are calculating average
    temperature is Conakry”.
-   Check the value of 70th row of year column, if the value is
    “1995”,then prints”We are calculating average temperature for the
    year 1995”.

``` r
if(City_temp$Region[11]=="Africa"){
  print("The region for which we are calculating average temperature is Africa")
}else if(City_temp$City[79961]=="Conakry"){
  print("The city for which we are calculating average temperature is Conakry")
}else if(City_temp$Year[70]=="1995"){
  print("We are calculating average temperature for the year 1995")
}
```

    ## [1] "The region for which we are calculating average temperature is Africa"
