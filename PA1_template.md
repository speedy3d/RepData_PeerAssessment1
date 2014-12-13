# Reproducible Research: Peer Assessment 1

This R Markdown document was created for Peer Assignment 1 for the COursera class Reproducible Research. 

## Loading and preprocessing the data

The folloowing code will read the data from the working directory and set the data type for each column


```r
activity <- read.csv("activity.csv", header=TRUE)
activity$steps <- as.numeric(activity$steps)
activity$date <- as.Date(activity$date)
activity$interval <- as.numeric(activity$interval)
```

Next, we will get the first few rows as well as a brief summary of the data


```r
head(activity)
```

```
##   steps       date interval
## 1    NA 2012-10-01        0
## 2    NA 2012-10-01        5
## 3    NA 2012-10-01       10
## 4    NA 2012-10-01       15
## 5    NA 2012-10-01       20
## 6    NA 2012-10-01       25
```

```r
summary(activity)
```

```
##      steps             date               interval     
##  Min.   :  0.00   Min.   :2012-10-01   Min.   :   0.0  
##  1st Qu.:  0.00   1st Qu.:2012-10-16   1st Qu.: 588.8  
##  Median :  0.00   Median :2012-10-31   Median :1177.5  
##  Mean   : 37.38   Mean   :2012-10-31   Mean   :1177.5  
##  3rd Qu.: 12.00   3rd Qu.:2012-11-15   3rd Qu.:1766.2  
##  Max.   :806.00   Max.   :2012-11-30   Max.   :2355.0  
##  NA's   :2304
```


## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
