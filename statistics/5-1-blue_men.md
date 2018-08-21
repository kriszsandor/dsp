[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

# Problem  
**Exercise 5.1:** In the BRFSS (see Section 5.4), the distribution of heights is roughly normal with parameters μ = 178 cm and σ = 7.7 cm for men, and μ = 163 cm and σ = 7.3 cm for women.
In order to join Blue Man Group, you have to be male between 5’10” and 6’1” (see http://bluemancasting.com). What percentage of the U.S. male population is in this range? Hint: use scipy.stats.norm.cdf.  

# Answer  
The answer depends if I take the original distribution and use CDF, or use the model distribution via scipy.stats.norm.
Using the original distribution ~55% of US male population is good for casting, if using the normal distribution the percentage is 38%. The book (in my judgement) uses the model std dev 7.7 wrongly as the US male population has a height std dev of ~7.3cm.


# Python code  
```python
thinkstats2.RandomSeed(17)

nrows=1000
nrows = int(nrows)    
df = ReadBrfss(nrows=nrows)

def imperial_to_metric(h_ft, h_inch): # return height in cm
    h_inch += h_ft * 12
    return round(h_inch * 2.54, 1)

high = cdf_height[imperial_to_metric(6,1)]
low = cdf_height[imperial_to_metric(5,10)]
low, high, high-low

import scipy.stats
mu = heights_male.mean()
sigma = math.sqrt(heights_male.var()) # 7.7 is a typo in the book, it is 7.3
dist = scipy.stats.norm(loc=mu, scale=sigma)
low = dist.cdf(imperial_to_metric(5,10))    # 5'10"
high = dist.cdf(imperial_to_metric(6,1))   # 6'1"
low, high, high-low
```