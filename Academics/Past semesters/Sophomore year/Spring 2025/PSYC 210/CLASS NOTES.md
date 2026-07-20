## **Key concepts**

***Types of statistics***
- Descriptive: describes aspects of people in a sample
- Inferential: deduces information about the population from which a sample was drawn
	- **Statistical significance** comes into play in inferential stats

***Sample vs population:***
- Population: an entire group of individuals (every American, every woman, etc)
	- Parameters describe populations
	- Population distributions are typically normal due to larger size (central limit theorem)
- Sample: a subset of a population with specific characteristics
	- Statistics describe samples

***Key terms***
- Variable: data point that varies
- Measurement: assignment of numbers to variables
- Data: observations of variables coded into categories

***Types of variables***
- Discrete: finite number of values
- Continuous: infinite number of values

***Four types of measurement (NOIR)***
- Nominal: 
	- Type: name-based 
	- Notes: no numerical values, values are not related - essentially categories
	- Central tendency: mode
	- Graphing: pie charts and bar graphs
		- The datapoints are not related, so histograms cannot be used
			- **Histograms imply adjacent data** - equal interval spacing
	- Example: nationality, blood type, sex, hair color
- Ordinal: 
	- Type: order/rank-based
	- Notes: values are related but spacing is not equal
	- Central tendency: mode and range
	- Graphing: bar graphs
	- Example: rankings of TV shows, podium rankings, psychological evaluations
	- "Disagree, somewhat disagree, neutral, somewhat agree..."
- Interval: 
	- Type: distance-based
	- Notes: values are related, spacing is equal, values can be negative
	- Central tendency: median and range **or** mean and standard deviation
	- Graphing: histograms
	- Example: Likert scales, temperature (F), SAT scores, dates
- Ratio: 
	- Type: comparison-based
	- Notes: values are related, spacing is equal, values cannot be negative, true zero exists
	- Central tendency: median and range **or** mean and standard deviation
	- Graphing: histograms
	- Example: incomes, heights, weights, crime rates

***Class intervals*** 
- Grouping of ranges of datapoints
- Good way to simplify complicated data
- Many different ways to create class intervals
- Class intervals are the boxes in histograms

***Frequency
- Frequency distributions differ in many ways:
	- Central tendency (mean, median, mode)
		- Typical, representative, or central score
			- Mean: all data points summed, then divided by # of data points
				- Sum of deviations from the mean will always equal 0
				- Only works with interval or ratio data
			- Median: exact middle point
				- Only works with interval or ratio data
			- Mode: most commonly repeated data point
	- Variability (how much the data differs)
		- Range: difference between highest and lowest values
		- Standard deviation: square root of variance
		- Variance: how much the data points vary from the mean
	- Skewness (how the data are skewed)
		- Direction that the "tail" of the distribution takes - above or below the mean
		- **Positively skewed distributions have more values on the left of the x-axis**
		- **Negatively skewed distributions have more values on the right of the x-axis**
	- Kurtosis (shape of curve)![[Screenshot 2025-01-28 at 6.16.47 PM.png]]![[Pasted image 20250128182254.png]]

***Frequency definitions***
- Frequency: number of responses in a particular category of a variable
- Cumulative frequency: number of responses above or below a particular data point
	- Added up/calculated as you progress through the data
	- Last category is always the entire sample
- Relative frequency: frequency of a particular data point divided by the total number of responses
- Cumulative relative frequency: percentages of data above or below a particular data point
	- Divide the frequency of each interval by the total number of observations

***Variability***
- Measures of variability 
	- Range: maximum score minus minimum score
	- Variance: average squared deviation from the mean
		- $s^2$ = variance
		- Sum of the squared deviations from the mean divided by $n - 1$
	- Standard deviation: square root of the average squared deviation from the mean
		- $s$ = standard deviation
		- Square root of variance
- Lower variability, pointier curves; higher variability, wider curves

***Relative standing
- Relative standing: using single numbers to describe a larger group of numbers
- Descriptive statistics are needed to compare between data
- Percentiles and percentile ranks: describes a particular data point relative to other data points in its distribution (80% of ACT test takers)

***Distributions***
- **Normal distribution**
	- **Mean = 0**
	- **Standard deviation = 1**
	- Total area under the curve = 1
	- Curve is symmetrical
	- Asymptotic
	- Used to estimate the proportion of scores that should fall at or below any given z score
- **Types of statistical distributions:**
	- Population Distribution
		- The entire population
	- Sample Distribution
		- Distribution of scores in a particular sample
	- Sampling Distribution
		- Distribution of sample statistics
- Z formula tells us how far people are deviating from the SD/mean
- Population distribution - actual distribution of scores across the entire population
- Sample distribution - distribution of scores in a particular sample
- Meaning: each mean can be seen as a sample from a distribution of means
- **In a symmetrical distribution, the mean = the median**

***Deviations***
- Standard deviation
	- Indicator of how far data differ from the mean
	- Standard deviation of the sampling distribution of means
		- *SD of the population* divided by *the square root of the sample size*
		- Why the fuck would we want to know this
		- In what world is this meaningful or useful
- Standard error
	- Indicates how far, on average, the data differs from the mean of all the sample means
	- Indicator of how reliable a given mean is
	- A lower SE indicates that a mean is an accurate reflection of the population
	- Standard error of the mean
		- *SD of the population* divided by *the number of samples*
		- How different the population mean is likely to be from a sample mean

***Hypothesis testing***
- Is the sample mean far enough away from the population mean that I can assume the sample came from a different population?
- Types of hypotheses
	- $H_0$ - Null hypothesis 
		- Differences are due to chance
		- There is no real difference
	- $H_1$ - Alternative hypothesis
		- Differences are not due to chance 
		- There are real differences
- Errors:
	- Types of errors:
		- Type I error: rejecting a true null hypothesis
		- Type II error: failing to reject a false null hypothesis
	- Decreasing statistical errors:
		- Type I error: change alpha level
		- Type II error: increase power, improve measurement, and increase sample size
	- Power (1 - beta): the probability of correctly rejecting the null hypothesis
		- Increased by:
			- Reducing error variance (better measures, more homogeneous population)
			- Increasing sample size (standard error of the mean is decreased)
	- Error graph: ![[Screenshot 2025-02-05 at 3.12.22 PM.png]]

***Interpreting data***
- **Effect sizes**
	- Helps us to determine whether the effect of a variable is meaningful
	- P-value indicates significance
	- Cohen’s d measures the standardized size of the difference (that’s what she said)
	- R (correlation and regression):
		- Small: 0.10
		- Medium: 0.30
		- Large: 0.50
	- R² (correlation and regression):
		- Small: 0.01 
		- Medium: 0.09
		- Large: 0.25
	- Cohen’s d (ANOVA, t-test):
		- Small: 0.2
		- Medium: 0.5
		- Large: 0.8
	- Omega² and eta² (one-way and factorial ANOVA):
		- Small: 0.01
		- Medium: 0.06
		- Large: 0.14
- **Significance**
	- A p-value of less than 0.05 indicates statistical significance (t-test)
	- Z score of 1.96 indicates statistical significance (z-test)
- **Confidence intervals**
	- The range that we expect our estimate to fall into should we continue testing
	- Simple explanation: 
		- Range of values that we can expect our population value to be within
		- Most common one is the 95% confidence interval
		- While not exact, you can think of it as a standard deviation for our population value
- **Main effect:** the effect of an independent variable on a dependent variable
- **Interaction effect:** the effect of one independent variable on the dependent variable changing because of another independent variable
- **Spreading effect:** effect of one independent variable at one level of the other independent variable
	- There is either a weak effect or no effect of that independent variable at the other level of the other independent variable
- **Crossover effect:** one independent variable has an effect at both levels of another independent variable, but the effects are in opposite directions

## **Types of tests**

***Z transformation***
- Z scores allow us to compare scores across different distributions (samples vs populations or sampling distributions) and measure standard deviations
- Standard normal distribution is used: z scores equate the means by making them 0 and the standard deviations by making them 1 
- **Used when the population standard deviation is known**
- $(x - m)/s_x$
	- $x$ = your score
	- $m$ = mean
	- $s_x$ = standard deviation
- **Alpha (ɑ):** the cut-off line for determining if your results are significantly different
	- Application: the typical alpha value is ɑ = 0.05 which means that we only allow 5% of margin for error when determining if our results are significantly different
	- _Arbitrary number_ chosen by psychologists - your data doesn’t affect your alpha value since psychologists set it beforehand
	- *Note: Alpha is also the probability of a Type I error
- **Z score of 1.96** is different enough to indicate that the data originates in another group ![[Screenshot 2025-02-07 at 2.59.49 PM.png]]

***One-tailed and Two-tailed Tests***
- One-tailed:
	- A one-tailed test has the entire 5% of the alpha level in one tail (in either the left, or the right tail)
	- Appropriate if you only want to determine if there is a difference between groups in a specific direction
	- The main advantage is that it has more statistical power than a two-tailed test at the same significance (alpha) level
- Two-tailed:
	- A two-tailed test splits your alpha level in half 
	-  Appropriate if you want to determine if there is any difference between the groups you are comparing
	- Uses both the positive and negative tails of the distribution
	- Tests for the possibility of positive or negative differences

***Degrees of freedom***
- Each data point in a sample is free to vary
- Sample of $n = 5$: five degrees of freedom
- Once you calculate something, you lose a degree of freedom

***T-tests***
- **Used when the population standard deviation is unknown**
- **Sample standard deviation is used instead**
- **T = (individual score - mean)/sample standard deviation**
- **A p-value of less than 0.05 indicates statistical significance** 
- Degrees of freedom are $n - 1$
- Types of t-tests:
	- Two-sample/independent t-test: used to find statistical significance between two samples
		- Independent-samples t-test deals with both variance between groups and variance within groups
		- Independent-samples t-test has less statistical power
	- Correlated samples t-test: used when there is no individual difference variance (?)
		- Pre vs Post Test
		- Couples
		- Multiple Interventions
		- Related Samples
- Basics: assume homogeneity of variance/homoscedasticity, independence of observations, and normality

***Regression and Correlation***
- Sir Francis Galton established eugenics - oops
- Linear relationships - graphed with the line of best fit
- Regression equations
	- Y = (predicted) outcome score
	- b = slope
	- X = individual score
	- a = y-intercept
	- e = standard error
![[Screenshot 2025-02-26 at 2.54.06 PM.png]]
![[Screenshot 2025-02-26 at 2.59.06 PM.png]]

***Multiple regression***
- Explains the relationship between multiple independent variables and one dependent variable
- Shows the line of best fit to describe the relationship between variables but does not tell us the relative strength of the relationship
- Value add of multiple regression
	- Effect of each variable while controlling for the impact of the other predictors
	- Contrast with bivariate correlations
- Simple explanation: 
	- Multiple regression predicts how one variable will react given that we know the changes in the other variables
	- Doesn't tell us the strength of the relationship, just allows us to know that it is there

***Correlation***
- Statistical measure that expresses the extent to which two variables are linearly related
- Explains the strength of a relationship
- Falls from -1 to 1
- Limitations:
	- Can be affected by the range of the X and Y variables
	- Extreme scores can inflate correlations

***Basics of correlation and regression***
- Interval or ratio scales
- Linear relationship
- Normal distributions for X and Y
- Homoscedasticity
- Combining groups can sometimes be misleading
- Some relationships are non-linear (?)
- Correlation DOES NOT imply causation

***ANOVA***
- Analysis of variance
- Factors: independent variables
- Levels/groups: different conditions within the independent variables
- Types of ANOVA:
	- One-way ANOVA: 
		- Used to calculate the differences between the means of several independent groups (usually three, can be two)
		- Can only be used for one independent factor
	- Two-way ANOVA:
		- Factorial but with only two independent variables
		- Smallest number of IVs that you can have and still use factorial
	- Factorial ANOVA: 
		- Used when there is more than one independent factor
		- Groups are split on the independent variables
		- Testing for the effects on the groups and the interaction between the IVs
		- Assumptions: ratio or interval DV, categorical IV, normality, homoscedasticity, independence of observations, independence of groups
- Null hypothesis of ANOVA: all means are the same/came from the same distribution
- Alternative hypothesis of ANOVA: at least one of the means came from a different distribution

***F-statistic:***
- Tells us how important group differences are relative to how groups differ within themselves
- Large omnibus difference is ideal
- Numerator of F-ratio measures the size of the sample mean differences - obtained by computing the variance for the sample means
- When the null hypothesis is true for an ANOVA, F-ratio will be 1.00
- **F-distribution:**
	- Can never be negative
	- If the F statistic is past the critical point (which varies based on degrees of freedom), you reject the null hypothesis that all samples are from the same population

***Tests performed after rejecting the null hypothesis:***
- **Post-hoc:** inflates family-wise type I error, but allows you to see all differences
- **Planned contrasts:** pinpoints a specific difference