For Loop
================
Monalisa Roy

### Read the data,load libraries

``` r
placement=read.csv("Placement_Data_Full_Class.csv",stringsAsFactors = T)

customer=read.csv("customer-churn",stringsAsFactors = T)
```

### Using for loop, calculate the number of students from the placement dataset according to the following condition:

## students who are placed.

``` r
count=0
for( i in 1:nrow(placement)){
  if(placement$status[i]=="Placed"){
    count=count+1
  }
}
count
```

    ## [1] 148

## Students who are from Science stream.

``` r
count=0
for(i in 1:nrow(placement)){
  if(placement$hsc_s[i]=="Science"){
    count=count+1
  }
}
count
```

    ## [1] 91

## Students who are from Commerce stream.

``` r
count=0
for(i in 1:nrow(placement)){
  if(placement$hsc_s[i]=="Commerce"){
    count=count+1
  }
}
count
```

    ## [1] 113

### Using for loop, calculate the number of students from the placement dataset who score more than 80.0 in higher secondary exams.

``` r
count=0
for(i in 1:nrow(placement)){
  if(placement$hsc_p[i]>80){
    count=count+1
  }
}
count
```

    ## [1] 18

### Calculate the number of students who scored more than 75% in MBA(mba_p)and got placed from campus placement drives.

``` r
count=0
for(i in 1:nrow(placement)){
  if(placement$mba_p[i]>75 & placement$status[i]=="Placed"){
    count=count+1
  }
}
count
```

    ## [1] 3

### Calculate the number of seniorcitizens from customer churn dataset who are using InternetService as ‘DSL’.

``` r
count=0
for(i in 1:nrow(customer)){
  if(customer$SeniorCitizen[i]==1 & customer$InternetService[i]=="DSL"){
    count=count+1
  }
}
count
```

    ## [1] 259
