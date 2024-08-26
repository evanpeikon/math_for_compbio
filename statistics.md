# 📚 Statistics
### Basic Formulas 
- $mean(x) = \frac{Σx_i}{count(x)}$
- $variance(x) = Σ(x_i - mean(x))^2$
- $co-variance = Σ(x_i - mean(x)*(y_i - mean(y))$

### Linear Regression 
- Linear regression is a data analysis technique that uses a single known data point to predict a single unknown, but related, data point. For example, predicting someones relative risk of stroke based on their systolic blood pressure.
- To perform a linear regression we use training data to estimate two coefficients (b1 and b0), which are used to make predictions on new data. The formula to determine the coefficients $b_1$ and $b_0$ is as follows:
  - $b_1 = \frac{Σ(xi - mean(x)) * (yi - mean(y))}{Σ(xi - mean(x))²}$
  - $b_0 = mean(y) - b_1 * mean(x)$
- Finally, when we know the values of the coefficients $b_1$ and $b_0$ we can use the following formula to perform a simple linear regression: $y = b_0 + b_1 * x$

## Probability
### The Addition Rule
- The addition rule determines the probability that one event, another, or both occur. The two events can be non-mutually exclusive (outcomes are related) or mutuatlly exclusive (outcomes are not related).
  - For example, we have a 6-sided die and want the probability of rolling an odd number (event A) or the probability of rolling a number $>2$ (event B). The combined probability of these events is $P(A or B)$. Since events A and B are non-mutually exclusive (i.e., its possible to roll an odd number that is greater than 2) the probability is as follows: $P(A or B) = P(A)+P(B) - P(A and B) = \frac{3}{6} + \frac{4}{6} - \frac{2}{6} = 0.83$
- If events A and B are mutually exclusive the probability that one or the other occurs is $P(A or B) = P(A)+P(B)$
  - For example, the probability of rolling 3 on a 6-sided die (event A) or a coin flip landing on heads (event B) is as follows: $P(A or B) = \frac{1}{6}+\frac{1}{2}=0.67$

### Conditional Probability 
- Whereas the addition rule determines the probability that one or both independent events occur, conditional probability determines the liklihod of two dependent events occuring. For example, say we have 5 marbles (3 red and 2 blue) in a bag. If we pick 2 marbles without replacement the chance of hte second marble being red depends on the color of the first marble. Thus, conditional probability is the chance of one event occuring given that another event already happened.
- We denote the word given with the pipe symbol $|$. For example, the probability that we choose a red marble given the first is blue is $P(Red|Blue)$=\frac{3}{4}=75%$
- However, if we replace the marble after selection the events are independent and therefore we use the addition rule... $P(Red|Blue)=P(Red)=\frac{3}{5}$.

### The Multiplication Rule
- The multiplication rule determines the probability of two independent or dependent events occuring simultaneously,denoted as $P(A and B)$. 
- If the events are dependent, then $P(A and B)=P(A)*P(B|A).
  - For example, we have 5 marbles (3 red and 2 blue) and pick two without replacement. What is the probability of picking a blue marble first and second.
    - $P(A and B)= \frac{2}{5}*\frac{1}{4}=0.1 or 10%$
- If the events are independent, the multiplication rule states $P(A and B)= P(A)*P(B)$.
  - For example, what is the probability of flipping heads twice in a row?
    - $P(A and B)= \frac{1}{2} * \frac{1}{2}= 0.25 or 25%$

### Bayes Theorem
- Bayes theorem describes the probability of events based on prior knowledge of conditoons relating to it.
- Bayes theorem states that conditional probability of an event, $P(A|B)$ is equal to the liklihod of the second event given the first event $P(B|A)$ multiplied by the probability of the first event divided by the probability of the second event, as demonstrated below:
  - $P(A|B)= \frac{P(B|A)*P(A)}{P(B)}$

### Probability Mass Function (PMF)
- PMF is the probability distribution that defines the probability of observing a particular value of a discrete random variable. For example, if we flip a coin 10 times we can use the PMF to express the liklihood of all possible outcomes (ie, how likely is it we get 1 head, 2 heads...10 heads).
- The ```binom.pmf()``` function from ScipyStats can be used to calculate the PMF at any value. This function takes three values as it's input: $x$ (number of interest), $n$ (number of trials), and $p$ (probability of success).
  - For example, lets say we flip a coin 10 times and want the probability of observing 6 heads. We can use the code ```stats.binom.pmf(6,10,0.5)``` to get the result $0.2$.
- We can also use PMF over a range of values for discrete random variables by adding the probability of each value. For example, if we flip a coin 5 times and want the probability of 1-3 heads.
  - For example, if $P(x)$ is the probability of observing $x$ successes, we can calculate $P(1 to 3 heads)$ as $P(x=1)+P(x=2)+P(x=3)=0.15+0.31+0.31=0.78$

### Cumulative Distribution Function (CDF)
- The CDF for discrete random variables gives the probability of observing a specific value or less. Thus, CDF at a given value is equal to the sum of all possibilities lower than it, with the value of 1 for the largest possible number.
- In the last PMF xample we found the probability of observing 1-3 heads in 5 coin flips. This could more easily be calculated with the CDF, as demonstrated below...
  - $CDF(x=3)-CDF(x=0)=0.78$
  - We can also use ```stats.binom.cdf()``` with $x$, $n$, and $p$ as inputs, just as we did for PMF.

### Probability Distribution Function (PDF)
- Just as discrete random variables relate to probability mass functions, continous random variables relate to PDFs, which define the probability distributions of continous random variables and span across all possible values that a given random variable can take on.
- When graphed, PDF is a curve across all possible values for random variables and the area under the curve is 1.
- We can calculate the AUC using the CDF for a given probability distribution. For example, say the mean height is 167cm and the standard deviation is 8cm (and height is normally distributed). Now, if we want the probability that a random person is <158cm we can calcualte that using ```stats.norm.cdf(x, loc, scale)``` where $x$ is the value of interest (158), $loc$ is the mean of the probability distribution (167), and the $scale$ is the standard deviation (8). Thus, ```stats.norm.cdf(158, 167, 8)=0.11$

### Poisson Distribution
- The Poisson distribution is used to describe the nunber of times a certain event occurs in a fixed time or space interval. For example, the PD can describe how many support emals you recieve between 10am-12pm on a given day, then represent it as a PMF or CDF.
  - For example, say you expect 25 support emails in a 2 hour window. In that case, the number of emails is poisson distributed with $λ=25$. You can then calculate the probability of getting 11 emails with ```stats.poisson.pmf(11,25)```.
  - Similarly, you can use ```stats.poisson.cdf()``` to evaluate the probability of observing a speciic number of emails or less. For example, if we want the probability of observing 7 emails or less in a 2 hour window when we expect 25 we can use ```stats.poisson.cdf(7,25)```.
- The spread of the poisson distribution is expressed as variance and is equal to $λ$ (the epected value). Thus, the larger $λ$ is, the larger the number of potential values (ie the larger the spread). In other words, the larger the λ, the greater the range (max-min) of data.
- Other probability distributions (like binomial) also have expected values. For example, if you flip a coin 10x ($n=10$) the probability of heads each time is 0.5 ($P=0.5$) and thus we expect 5 heads. As a result, the equation for the expected value of a binomial distribution is $Expected = E(x)=n*p$. Additionally, the variance (spread) of the binomial distribution is $variance = var(x) = n*p*(1-p)$

### Properties of Expectation and Variance
- The expected value of two independent random variables is the sum of each expected value $E(x and y)=E(x)+E(y)$.
- Increasing the value on a distribution by a constant does not change variance $var(a and x)=var(x)$.

### Central Limit Theorem
- CLT states that the sampling distribution of a mean is normally distributed as long as the population is not skewed or the sample size is large enough.
- Importantly, CLT only applies to sampling distributions of mean and not othr statistics like max/min and variance.
- CLT not only establishes that a sampling distribution will be normally distributed, byt also allows us to describe the normal distribution quantitativley by their mean $µ$ and standard deviation $σ$.
  - For example, take a sample size $n$ from a population with a true mean $µ$ and standard deviation $σ$. As long as $n$ is sufficiently large the sampling distribution of means will be normally distributed and the sample mean $x$ will be roughly equal to the population mean $µ$. Additionally, the sample standard deviation $σ$ will be equal to the population standard deviation divided by the square root of the sample size: $sample dist. std dev = \frac{σ}{\sqrt{n}}$
- The standard deviation of the sampling distribution is also known as the standard error of the estimate of the mean. Often we cannot know the true populations standard deviation, so we can estimate the standard error as follows: $std error = \frac{sample standard dev}{\sqrt{n}}$.
  - As $n$ increases, the standard error decreases and as sample standard deviation increases so does the standard error.
- Because the mean of the sampling distribution of the mean is equal to the mean of the population its called an unbiased estimator. A statistic is an unbiased estimator of a population parameter if the mean of the sampling distribution of the statistic is equal to the value of the statistic of the population. Biased estimators on the other hand, is one where the mean of the sampling distribution is not equal to the mean of the statistic for the population. 
