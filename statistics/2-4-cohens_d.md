[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>>>Using the variable totalwgt_lb, investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

```python
def CohenEffectSize(group1, group2):
  diff = group1.mean() - group2.mean()
  var1 = group1.var()
  var2 = group2.var()
  n1, n2 = len(group1), len(group2)
  pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
  d = diff / np.sqrt(pooled_var)
  return d
CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
```
* cohen d: total weight: -0.0887
* cohen d: preg length: .0289

The cohen effect size is described as the difference in means expressed in numbers of standard deviations. So the difference in means of total weight is -0.0887 standard deviations. This means first babies tend to be lighter than others, but only slightly.

The difference of pregnancy lengths is .0289 standard deviations. So while total weight has more than double an effect than pregnancy length, they are both still very small. 
