# Project Motivation

Most Markets **!=** the **Bean Machine** 

![Bean Machines](https://github.com/mattsinbox/pricing_with_non-normal_distributions/blob/master/bean_machine.jpg)

Most Markets are *NOT NORMAL* and have *WACKY* Distributions

# Problem
Pricing option prices or risk products when normality can not be assumed.  Most option market makers price at - the - money options well, but struggle with far out - of - the _ money options because the models used assume normality.  Black-Scholes models assume normality whenn pricing options.  Therefore when pricing out - of - the_ money options, many market makers take the at the money option volatility and apply a positive skew as you go further away from the current price.  This method does not have any statistical merrit and is more like a back of envelope calculation.  

# Solution
With today's computer power and data science techniques, I thought I could develop a model tht would accurately portray the distribution and therefore better price out of the money options.  This would be especially useful in markets where the distributions are far from normal like Bitcoin.  

# The Model
This model uses bootstrapping sampling techniques to price the options.  It takes historical data and samples percentage moves.  It then iterates this process and calculates the option price for each iteration.   It saves each iteration to a list and calculates the mean.  It therefore calculates each option price independent of each other and based on the **ACTUAL** distribtion displayed in the prices.  

# Other Uses
This technique can be used to examine any sample set or group of prices.  Instead of making assumptions on the distribtion, one can bootstrap and calculate pvalues or other statistics straight from the data.  Normality does not need to assumed.  


