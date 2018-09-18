HW01\_nasaweather
================
Chenchen Guo
2018 Sep 15th

Load data
---------

Install tklhe nasaweather package firstly

``` r
library(nasaweather)
```

Data set: Storm
---------------

Information of data set storms of package nasaweather

``` r
str(storms)

head(storms)

ncol(storms)
nrow(storms)

summary(storms)
```

Variance of pressure
--------------------

Calculating the variance with one method and var function of pressure which belongs to storm data set

``` r
na_pres<- storms$pressure
length(na_pres)
max(na_pres)
min(na_pres)

ave<- (sum(na_pres)/(length(na_pres)))
diffs<- (na_pres-ave)
variance<- (sum(diffs^2)/(length(na_pres)-1))
variance

var(na_pres)
```

Plots
-----

Indicate the length of every storm of each year

``` r
str(storms)
plot(storms$year,storms$day)
plot(storms$year,storms$hour)
```
