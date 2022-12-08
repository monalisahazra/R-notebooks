Calculating Rows and Columns
================
Monalisa Roy

## Read the data,load libraries

``` r
pharma=read.csv("Pharmacovigilance_audit_Data.csv",stringsAsFactors = T)
View(pharma)
```

## Extract the following columns from the dataset:

-   Age and Issues

``` r
pharma[,c("Age","Issues")]->new_age
View(new_age)
```

-   Patient ID and Drug ID.

``` r
pharma[,c("PatientID","DrugID")]->new_data
View(new_data)
```

-   Gender, Age, Issues.

``` r
pharma[,c("Gender","Age","Issues")]->new_data1
View(new_data1)
```

## Extract the following rows:

-   Row numbers 1,2,3,4 and 5

``` r
pharma[c(1:5),]->new_row
View(new_row)
```

-   Rows from 15 to 75.

``` r
pharma[c(15:75),]->new_row1
View(new_row1)
```

-   Rows from 100-150.

``` r
pharma[c(100:150),]->new_row2
View(new_row2)
```

## Extract the following rows and columns:

-   Columns (1,2,4)and rows(1 to 10)

``` r
pharma[c(1:10),c(1,2,4)]->new_col_row
View(new_col_row)
```

-   columns(2,4,5)and rows(50 to 120)

``` r
pharma[c(50:120),c(2,4,5)]->new_col_row_1
View(new_col_row_1)
```

-   columns(1,3,6)and rows(100 to 200).

``` r
pharma[c(100:200),c(1,3,6)]->new_col_row_2
View(new_col_row_2)
```
