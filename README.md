# Autolib-Hypothesis-Testing-Project

Problem Statement

Autolib was an electric car sharing service which was inaugurated in Paris, France, in December 2011. However it was closed on July 31st 2018.It was operated by the Bellore industrial group. As of 3 July 2016, 3,980 Bluecars had been registered for the service, and the scheme had more than 126,900 registered subscribers.
I will be look into autolib data contained in ‘autolib_daily_events_postal_code.csv’ file’
I will be investigating the variable ‘Postal code’. I want to investigate if there is any difference between the average number of Blue cars being taken in areas with Postal code 75015 and 75017.
My hypothesis looks like this:
Ho: There is no difference between the average number of Blue cars taken in areas with postal code 75015 and 75017 
Ha: The mean of Blue cars taken in areas with postal code 75015 and 75017 is different
Level of significance =0.05
What has led me to come up with this hypothesis is that the exploratory data analysis with Time series has shown close to a similar pattern with both Postal code 75015 and 75017.
 The reason as to why this hypothesis is important is because it will help me understand which areas have embraced this product. This will in turn be communicated to the relevant personnel who will now be in a position to understand how the product is performing in various areas and make an informed decision on how to increase product acceptance to the people in specific regions.


Data Description

Datasets
    i.   Dataset (autolib_daily_events_postal_code.csv [http://bit.ly/DSCoreAutolibDataset]
   ii.   Dataset description [Link]  
Assumptions
The data provided is correct
The data has a normal distribution
Constraints
There are no constraints

The specific variables I am working with are Postal code, Blue cars taken sum.
What has led me to come up with this hypothesis is that the exploratory data analysis with Time series has shown close to a similar pattern with both Postal code 75015 and 75017.
Postal code field has a variety of postal code, but I choose to focus on these two postal codes; 75015 and 75017, reason being their time series trend seemed have similarities. There I want to investigate if the average number of blue cars taken is the same or not.
The sample mean for blue cars taken in postal code 75015 is: 908.5
The sample mean for blue cars taken in postal code 75017 is: 775.5
We can see that the sample mean are different, But the question is, is this difference in the mean statistically significant or was it just due to random chance?

Hypothesis Testing Procedure

The argument behind my null hypothesis is this: the status quo is that there is not difference between the blue cars taken in areas with postal codes 75015 and 75017.
My alternative hypothesis is a claim that even if the EDA on time series show similarities in the graph, the average number of blue cars taken might not be the same in the areas with postal code 75015 and 75017.
Procedure for Hypothesis Testing.
i.	I filtered my dataset to the following specific fields: Blue Cars taken sum, Postal code. I further filtered my data frame to have only the two Postal codes 75015 and 75017.
ii.	From my filtered data frame, I selected a sample with a proportion of 10% from the filtered data frame.
iii.	I used stratified sampling technique to ensure that the random sample I get will be a mirror reflection of the population
iv.	I used two sample independent T test to compare between the two sample means for postal code 75015 and 75017.
v.	For us to conduct the two sample independent test, the following assumptions must hold:
vi.	The distribution of the residual between the two groups should follow the normal distribution, 
vii.	To check this, I plotted histogram to see whether the distribution followed a normal distribution or not. I also used shspiro-wilks test as well to check for normality.
Observations
Using a histogram, I observed that the distribution was close to a bell shaped
Shapiro-wilks normality test proved that the sample distribution was not a normal.
Nevertheless, I continued with the hypothesis testing for demonstration purposes.
Since I did not want a high margin error, I used 0.05 as the level of significance

Hypothesis Testing Results

Results:  Ttest_indResult(statistic=2.2741134877028197, pvalue=0.030277872726882087)
The test returned a p value of 0.030277872726882087
Since alpha is 0.05, my confidence level will be 95%, meaning I am 95% confident that the sample means are different.
Since the p value is less than 0.05, we reject the null hypothesis 
Therefore, we have enough evidence to support that the sample means of Blue cars taken in areas with postal code 75015 and 75017 is statistically different (significant difference between the sample means)
The sample mean for blue cars taken in postal code 75015 is: 908.5
The sample mean for blue cars taken in postal code 75017 is: 775.5





Summary and Conclusions

Summary of the project
i.	Data cleaning
ii.	Univar ate analysis
iii.	Bivariate analysis
iv.	Hypothesis Testing
v.	Results
Results:  Ttest_indResult(statistic=2.2741134877028197, pvalue=0.030277872726882087)
The test returned a p value of 0.030277872726882087
Since alpha is 0.05, my confidence level will be 95%, meaning I am 95% confident that the sample means are different.
Since the p value is less than 0.05, we reject the null hypothesis 
Therefore we have enough evidence to support that the sample means of Blue cars taken in areas with postal code 75015 and 75017 is statistically different (significance difference between the sample means)



