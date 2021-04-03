
## Maturity stages in analytics
### Descriptive analysis
* What happened?
* Main Goal: explain variances and look for trends
    * Variance = year x / (year x - 1) + 1 
* Analytics techniques: Historical analysis, variance analysis, trend analysis

### Diagnostic analysis
* Why did it happen?
* SWOT (strength, weakness, opportunities, threats) analysis 
* Analytics techniques: Comparative analysis, value-based analysis, correlation analysis

### Predictive analysis
* What will happen?
* Analytics techniques: Time series analysis, regression analasis, decision tree analysis

### Prescriptive analysis
* How can we make it happen?
* Recommends a course of action based on expectation of what might happen in the future
* Analytics techniques: Machine learning (trial and error), AI/ natural language processing

## Analytics techniques in practice
### Trend analysis
* Excel function: DATE(), EOMONTH(), SUMIF()
* Excel graph: line graph with time

### Comparison analysis
* Comparing the performance of two units (internal teams / external benchmarking)
* Example: Profitability of team A and team B in company 

### Value based analysis
* OUtlines the most valuable activities of a firm
* Sensitivity analysis. Eg: How would revenues change if we adjust price? Note that when price changes, volume is affected

### Correlation analysis
* -1 <= Correlation value < 1
* Excel function: correl(array1, array2)

### Time series analysis
* Steps on the idea that the future realisation of a variable can be predicted by studying the past behaviour of the variable itself
* Time series modelling methods: Naive, Deterministic (with +/- tolerance), Probabilistic (Monte-Carlo), Hybrid (Deterministic + Probabilistic)
* Simple techniques: Naive, auto-regressive modelling with one lag, moving averages
* Advanced techniques: ARMA, ARIMA
* Excel Data Analysis ToolPak: Regression
   * Compare one column of current value to another column of historical value, using simple linear regression model. In this case, the current value is Y and the historical value is X. 
  * To capture annual seasonality patterns, first and second columns must be 12 months apart

### Regression analysis
* Used to quantify causal relationships among different variables
* When you have more than one X variable, it is called "mutiple regression"
* Linear regression, logistic regression
* Excel Data Analysis ToolPak: Regression.
* Y = aX1 + bX2 + ... + c
* * Two important parameters to determine fit of model:
   1. r^2 least squares estimate: It tells you how many points fall on the regression line, ie what percentage of the variation of y-values around the mean are explained by the x-values.
   2. p-value: probability that the coefficient is wrong. If p is small, this means that the linear model is statistically significant
