## Data 
**Big data in psychology
- Big data has been present in the field since the 1800s
	- Analyzing large amounts of data presents a problem for statisticians
	- Statistical measures of data gave rise to the idea of average
- Big data is now involved in almost every psychological field
	- Psychology provides an unusual angle to big data
		- Heterogeneity: spread of differences across data sample
- **Four key themes of big data 
	- **Information**
		- Digitization: process of converting continuous analog information into discrete digital information 
		- Dataification: process of quantifying information
			- Structured data: traditional textual and numeric information
			- Unstructured data: nontraditional information
	- **Methods**
		- Analysis requiring additional processing
		- Methods protect against illusory correlations and conclusions
		- Machine learning methods: supervised and unsupervised learning
			- Machine learning aims to generalize old data into new data
- **Human Screenome Project**
	- Researchers recorded changes in participants’ screens every 5 seconds for a year


-------------------------------------------------------------------

## Overview of Machine Learning
**Basics of Machine Learning**
- Method of data analysis that automates analytical model building
	- Specifically, a branch of AI based on the idea that systems can learn from data, identify patterns, and make decisions without human intervention 
- **Framework: learning from experiences to perform tasks**
	- Learning can be difficult to assess - how do computers learn?
	- Training experience for computers and agents is critical to the learning process
		- In psychology, this could include a dataset of physiological and psychological variables
		- We use these variables to predict future variables
		- This favors accurate prediction over statistical significance 
- **Sparsity:** complex model with many variables, where only a few variables are important
- **Supervised learning**
	- **Examples:** regression (numeric, continuous), classification (categoric, binary or multinomial)
	- “The process of developing a mathematical model that generates an accurate prediction”
	- In supervised learning, a predictive model is used for tasks predicting a given output based on known variables
	- **Terms**
		- Predictor = x, independent variable, attribute, feature
		- Target = dependent variable, response, outcome
- **Unsupervised learning**
	- **Examples:** clustering (creating groups of variables), dimension reduction (reducing # of variables)
	- In unsupervised learning, models analyze existing data and make predictions, but there is no target prediction 
	- Often used to identify groups in a dataset
	- **Issues**
		- More of an exploratory method 
		- Less objective than supervised learning
		- Quality of results is difficult to assess

## Machine Learning & AI
**Artificial intelligence**
- Creating systems that perform tasks that normally require human intelligence
- Goal is for the model to simulate intelligent behavior, not to learn from the data
**Machine learning**
- Branch of AI focused on systems that learn patterns from data
- Goal of ML is to make refined predictions for future data
- Deep learning is a further subset of ML 
**The scope of AI is much more general than the scope of ML**

## Key elements of machine learning
**Algorithms**
- **Elements of algorithms**
	- Input: data the algorithm runs on
	- Output: result produced 
	- Finiteness: algorithm ends in finite number of steps
	- Definiteness: each step is clearly defined
	- Effectiveness: each operation can be fully carried out
- Algorithm is the procedure for learning
- No free lunch: no one algorithm will work best for all data
**Models**
- Models are the products of algorithms
- Different algorithms can produce different models from the same data
- Models are trained artifacts used for predictions
**Classification**
- Assigning categories or labels to each data point
- If the end goal is known, then classification is supervised
**Regression**
- Regression models predict probability values between 0 and 1
**Clustering**
 - Method of unsupervised learning
**Dimensionality reduction**
- Representing high-dimensional data in lower dimensions 
	- Example: 3D objects can be represented as 2D shadows
- Example in psychology: identifying constructs in surveys
- Allows you to pull out particular components without doing expensive computing
**Data splitting**
- Separating a dataset to train an algorithm for prediction
- We split data into two-three sets:
	- **Training set:** data used to develop feature sets and train algorithms
	- **Test set:** data used to estimate model’s performance (generalization error)
	- **Validation set:** data used to tune parameters
- Split between training and testing should be balanced, but training should be favored 
**Parameters**
- **Hyperparameters** are defined before training begins
	- Examples: number of clusters, initialization method, number of iterations, stopping criterion
- **Parameters** are estimated as part of the output model
	- Examples: mean, regression slope, coordinates of cluster centers
	- In training, we fit the model parameters
	- In validation, we compare different hyperparameter choices


-------------------------------------------------------------------

## Bradley, Chapter 2: ML Modeling
**No free lunch (ever)**
- ML models are extremely iterative
- Good training streamlines the iteration process

**Data splitting**
- **Goal:** find algorithm $f(x)$ that predicts future $y$ values based on a set of $x$ features
- We split data into two sets:
	- **Training set:** data used to develop feature sets and train algorithms
	- **Test set:** data used to estimate model’s performance (generalization error)
- More time should be given to training than testing
- **Simple random sampling**
	- Data is sampled with a simple random algorithm
	- Does not control for variables 
- **Stratified sampling**
	- Data is sampled so that training and tests sets have similar $y$ values

**Class imbalances**
- Instances where one class has a small proportions of observations
- Can be mitigated with **down-sampling** or **up-sampling**
	- **Down-sampling:** reducing size of classes to match the least frequent class
	- **Up-sampling:** increasing size of rarer samples by generating new samples

**Resampling methods**
- Testing model accuracy by resampling data
- **K-fold cross validation**
	- Method that randomly divides training data in $k$ sets of equal size
		1. Data is split into $k$ sets
		2. The model is trained on $k-1$ sets
		3. The last fold tests model performance 
		4. Process is repeated $k$ times
	- Greater variability in error measures, but lower bias
- **Bootstrapping** 
	- Method that randomly samples the data with replacement (?????)
	- Seems like a bad idea but tragically works
	- Bootstrap samples are the same size as the original dataset
	- Bootstrap samples includes duplicate values 
		- **Out of bag:** data not contained in a sample
		- Model can be trained on bootstrap samples and then tested on OOB samples
	- Lower variability in error measures, but higher bias

**Bias & variance**
- **Bias:** difference between predicted values and true values
	- Also, the tendency of a model to predict in a certain direction (under- or overestimation)
	- Higher bias correlates with higher consistency in resampling
- **Variance:** variability of model prediction
	- Higher variance comes with the risk of overfitting

**Tuning parameters**
- Parameters that control models and bias-variance trade off
- **Ordinary least squares:** method of finding best fit for a dataset
	- OLS represents the model that minimizes the sum of the squared distance between the data points and the line
- In KFVC, as $k$ increases, predictions are based on a larger subset of the data
- Parameters can be tuned manually or with computing techniques

**Model evaluation**
- **Loss functions:** metrics that compare predicted values with true values


-------------------------------------------------------------------

## Yarkoni & Westfall (2017)
- **Psychological data science lacks the ability to strongly predict future behaviors**
	- Explanation has been favored over prediction
		- Finding the parameters of the data-generating model that led from input to output
		- Self-reporting makes this difficult, leading to doubts about if psychological research is truly causal
	- Now, prediction and explanation are overlapping - both are seen as key elements of psychological research
	- Psychologically biased models can sometimes be better predictors
	- Machine learning could improve predictive psychology
- **Psychological models are poor predictors**
	- Research is evaluated based on statistical fit, not ability to predict
	- Research is increasingly unable to be replicated
	- Models that successfully explain behavior cannot always be used to predict behavior and some models show illusory correlations
- **Overfitting:** incorrectly fitting sample-specific noise (extraneous data) from given a given dataset as if it is signal (true data)
	- Overfit models perform well on the given dataset but not on new datasets since they are too tuned to the sample-specific noise, which may not be present in future datasets
	- The more variables in a dataset and the smaller the sample size, the greater the risk of overfitting
	- **Training errors:** errors that occur when the model is first fitted
	- **Test errors:** errors that occur when fitted model is applied to new datasets from the same population
	- Good results are favored in publishing, leading to a greater prevalence of overfitting
		- Pre-registration of research has been suggested to avoid “following the data”
- **Bias is defined negatively in psychology, but not as much in statistics**
	- The statistics definition of bias states that it is a specific directional error in the model (overshooting or undershooting)
	- Bias and variance can be separated to influence the total error of a model
		- Total prediction error = bias + variance
	- Linear models are more biased but less flexible, reducing variance associated with overfitting
- **Creating a model that minimizes prediction error requires:**
	1. Large enough datasets to support sound statistical models
	2. Ability to accurately estimate prediction error
	3. Ability to control the bias-variance tradeoff 
- **Advent of digital data collection has made larger datasets available to scientists**
	- Big data can reduce overfitting errors simply due to the massive size of datasets
- Recent significance seen in small samples can be attributed to intense overfitting - low bias and high variance - which identifies patterns that do not actually exist in the true function
- **Cross-validation allows researchers to evaluate the performance of their models**
	- Cross-validation involves testing models across different samples
	- Classical/independent replication: training models on one sample and testing on a completely different sample
		- Independent replication has been favored, but presents issues: timescale, cost, etc
	- **Datasets can be split into training and test sets to facilitate cross-validation**
		- Underfitting can be avoided by repeating cross-validation and splitting the datasets twice
		- **In K-fold cross-validation, each split is referred to as a fold**
			- In the first fold, dataset A is used for training and dataset B is used for testing
			- In the second fold, dataset A is used for testing and dataset B is used for training
		- One downside of KFCV is its high computation cost and potential to be biased
		- Overfitting is still possible with cross-validation and scientists should be mindful of best practice
- **Regularization allows researchers to improve overfitting models**
	- Researchers can improve statistical predictions by forcing their models to adhere to prior knowledge
	- In ML, researchers penalize the cost function as the model grows more complex, hoping to produce simpler outputs
- **Lasso regression & regularization penalties**
	- For linear regression that estimates outputs with ordinary least squares, the goal is to minimize the sum of squared deviations between the predicted values and the observed values
	- Lasso regression has the same goal, but also has a penalty term proportional to the sum of the absolute values of the coefficients
		- Both the sum of the squares and the absolute sum must be minimized
	- Outputs of lasso regression are always biased
	- Regularized predictions function better with new data, especially with many predictor variables
		- **Forced bias keeps the data from overfitting sample-specific noise, leading to more relevant and accurate outputs**
- **Future of prediction in psychology**
	- Ability to predict future academic performance is critical in educational fields
	- However as with much psychological research, it is difficult to confirm and replicate these findings - cross-validation could be a key technique
	- Instead of conducting large, expensive, and costly studies, scientists can use machine learning to analyze their findings in relation to other psychological research
	- Larger datasets has made current ML models more accurate 
	- ML can be inaccessible to many researchers and students but this is improving over time
	- Focusing on prediction can help to understand and analyze data
- **Key quotes**
	- “The reason effect sizes … have shrunk is that they were never truly big to begin with, and it’s only now that researchers are routinely collecting enormous datasets that we are finally in a position to appreciate that fact”
	- “Whether a machine or a human is drawing the inference, the fundamental problem remains the same: every pattern that could be observed in a given dataset reflects some (generally unknown) combination of signal and error”
	- “Ultimately, the new machine learning approaches working their way into psychology should be seen as opportunities, not threats … what we will hopefully then be left with are models that can demonstrably do something foundational to the study of psychology: reliably predict human behavior”


-------------------------------------------------------------------

## Data Preprocessing & Engineering
**Target engineering**
- Predictive models can be improved by transforming data to fit a more normal distribution
	- Regression models expect a certain error term - changing the data to align with that expectation will lead to better output
- **Correcting for positively skewed target variables**
	- Normalizing data with a log transformation
	- Normalizing data with a box cox transformation 
		- Yes, that is actually what it is called
		- Box cox transformations are more flexible than log transformations
		- BC transformations find a power model that will make the data as normal as possible

**Missing data**
- **Types of missing data**
	- **Missingness completely at random**
		- Missing values unrelated to the data collection process
		- Typically deleted or imputed (estimated)
	- **Missingness at random**
		- Missingness is often systematically related to other observed variables in the dataset
	- **Missingness not at random**
		- Missing values related to the data collection process or unobserved variables
		- No way of predicting missingness
		- Typically categorized as “None”
- Different ML models read missing data differently
	- Some models are able to comprehend missing data, but most cannot parse it
	- Missing data is best deleted before the training process begins
- Distribution of missing data can be visualized with heat maps to inform data cleaning process
- **Imputation of missing data**
	- **Central tendency imputation** 
		- Replacing missing values with mean or median
	- **K-nearest neighbor imputation**
		- Replacing missing values with equivalent values from similar individuals in the dataset
		- **Imputation based on context**
	- **Decision tree imputation**
		- Decision trees can inform missing values
		- Values gathered across many trees results in a reliable, low-variance predictor
		- Random forest imputation or bagged tree imputation can be used

**Feature filtering**
- **Why perform feature filtering?**
	- Larger datasets require models with more features, which have higher computing costs
	- Training times are positively correlated with the amount of features a model has
- Features with little to no variance are easy to eliminate

**Numeric feature engineering**
- **Skewness**
	- Models will perform more poorly on skewed data
	- BC or Yeo-Johnson transformations work best to normalize data
		- Yeo-Johnson transformations stabilize data and reduce variance, but are more flexible than BC transformations
- **Standardization**
	- Standardizing and centering the data around a zero mean results in better model performance 
		- Standardized variables have a mean of 0, a variance of 1, and all equal units

**Categorical feature engineering**
- **Lumping**
	- Features will contain levels with few observations
	- These observations can be lumped into fewer categories
- **One-hot encoding**
	- Common method that encodes categorical variables as numeric by creating a new binary/boolean column for each category
- **Dummy encoding**
	- Some models require numeric, instead of categorical, variables
	- Categorical variables can be transposed with one-hot encoding into boolean values
- **Label encoding**
	- Pure numeric conversion of the levels of a categorical variable
	- Categorical values are sorted into numerical equivalents
- **Target encoding**
	- Replacing categorical data with the mean or proportion of the target variable
		- What is the target variable??

**Data leakage**
- Information from outside the training set that is used to create the model
- Avoiding data leakage requires feature engineering to be done outside of each resampling
	- Otherwise, data would be leaked from one set to another

**General steps for data processing**
1. Filter out zero or near-zero variance features
2. Perform imputation if required
3. Normalize to resolve skewness
4. Standardize numeric features
5. Perform dimension reduction on numeric features
6. Encode categorical features


-------------------------------------------------------------------

## Linear Regression
**Introduction to regression**
- LR is one of the simplest algorithms for supervised learning
- **Key components of LR**
	- **Pearson’s correlation coefficient:** value used to gauge the strength of a linear relationship
	- **Simple linear regression:** model that assumes a linear statistical relationship between variables
		- LR often revolves around finding conditional means
		- This can be an issue with some data, since not all relationships are inherently linear
		- LR does not assume that errors are correlated and often does not account for errors correctly 
	- **Multiple linear regression:** model that includes multiple predictor variables
	- **Principal component regression:** method that represents larger, more complex variables as smaller, less complex variables 
		- The final simple variables are used as predictors in LR
	- **Ordinary least squares:** LR model that uses least squares to estimate the line of best fit
		- Method does not estimate the error variance, but this can be done using maximum likelihood estimation
		- OLS struggles with collinearity (close relation of multiple predictor variables)
			- It cannot tell which effects are individual 
	- **Partial least squares:** supervised dimension reduction method that highlights new features in the data
- **Inference with LR**
	- **Standard error** (square root of variance) can be used to judge the accuracy of LS estimates


-------------------------------------------------------------------

## Logistic Regression
**Boolean analysis**
- Linear regression cannot be applied to binary/boolean data
- Logistic regression is equivalent to linear for boolean data
	- LOR better represents the probability of boolean events by refitting the function based on binary outputs (0 or 1)
- Multiple LOR can predict binary outputs with multiple predictors
- Residual analysis can be used to judge the efficacy of LOR models
- **Feature interpretation**
	- Absolute value of z-statistic of each coefficient represents variable importance 
- **Sensitivity:** true positives / (true positives + false negatives)
- **Specificity:** true negatives / (true negatives + false positives)


-------------------------------------------------------------------

## Regularized Regression
**Regularization** 
- With large data sets, regularization normalizes data points and decreases variance by constraining the total size of all coefficients 
- **Regularization is applied to OLS** 
	- OLS regression seeks to find the line that minimizes the sum of squared errors between the observed and predicted values
	- However, OLS assumptions do not hold true with larger data sets, compromising the accuracy of models 
- **Feature selection** 
	- Certain techniques are preferred, including hard thresholding feature selection, forward selection, backward elimination, soft thresholding
	- These techniques 
- **Penalty parameters**
	- **Ridge**
		- Constrains coefficients as data sets get larger
		- Does not perform feature selection
	- **Lasso
		- Reduces coefficients to zero as data sets get larger
		- Extracts features with largest signals
	- **Elastic net** combines ridge and lasso penalties
