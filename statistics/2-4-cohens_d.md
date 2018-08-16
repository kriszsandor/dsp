[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 
#Problem
Exercise 2.4 Using the variable 'totalwgt_lb', investigate whether first babies are lighter or heavier than others. Compute Cohen’s d to quantify the difference between the groups. How does it compare to the difference in pregnancy length?

#Answer
Based on the statistics below first and other babies are born with only marginally different weight from each other. The difference in pounds is 0.12, with heavier babies being slightly more present among 'first' ones, however when compared to the standard deviance using Cohen d, the difference in means only translates to 0.09 standard deviations. This is slightly higher than for the lenghts of the pregnancy but still seems very small.

#Summary statistics results
Live mean 7.265628457623368
Live variance 1.9832904288326532
Live std 1.4082934455690168
Mean
First babies 7.201094430437772
Others 7.325855614973262
Variance
First babies 2.0180273009157768
Others 1.9437810258964572
Difference in pounds -0.12476118453549034
Difference in gramms -56.59067521582213
Cohen d -0.088672927072602

#Python code

mean = live.totalwgt_lb.mean()
var = live.totalwgt_lb.var()
std = live.totalwgt_lb.std()

print('Live mean', mean)
print('Live variance', var)
print('Live std', std)

mean1 = firsts.totalwgt_lb.mean()
mean2 = others.totalwgt_lb.mean()

var1 = firsts.totalwgt_lb.var()
var2 = others.totalwgt_lb.var()

print('Mean')
print('First babies', mean1)
print('Others', mean2)

print('Variance')
print('First babies', var1)
print('Others', var2)

print('Difference in pounds', mean1 - mean2)
print('Difference in gramms', (mean1 - mean2) * 453.592)

d = thinkstats2.CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
print('Cohen d', d)
