## Intro to Data Science
**Chapter 1**
- Three core aspects of data science: exploration, prediction, inference 
	- Inferences: mathematically sound conclusions based on randomized data
- Two essential tools: computation and randomization
	- Computing provides information, randomness provides perspective

**Chapter 2**
- Causality can be determined from observational studies with treatments and outcomes
- Other variables can interfere and confound the results
- Randomization such as in a randomized controlled experiment can prevent confounding


-------------------------------------------------------------------

## Basics of Python: Plotting Huck Finn
**Viewing book chapters from Gutenberg:**
```
huck_finn_url = 'https://www.inferentialthinking.com/data/huck_finn.txt'
huck_finn_text = read_url(huck_finn_url)
huck_finn_chapters = huck_finn_text.split('CHAPTER ')[44:]
```

**Displaying book chapters in a table:**
```
Table().with_column('Chapters', huck_finn_chapters)
```

**Counting number of characters:**
```
np.char.count(huck_finn_chapters, 'Huck')
```

**Plotting the occurrences of names:**
```
counts = Table().with_columns([
        'Jim', np.cumsum(np.char.count(huck_finn_chapters, 'Jim')),
        'Tom', np.cumsum(np.char.count(huck_finn_chapters, 'Tom')),
        'Huck', np.cumsum(np.char.count(huck_finn_chapters, 'Huck'))
    ])

# Plot the cumulative counts:
# how many times in Chapter 1, how many times in Chapters 1 and 2, and so on.

cum_counts = counts.with_column('Chapter', np.arange(1, 44, 1))
cum_counts.plot(column_for_xticks=3)
plots.title('Cumulative Number of Times Each Name Appears', y=1.08)
```

**Counting number of periods and length of chapters:**
```
chars_periods_huck_finn = Table().with_columns([
        'Huck Finn Chapter Length', [len(s) for s in huck_finn_chapters],
        'Number of Periods', np.char.count(huck_finn_chapters, '.')
    ])
chars_periods_little_women = Table().with_columns([
        'Little Women Chapter Length', [len(s) for s in little_women_chapters],
        'Number of Periods', np.char.count(little_women_chapters, '.')
    ])
```

**Plotting number of chapters:**
```
plots.figure(figsize=(6, 6))
plots.scatter(chars_periods_huck_finn.column(1), 
              chars_periods_huck_finn.column(0), 
              color='darkblue')
plots.xlabel('Number of periods in chapter')
plots.ylabel('Number of characters in chapter');
```

## Basics of Python: Plotting Playlists
**Calculating length of playlist:**
```
songs = Table.read_table('songs.csv')
songs
```

**Calculating average song length in minutes:**
```
np.mean(songs.column('duration'))/60
```

**Finding the expected length of 10 songs:**
```
(10*np.mean(songs.column('duration')))/60
```

**Finding the shortest 10 songs:**
```
np.sort(songs.column('duration'))[:10]/60
```

**Finding the longest 10 songs:**
```
np.sort(songs.column('duration'))[:-10]/60
```

**Finding the sum of the longest 10 songs:**
```
sum(np.sort(songs.column('duration'))[:10])/60
```

**Plotting number of songs by length:**
```
songs.with_column(
	'duration in minutes', songs.column('duration')60
).hist('duration in minutes', bins = 50, normed = False)
```

**Finding 10 random songs in the plot:**
```
np.sum(songs.sample(10).column('duration'))/60
```

**Taking a sample of 10 songs:**
```
durations = make_array()

for i in np.arange(10000):
	durations = np.append(np.sum(songs.sample(10).column('duration'))/60, durations)
```

**Plotting a table of those 10 samples:**
```
Table().with_column('Duration in Minutes', durations).hist(bins = 30, normed = False)
plots.title('Duration of 10 Songs in Minutes')
plot.axvline(x = 60, color = 'red', lw = 2)
avefig('hist.png')
```

**Creating an f-string of something:**
```
print(f”{np.round(np.mean(durations < 60), 4):.2%}”)
```

## Basics of Python: Expressions

| **Operand** | **Type**                 |
| ----------- | ------------------------ |
| +           | Addition                 |
| -           | Subtraction              |
| *           | Multiplication           |
| /           | Division                 |
| %           | Remainder                |
| **          | Exponentiation           |
| =           | Assignment               |
| <           | Less than                |
| >           | Greater than             |
| <=          | Less than or equal to    |
| >=          | Greater than or equal to |
| ==          | Equal                    |
| !=          | Unequal                  |

## Basics of Python: Call Expressions
**Functions are used as follows:**
```
my_function(parameter input)
```

**Other functions can be accessed by importing modules:**
```
import math
```

**Access function descriptions by adding a question mark:**
```
math.log?
```

**Tables can be viewed as columns or rows of data and are called like so:**
```
name_of_table.method(arguments)
```

| Table method   | Syntax                          | Purpose                                     |
| -------------- | ------------------------------- | ------------------------------------------- |
| **Table call** | name_of_table.method(arguments) | Retrieves a given table of arguments        |
| **Show**       | table.show()                    | Displays items within a given table         |
| **Select**     | table.select()                  | Creates a new table with selected columns   |
| **Drop**       | table.drop()                    | Removes selected items from table           |
| **Sort**       | table.sort()                    | Arranges rows in ascending order            |
| **Where**      | table.where()                   | Creates a new table with items of condition |

## Basics of Python: Data Types
**Numbers**
- **int:** integer data type
- **float:** decimal data type
- Note that **int + float** = **float**

**Text**
- **string:** text data type in quotes
- Strings can be concatenated with **+**, resulting in a new string

| String method | Syntax        | Purpose                                        |
| ------------- | ------------- | ---------------------------------------------- |
| **Uppercase** | str.upper()   | Capitalizes the whole string                   |
| **Replace**   | str.replace() | Replaces instances of substrings within string |

## Basics of Python: Sequences
**Arrays**
- Arrays are sequential collections of a given type of data
	- One array can be used to store one type of data
	- Organized sequence of data points (including ints, floats, strings, etc)
- Built-in function `make_array()` transforms other functions into arrays
	- `sum()`, `mean()`, and `len()` are useful to quantify arrays and data
- Matrix arithmetic can be applied to numerical arrays

**Creating arrays in Python:** `name = make_array(1,2,3)
**This results in:** `array([1,2,3])`

**numpy (np)**
- Why do these packages have the most goofy ass names
- **np** includes functions for manipulating arrays
- `np.arange` defines a **range** of data
	- **Range:** array of data listed in sequential order
	- The first argument assigned to `np.arange` is the `end` value
	- `start = 0` and `step = 1` for a range
	- Values in a range go up by the given step, stopping before they reach `end`

| np method      | Syntax               | Purpose                                        |
| -------------- | -------------------- | ---------------------------------------------- |
| **Product**    | np.prod()            | Multiplies all elements                        |
| **Sum**        | np.sum()             | Adds all elements                              |
| **All**        | np.all()             | Tests if all elements are true                 |
| **Any**        | np.any()             | Tests if any elements are true                 |
| **Nonzero**    | np.count_nonzero()   | Counts the number of nonzero elements          |
| **Difference** | np.diff()            | Finds the difference between adjacent elements |
| **Round**      | np.round()           | Rounds each number to nearest integer          |
| **Cproduct**   | np.cumprod()         | Multiplies element with all preceding elements |
| **Csum**       | np.cumsum()          | Adds element to all preceding elements         |
| **Exponent**   | np.exp()             | Exponentiates each element                     |
| **Logarithm**  | np.log()             | Takes the $ln$ of each element                 |
| **Root**       | np.sqrt()            | Takes the square root of each element          |
| **Sort**       | np.sort()            | Sorts elements                                 |

## Basics of Python: Tables
**Tables**
- Sequences of rows and columns that allow you to easily and quickly view data
- To create tables, import all of the `datascience` package and type `Table()`

| Table method           | Syntax                        | Purpose                               |
| ---------------------- | ----------------------------- | ------------------------------------- |
| **Add new columns**    | Table().with_columns          | Adds a new column to a table          |
| **Import data**        | Table.read_table()            | Imports a dataset as a table          |
| **Number of columns**  | Table.num_columns             | Calculates the length of a table      |
| **Number of rows**     | Table.num_rows                | Calculates the width of a table       |
| **Column labels**      | Table.labels                  | Lists the labels of each column       |
| **Relabeling columns** | Table.relabeled(“old”, “new”) | Changes the names of labels           |
| **Viewing data**       | Table.show()                  | Shows specified rows                  |
| **Accessing data**     | Table.column()                | Lists selected columns                |
| **Sorting data**       | Table.sort()                  | Sorts rows in ascending order         |
| **Searching data**     | Table.where()                 | Searches for compatible data          |
| **Formatting**         | Table.set_format()            | Specifies formatting for columns      |
| **Create new table**   | Table.select()                | Creates a new table with said columns |
| **Create new table**   | Table.take()                  | Creates a new table with said rows    |
| **Dropping data**      | Table.drop()                  | Deletes selected columns              |

**We can create new tables based on rows:**
`Table.sort('LABEL', descending=True).take(np.arange(5))`

## Basics of Python: Visualization

| Plotting method   | Syntax             | Purpose                                |
| ----------------- | ------------------ | -------------------------------------- |
| **Scatter plot**  | data.scatter(x, y) | Creates a scatter plot with axes       |
| **Line plot**     | data.plot(x, y)    | Creates a line plot with axes          |
| **Bar chart (H)** | data.barh(x, y)    | Creates a bar chart with axes          |
| **Bar chart (V)** | data.barv(x, y)    | Creates a vertical bar chart with axes |
| **Histogram**     | data.hist(x, y)    | Creates a histogram with axes          |

**Plotting histograms allows us to view the data in a normal distribution** 
- The area under the curve of a histogram represents **percentages**


-------------------------------------------------------------------

## Basics of Probability
**Terminology**
- **Lowest value:** chance of an event that is impossible
- **Highest value:** chance of an event that is certain
- **Complement:** chance of an event not happening
	- 100% - chance = complement
- **Chances of event A** = (number of outcomes where A occurs) / (total number of outcomes)
- **Chances of event A and B** = P(A) • P(B given A)
- **Chances of event A if A can happen 2 ways** = P(A first way) + P(A second way)

**Probability distribution**
- Random event with various possible outcomes

**Empirical distribution**
- Event with possible outcomes based on previous data

**Law of large numbers**
- If a chance experiment is repeated many times, the probability that an event occurs gets closer to the theoretical probability of the event occurring 


-------------------------------------------------------------------

## Basics of Statistics
**Population:** 
- Large original group
**Parameter:** 
- Number associated with population
**Sample:** 
- Selected subset of the population
- **Random sampling:** selection probability of every data point is known 
- **Deterministic sampling:** taking a sample without probability 
**Statistic:**
- Number calculated from the sample 
**Statistical inference:** 
- Conclusions made based on data in random samples
**Testing hypotheses:** 
- Statistical analysis that selects the most accurate hypothesis 
- **Null hypothesis:** no difference is seen 
	- **Empirical distribution:** simulation of the test statistic using a histogram displaying the null hypothesis
- **Alternative hypothesis:** difference is seen
- **A/B testing:** testing to see if two averages come from the same distribution 
**Statistical significance:**
- Observed difference between dataset and reference mean
- Typically, statistical significance is marked at $p = 0.05$
**Confidence intervals:** 
- Interval that estimates a parameter (i.e., mean, median)
- Based on random sampling from a population
- 95% confidence level - higher levels mean wider intervals
	- Indicates probability of either 1 or 0


-------------------------------------------------------------------

## Probability Distributions
**Quantifications:**
- **Mean:** average of all data points
- **Median:** middle data point
- **Standard deviation:** distance from the mean
**Central limit theorem:** with a large sample size, the distribution of the sample average will be normal
**Distribution of sample average:** distribution of all possible sample averages
- Found with empirical distribution 
- The mean/center = the population average
- The standard deviation = the standard deviation of the population divided by the root of the sample size
**Normal distribution:**
- The mean = 0 
- The standard deviation = 1
**T-distribution:**
- The center = 0 
- The standard error = 1
- For sample size $n$, there are $n - 1$ degrees of freedom
- Generally “fatter” than the normal distribution
- The larger the sample size, the more the t-distribution looks like the normal distribution
**Correlation:**
- Correlation coefficient r measures strength of linear relationship 
	- $-1 < r < 1$ 
	- Smaller $r$ indicates a weaker relationship, larger $r$ indicates a stronger relationship
	- Negative $r$ indicates an inverse correlation, positive $r$ indicates a proportional correlation