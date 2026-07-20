## Computational Statistics
**Definition of computational statistics**
- Interface between statistics and computing
- Enabling difficult statistical inferences
- Data science eclipses the role of statistics in quantitative research
- **Methods of programming**
	- Understand the question, plan, and divide larger tasks into smaller tasks


-------------------------------------------------------------------

## Basics of R
**Projects**
- Projects store all R scripts, data, documents, and functions in one place
- Each project has its own directory, workspace, history, and source 
- Projects make code easier to replicate and access

| **Operand** | **Type**                 |
| ----------- | ------------------------ |
| `<-`        | Assignment               |
| ==          | Equal to                 |
| !=          | Not equal to             |
| <           | Less than                |
| >           | Greater than             |
| <=          | Less than or equal to    |
| >=          | Greater than or equal to |

| **Operand** | **Output**   | **Results**                                                                                                     |
| ----------- | ------------ | --------------------------------------------------------------------------------------------------------------- |
| !           | NOT          | `! TRUE == FALSE`  <br>`! FALSE == TRUE`<br>                                                                    |
| &           | AND (vector) | `TRUE & TRUE == TRUE`  <br>`TRUE & FALSE == FALSE`  <br>`FALSE & TRUE == FALSE`  <br>`FALSE & FALSE == FALSE`   |
| &&          | AND          | `TRUE & TRUE == TRUE`  <br>`TRUE & FALSE == FALSE`  <br>`FALSE & TRUE == FALSE`  <br>`FALSE & FALSE == FALSE`   |
| \|          | OR (vector)  | `TRUE \| TRUE == TRUE`  <br>`TRUE \| FALSE == TRUE`  <br>`FALSE \| TRUE == TRUE`  <br>`FALSE \| FALSE == FALSE` |
| \|\|        | OR           | `TRUE \| TRUE == TRUE`  <br>`TRUE \| FALSE == TRUE`  <br>`FALSE \| TRUE == TRUE`  <br>`FALSE \| FALSE == FALSE` |

**Vectors**
- Simplest data structure
	- A vector corresponds to a single row or column in a table
- Homogenous sets of data
- `class()` function identifies a given object

**Vectorized operations**
- Vectorized operations speed up coding in R

**Other data structures**
- Matrices: two dimensional, homogeneous
- Arrays: n dimensional, homogeneous
- Factors: nominal/categorical data
- Data frames: two dimensional, heterogeneous
- Lists: collection of objects, heterogeneous

**Conventions**
- For objects, use noun names
- For functions, use verb names
- Indices start at 1
- Function definitions are found with ?func
- True is TRUE and false is FALSE


-------------------------------------------------------------------

## Data Visualization
**Benefits of data visualization**
- Seeing trends and spreads in the data
- Making data more accessible and engaging

**Guidelines**
- Use equal intervals within an appropriate range
	- **Do not truncate** either axis
- Label both axes with units
- Label the title of the graph
- Use appropriate symbols for data points
- Add error bars and significance if possible
- Ensure perspective is not misleading
- Know the purpose of visualization
	- Comparison, composition, distribution, or relationship?

**Four basic plots in R**
- **Histogram**
	- Usage: distributions
- **Box or violin plot** 
	- Usage: distributions and comparisons
- **Scatter plot**
	- Usage: relationships
- **Heat map**
	- Usage: relationships

**Using ggplot**
- **Layers:** adding graphs to the axes
- **Scales:** transforming data to fit the graph
- **Coordinates:** controlling the perspective of the graph (grid etc)
- **Faceting:** splitting the data
- **Themes:** controlling the design of the graph


-------------------------------------------------------------------

## Documentation
**Rationale**
- Documentation aids reproducibility 
	- Lack of documentation can lead to errors and false conclusions
		- Figures can misrepresent the original text
		- Authors can use the wrong data files 
		- Sequence of code can be unclear
- Data, analyses, and results need to be interlinked and clearly denoted
	- Mark which data and which processes were used
	- Names should be clear and informative 
	- Data should be publicly available for reproduction testing
- Documentation is for other people, not for computers
	- With good documentation, other coders can understand your processes

**Rmarkdown**
- Method of writing reports in R that incorporates plain text and R code
- Can also incorporate shiny apps for interactivity 


-------------------------------------------------------------------

## Basic Statistics
**T-tests**
- Tests if two means are significantly different 
- Means and standard deviations are needed for analysis
- **General form:** ${\mu_{diff}}/{se}$
	- $se$ is standard error (standard deviation of the sampling distribution of the means)
- **Assumptions**
	- DV is continuous & normally distributed 
	- There are no outliers within the DV
	- Observations within a sample are independent
	- Probability: relative frequency of an event’s occurrence when repeating tests
- **Types of t-tests**
	- **One-sample:** testing if a data average is equal to a given value
		- **Null hypothesis** ($H_0$): the average is equal to the given
		- **Equation:** $t = (\bar x - \mu) / se_{\bar x}$
			- $t > 1.96$ and $p < 0.05$ indicate significance 
	- **Two-sample:** testing if two data averages are equal
		- **Null hypothesis** ($H_0$): the averages are equal
		- **Equation:** $t = (\bar x - \bar y) / se_{\bar x - \bar y}$
			- $t > 1.96$ and $p < 0.05$ indicate significance 
		- **Types**
			- **Paired:** data points are related
			- **Independent:** data points are not related

**Correlation**
- Correlation coefficients measure the variation of two variables in standardized terms
- Coefficients are found by dividing the covariance by the product of the standard deviations
- Quantifications:
	- Strength: measuring the intensity of the relationship
		- Coefficients can range from -1 to 1
	- Form: correlation only applies to linearity
	- Direction: testing for positivity or negativity

**Variability**
- Defined in terms of deviations from the mean

**Quiz**
- Know how to interpret t-test results
	- $t > 1.96$ and $p < 0.05$ indicate significance 
	- $df$ indicates magnitude 
- Know when to do independent- vs. paired-sample t-tests
	- Paired: different categories from the same dataset
	- Independent: different categories from different datasets
- Know how to interpret Pearson correlation coefficient
	- 0 = no relation
	- -1 = inverse relation
	- 1 = positive relation
- Visualize data with a correlation coefficient of 0
	- Scattered, ungrouped data with no clear pattern
- Visualize data with a correlation coefficient of 1
	- Data that can be grouped near a straight line of $y = x$


-------------------------------------------------------------------

## Control Structures
**Workflow in R**
- Control structures specify the flow of your code in R
	- **Examples**
		- **If-else:** running based on conditions
			- Structure: if statement, body
		- **For:** running a fixed number of true
		- **While:** running while conditions are true
		- **Repeat:** running infinitely (YIPPEEEE) 
		- **Break:** halting an infinity loop

**Quiz**
- **Structure of quiz**
	- Prompt: we want a function that provides a certain output
	- From a list of 4 functions, choose which one provides the correct output
- **Tips**
	- Review function components and structures
	- Review process of calculating mean


-------------------------------------------------------------------

## Functions
**Writing basic functions**
- Structure:
```
name <- function(<argument list>){
	<code>
	return(<output>)
}
```



-------------------------------------------------------------------

## Simulations
**Data processing with distributions**
- Data can be simulated based on probability distributions
- Simulations allow different statistical methods to be tested on large data sets when new reliable data is not available 
	- Especially relevant in psychology when data is often messy or polarized 
- Numerical simulations are typically created through repeatedly randomly sampling from a given distribution

| **Function** | **Description**              | **Arguments**   |
| ------------ | ---------------------------- | --------------- |
| rnorm        | Random normal distribution   | n, mean, sd<br> |
| runif        | Random uniform distribution  | n, min, max     |
| rbinom       | Random binomial distribution | n, size, prob   |
| rpois        | Random Poisson distribution  | n, lambda       |


-------------------------------------------------------------------

## Models
**Data processing with models**
- A model is a mathematical expression
- Data can be simulated with models by providing the predictor variables 
**Linear regression**
- Equation: $y = B_0 + B_1x$
- Linear regression is stochastic
	- Correlation coefficient $r$ is rarely 1 
	- There is always variance & error
	- Regression line passes through the means of both variables
	- The sum of the residuals always equals 0
	- $B_1$ is directly proportional to $r$ times the slope


-------------------------------------------------------------------

## Bootstrapping
**Methods of bootstrapping**
- Bootstrapping is a method for achieving resampled inferences (statistics from sampling the data)
- **Steps**
	1. Obtain a sample of values
	2. Obtain a test statistic estimate from the data
	3. Randomly select data points with replacement
	4. Obtain a test statistic estimate from the resampled data
	5. Repeat this process “a lot of times, like at least 1,000”


-------------------------------------------------------------------

## Errors
**Type I Errors - False Positives**
- Type I errors occur when the null hypothesis is falsely rejected - i.e., we claim there is an effect when there really isn’t
- In most cases, we have a 5% percent of falsely rejecting the null hypothesis
- Probability of false positives increases as the number of tests increases
**Reducing Errors**
- **Bonferroni Correction**
	- Alpha is divided by number of tests
	- Likelihood of seeing significance is equal to the original alpha
		- Very hard to see significant findings with Bonferroni
- **False Discovery Rate**
	- Controls the expected proportion of false positives among all significant tests
	- Rate that significant features are truly null
	- Less conservative than Bonferroni
	- **Equation:** $FDR = FP/(TP + FP)$


-------------------------------------------------------------------

## Final Project
**[Requirements](https://uncch.instructure.com/courses/94661/assignments/699843)**
- The projects will require that you complete a task that hasn't been done yet in class. All final projects will contain the following elements
	1) At least one function you created that carries out the analyses
	2) Data manipulation, if applicable (some projects may not require this)
	3) Statistical analysis 
	4) Plots
	5) Rmarkdown file (this is your final report)
- A group presentation will be given on November 25th
- Project should explore one or more of the following
	- Bootstrapping
		- Data that benefits from bootstrapping: small samples, unknown population distribution
	- Multiple testing
		- T-tests, multiple correlations
		- Geographical data can be a good source
	- Lying with statistics (with graphs)
		- Find a way to manipulate the data to confirm your hypotheses
		- Represent that in a graph
- Project should show
	- Original results with standard analyses (mean differences, correlation tests) 
	- New results after conducting optimal statistical analyses
- Use r-graph-gallery for plot inspiration