[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

Use the NSFG respondent variable numkdhh to construct the actual distribution for the number of children under 18 in the respondents' households.

Now compute the biased distribution we would see if we surveyed the children and asked them how many children under 18 (including themselves) are in their household.

Plot the actual and biased distributions, and compute their means

```python
resp = nsfg.ReadFemResp()
'''
to get pmf:
n = hist.Total()
d = {}
for x, freq in hist.Items():
  d[x] = freq / n

for bias pmf, multiply the probability by number of kids
'''
pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
biased = BiasPmf(pmf, label='biased')

thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf, biased])
thinkplot.Config(xlabel='Number of children', ylabel='PMF')

pmf.Mean()
biased.Mean()
```
* actual mean: 1.0242
* biased mean: 2.404

The biased mean is more than double the actual mean. Since the biased pmf multiplies by the number of kids, when there are 0 kids the biased probability of 0 kids is 0. 
