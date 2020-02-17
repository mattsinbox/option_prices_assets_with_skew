# Project Motivation

Most Markets **!=** the **Bean Machine** 

![Bean Machines](https://github.com/mattsinbox/pricing_with_non-normal_distributions/blob/master/bean_machine.jpg)



# Problem
Most Markets are *NOT NORMAL* and have *WACKY* Distributions.  Therefore pricing options can be difficult especially considering many strikes represent outliers which by definition contradict normality.  Most option market makers price at - the - money options well, but struggle with far out - of - the _ money options because the models assume normality.  Black-Scholes models assume normality when pricing options.  Therefore when pricing out - of - the_ money options, many market makers take the at the money option volatility and apply a simple linear skew.  This method does not have any statistical merrit and is more like a back of the envelope calculation.  

# Solution
With today's computer power and data science techniques, I built a model that portrays the actual distribution specific to the distribution.   It would therefore price out of the money options more accurately because it would not have to assume its distribution.  This would be especially useful in markets where the distributions are far from normal like Bitcoin.  

# The Model
This model uses bootstrapping sampling techniques to price the options.  It takes historical data and samples percentage moves.  It then iterates this process and calculates the option price for each iteration.   It saves each iteration to a list and calculates the mean.  It therefore calculates each option price independent of each other and based on the **ACTUAL** distribtion displayed in the prices.  

# Other Uses
This technique can be used to examine any sample set or group of prices.  Instead of making assumptions on the distribtion, one can bootstrap and calculate pvalues or other statistics straight from the data.  Normality does not need to assumed.  


