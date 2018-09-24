[Think Stats Chapter 6 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2007.html#toc60) (household income)

Compute the median, mean, skewness and Pearson’s skewness of the resulting sample. What fraction of households reports a taxable income below the mean? How do the results depend on the assumed upper bound?

Use InterpolateSample to create a sample of log10 household income. Then raise the sample to the 10th power to get back the household income in dollars.

```python
log_sample = InterpolateSample(income_df, log_upper=6.0)
sample = np.power(10, log_sample)

Mean(sample)
Median(sample)
Skewness(sample)
PearsonMedianSkewness(sample)

cdf.Prob(Mean(sample))
```
* Mean: 74278.70
* Median: 51226.45
* Skewness: 4.949
* PearsonMedianSkewness: 0.736

About 66% of households report taxable income below the mean. However, InterpolateSample assumed the highest income to be 1 million, and there are definately households that earn more than that.

Increasing the upper bound to 10 mill results in 98.6% of households reporting taxable income below the mean. So the upper bound has a huge impact 
