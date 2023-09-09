# Understanding Statistical Techniques Using R Programming

## Introduction

This project report demonstrates the appropriate use of statistical techniques to analyze data and extract meaningful insights. In this summary, two datasets (from Kaggle), "Exams_data" and "Cars Data," are evaluated using a selected number of applicable statistical methods. The tests performed include checks for normality, hypothesis testing, correlation analysis, and simple linear regression.

### Exploring the Exams_Data Dataset

The "Exams_data" dataset captures the examination performance of students in various subjects. It contains 8 different columns:

- "gender"
- "race.ethnicity"
- "parental.level.of.education"
- "lunch"
- "test.preparation.course"
- "math.score"
- "reading.score"
- "writing.score"

Each column has 1,000 rows with no null values. The dataset was sourced from Kaggle (Chauhan, 2022).

#### Checking the Distribution and Testing for Normality on the "math.score" Variable

To determine the appropriate statistical tests to apply to the dataset, we need to check the distribution of the "math.score" variable. This is done using both graphical and theoretical tests for normality, including QQ plots, skewness plots, and the Shapiro-Wilk's test for normality.

**Research Question:** Are the test scores normally distributed?

- **H0:** The math score is normally distributed.
- **H1:** The math score is not normally distributed.

**Inference:** The QQ plot for the test score has points that mostly fall on the line, characteristic of normal distributions. However, a skewness of (-0.15) was observed, indicating slight left skew. The p-value of 0.002512, which is less than 0.05, provides sufficient evidence to reject the null hypothesis that the math score is normally distributed.

#### Conclusion on Test for Normality

The "math.score" variable does not follow a normal distribution; hence, non-parametric tests would be used for further hypothesis testing.

### Hypothesis Testing

#### Mann-Whitney U Test

To compare the math scores of males and females who took the exam, we use the Mann-Whitney U test, a non-parametric alternative to the independent t-test. The test is conducted at a 95% confidence interval.

**Research Question:** Is the math test score for males and females similar?

- **H0:** The average math score of the two groups is equal.
- **H1:** The average math score of the two groups is not equal.

**Inference:** With a p-value of 0.000000005.25 (less than 0.05), there is enough evidence to reject the null hypothesis, indicating that the average scores of males and females in math are not similar.

#### Pearson's Chi-Squared Test

**Research Question:** Is there any correlation between parental level of education and student lunch type?

- **H0:** There is no relationship between the parent's education level and the type of lunch the child gets.
- **H1:** There is a relationship between the parent's education level and the type of lunch the child gets.

**Inference:** A p-value of 0.46 (greater than 0.05) means we fail to reject the null hypothesis, indicating no significant correlation between the parent's level of education and the student's lunch type.

### Exploring the Cars Data Dataset

The "Cars Data" dataset contains information about three different brands of cars: Europe, US, and Japan. It contains eight different columns:

- "mpg"
- "cylinders"
- "weightlbs"
- "hp"
- "time.to.60"
- "year"
- "cubicinches"
- "brand"

Each column has 256 rows with no null values. The source is Kaggle (Abineshkumar, 2022).

#### Checking the Distribution and Testing for Normality on the "mpg" Variable

**Research Question:** Is the "mpg" variable normally distributed?

- **H0:** The "mpg" is normally distributed.
- **H1:** The "mpg" is not normally distributed.

**Inference:** The histogram is skewed to the left, and the QQ plot indicates non-normal distribution. The observed p-value is less than 0.05, providing sufficient evidence to reject the null hypothesis that the "mpg" variable is normally distributed.

#### Kruskal-Wallis Test (ANOVA)

To investigate the average miles per gallon across the three brands, an analysis of variance test (Kruskal-Wallis) is conducted on the dataset.

**Research Question:** Is fuel economy (mpg) similar across the three brands of cars?

- **H0:** The three brands of cars have similar mpg.
- **H1:** At least one of the brands has a different mpg.

**Inference:** The p-value is less than the significance level of 0.05, indicating no similarity in the fuel economy (mpg) of the cars across the three brands. The null hypothesis is rejected.

#### Test for Correlation

A check for correlation between "mpg" and other variables (Cylinders, cubicinches, hp, weightlbs, year) was conducted using graphical multivariate methods.

**Inference:** There is a strong negative correlation between "mpg" and cylinders, cubicinches, and hp, with weightlbs having the highest correlation. This suggests that as the number of cylinders, horsepower, weight, and engine size increases, fuel efficiency decreases. However, there is a lesser positive correlation between "mpg" and year, indicating that more fuel-efficient cars have been manufactured over the years.

#### Linear Modeling (Simple Linear Regression)

Weightlbs has the highest negative correlation with "mpg." A linear model is constructed for the two variables.

**Inference:** The linear regression equation is mpg = 46.00 + (-0.0075) * weightlbs. The correlation coefficient (R-squared) is 0.68, indicating a good fit of the model. The low RSE (standard deviation of residual errors) of 4.45 suggests that the model predictions are close to the observed values.

## Conclusion

In conclusion, using two separate datasets, a variety of statistical techniques were successfully demonstrated. Detailed tests were performed using proven theories, hypothesis, and existing statistical assumptions, on selected continuous and categorical variables. Analysis of the datasets was then done with necessary illustrations and summary outputs. Inferences were then drawn from the assessment of the test results to produce meaningful insight on the datasets. However, some the observed results were expected, while the others were surprising.

