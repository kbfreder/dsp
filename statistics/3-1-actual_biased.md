[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

### Background
This problem presents a robust example of actual vs biased data. As a data scientist, it will be important to examine not only the data that is available, but also the data that may be missing but highly relevant. You will see how the absence of this relevant data will bias a dataset, its distribution, and ultimately, its statistical interpretation.

### Problem
*Something like the class size paradox appears if you survey children and ask how many children are in their family. Families with many children are more likely to appear in your sample, and families with no children have no chance to be in the sample.
Use the NSFG respondent variable NUMKDHH to construct the actual distribution for the number of children under 18 in the household.*


### Solution
Construct the PMF for the actual number of children per family:
```
actual_pmf = thinkstats2.Pmf(resp.numkdhh, label='actual')
```
Use the provided function `BiasPmf` to construct the biased PMF:
```
bias_pmf = BiasPmf(actual_pmf, label='bias')
```
Overlay histograms of the two PMFs:
```
thinkplot.PrePlot(2)
thinkplot.Pmfs([actual_pmf, bias_pmf])
thinkplot.Config(xlabel='# children in family', ylabel='probability')
```
![Image of plot](https://github.com/kbfreder/dsp/blob/master/statistics/3-1-fig.png)
