[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)


### Background
Cohen's D is an example of effect size. Other examples of effect size are: correlation between two variables, mean difference, regression coefficients and standardized test statistics such as: t, Z, F, etc. In this example, you will compute Cohen's D to quantify (or measure) the difference between two groups of data.

You will see effect size again and again in results of algorithms that are run in data science. For instance, in the bootcamp, when you run a regression analysis, you will recognize the t-statistic as an example of effect size.

### The Problem
**Exercise 4**   
*Using the variable totalwgt_lb, investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length?*

### Solution
Using the built-in function provided by Allen in his `thinkstat2` module, we compute:
  ```
  CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)  
-0.088672927072602006
```
Cohen's d for the difference in pregnancy lengths was:
```
CohenEffectSize(firsts.prglngth, others.prglngth)
0.028879044654449883
```
The effect of birth order on baby weight is larger than for pregnancy length, but it is still a small effect. (According to Cohen and [Sawilowsky](https://digitalcommons.wayne.edu/jmasm/vol8/iss2/26/), a *d* on the order of 0.01 is 'very small' and 0.20 is 'small').
