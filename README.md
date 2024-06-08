# AB test analysis
Executive Summary:
This report presents the results of an AB test conducted to assess the impact of a new user interface on the conversion rate of a digital platform.
The objective of the test was to determine whether the new user interface leads to a statistically significant improvement in the conversion rate
compared to the old interface.
Link to tableau dashboard
https://public.tableau.com/app/profile/samuel.obadan/viz/ABtestsample/GlowboxABtest

# Methodology:
Test Duration: The AB test was conducted over a period of two weeks, starting on [25th Jan 2023] and ending on [6th Feb 2023].
Participants: A random sample of [Number of Participants] users was selected for the test, with approximately [50%] exposed to the new user
interface (Group B- Treatment group in orange  and approximately [50%] using the old interface (Group A – Control group in blue

Metric: The primary metric of interest was the conversion rate, which measures the percentage of users who completed the desired action (e.g.,
signing up, making a purchase) on the platform.
![Binomial](https://github.com/indexsam/ABtest_Analytics/blob/master/binomial.PNG)

![Result](https://github.com/indexsam/ABtest_Analytics/blob/master/results.PNG)

# Power analysis:
The minimum population for both A and B groups for a possible 1% increase in conversion rate is 5104. With a population of approximately
24,000 for each group, we thus satisfy the minimum requirement.
Sanity check:
With a P-value > 0.01, we conclude that a ‘Sample Ratio Mismatch’ (SRM) is unlikely. Thus, there exist a fine balance between the control
group population and the treatment group population.
Power divergence Result (statistic=1.3495086120589257, p-value=0.24536404027139797)
SRM likely not present

![simpson paradox](https://github.com/indexsam/ABtest_Analytics/blob/master/simpson.PNG)

We have detected Simpson's paradox even when the counts between the two groups and their subgroups are proportional. Simpson's paradox is a statistical phenomenon in which a trend appears in different groups of data, but disappears or reverses when these groups are combined.

I suspect there is a confounding variable that affects the “others” devices that needs to be taken into account. We find the average spent (purchase) to be twice as much in the control group than in the treatment group.

![Maos](https://github.com/indexsam/ABtest_Analytics/blob/master/maps.PNG)

Most of this purchase has come from Mexico (The darkest green dot on the map), which also is the country with the third
highest number of users. They may exist confounding variables such as events in Mexico during the run of the simulation which may need further investigation especially between 26th of January to 28th of January

![Novelty](https://github.com/indexsam/ABtest_Analytics/blob/master/novelty.PNG)

While the randomness among both groups suggest that there are no novelty effects in both conversion rate the average purchase (spent) amount  for both groups, we however observe a novelty effect trend in both the control and treatment
groups when taking into account the total amount of money spent (purchases) during the experiment, for the period.

# Conclusion:
Conversion Rate
Based on the results of the AB test, the new user interface led to a [statistically significant] improvement in the conversion rate compared to the old interface. The conversion rate for the new user interface group was [4.63] %, while the conversion rate for the old interface group was [3.92]%. This suggests that the new user interface positively impacted user engagement and interaction with the platform.

Purchase rate
Based on the results of the AB test, the new user interface led to a [non-statistically significant] improvement in the purchase mean compared to the old interface. The conversion rate for the new user interface group was [$3.37], while the purchase mean for the old interface group was [$3.39]. Consequently, we cannot conclude at this moment that there exist a significant difference in the spending (purchase means) between the control and treatment groups. 

# Recommendation:
Despite the overall improvements in conversion rate, with the presence of a possible novelty effect and Simpsons’ paradox in the observations, it is recommended that we delay the implementation of the new interface subject to further investigations.

1. Long-Term Analysis: Towards the end of the second week, the novelty effect seems to begin to plateau. Thus it is recommended that we analyse the experiment over an extended period to determine if the initial increase is temporary or a lasting effect.
   
3. Explore Other Variables: In order to find a possible cause for the Simpson’s paradox, we need to consider whether there are other variables or factors at play especially in Mexico that could be influencing the increase in spending average especially in the controlled group A. It's important to examine other potential explanations for the observed change in this behaviour within the 26th of January to the 28th of January which showed a lower conversion rate in the control group A but significantly higher amount of aggregated sum of money spent (purchases) asindicated by the thickness of the blue line







