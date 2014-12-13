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

Next, we will get the first few rows of the data


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


## What is mean total number of steps taken per day?

To calculate the mean total number of steps taken per day we first must find the total steps taken per day. We must also make sure to remove "NA" values before we can calculate the sum. This code chuck will calculate the steps per day and output the head of the new dataset which includes the total steps per day.


```r
steps_per_day <- tapply(na.omit(activity)$steps, list(na.omit(activity)$date), sum)
head(steps_per_day)
```

```
## 2012-10-02 2012-10-03 2012-10-04 2012-10-05 2012-10-06 2012-10-07 
##        126      11352      12116      13294      15420      11015
```

Create a histogram of the total steps taken per day.


```r
hist(steps_per_day, breaks=25, col="red", main="Total Steps Per Day", xlab="The Total Steps Per Day", ylab="Frequency")
```

![](./PA1_template_files/figure-html/unnamed-chunk-4-1.png) 

Find the mean and median of steps per day.   


```r
mean(steps_per_day, na.rm=TRUE)
```

```
## [1] 10766.19
```

```r
median(steps_per_day, na.rm=TRUE)
```

```
## [1] 10765
```

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?