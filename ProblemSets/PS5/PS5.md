# Problem Set 5: Basic Statistics

## Introduction

In this Problem Set, we will practice doing basic statistical analyses and visualizations in R with a health dataset.  

Going along with the examples from lectures we will use the data from the [Problem Set 5 folder](https://github.com/gwcbi/ResearchAnalytics/blob/master/ProblemSets/PS5/sepsis.csv) file.  Use read.csv or read_csv (from the tidyverse) to read/load the file into a data.frame or tibble variable.  Tell me how many samples (rows) and variables (columns) there are in the data.

Determine the percentage of missing values for each variable.  Report which two variables have the most missing data and what percentage is missing for each?

Use the table function to get and report a 2x2 table of counts for the fate (1=mortality 0=no mortality) and treat (1=ibuprofen, 0=placebo) combinations.

Use the fisher.test function (with the above table as input) from the stats library (this comes in base R and is already loaded) to test if there is a significant association between treatment and mortality with the variables treat and fate. Report the p-value and whether it is significant.

## 5 points extra credit
temp0 represents the baseline temperature at "time 0" for each sepsis patient.  temp2 represents their temperature after two hours of treatment.  Treatment is a variable "treat" where 1 means ibuprofen and 0 means placebo.  Create a new variable that is the change of temperature between temp0 and temp2.  Use this variable to determine if there is a significant association between treatment and change in temperature within two hours.  Report the p-value, if it is significant which treatment had a larger average change in temperature. This can be done as either a bivariate linear regression or as a two-sample t-test.  The regression can be performed using the lm function with the formula changetemp~dat$treat where changetemp is made by temp0-temp2 and dat is the name used when loading in the data. The p-value can be found by using the summary function on the saved model. A two-sample t-test can be done using the t.test function where the two arguments separate vectors of changetemp for treat==1 and for treat==0.


## The report

Submit your code as an R script along with clear answers to the course 2GW site. Make sure to add comments to your code so I know you know what you're doing! The answers can be in a separate file (pdf or word) or clearly noted in the script.

## Due date

Friday, Week 5
