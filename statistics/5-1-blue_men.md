[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

This is a classic example of hypothesis testing using the normal distribution. The effect size used here is the Z-statistic.

### The Problem
*In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.*

### The Solution
Generate an analytic normal distribution using the mean and standard deviation of male height:
```Python3
import scipy.stats as stats

dist = stats.norm(loc=178, scale=7.7)

# convert heights to centimeters:
blue_min_ht = (5*12 + 10) * 2.54   
blue_max_ht = (6*12 + 1) * 2.54
```
The percent of men between 5'10" and 6'1" is equal to the difference in the evaluation of the CDF at these values:
```Python3
dist.cdf(blue_max_ht) - dist.cdf(blue_min_ht)

0.34274683763147457
```
