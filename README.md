# College Debt Analysis

## Is there a relationship between salary and debt?

With the increasing cost of attending college, wondering if taking on potential debt to get a degree has become a question that many ask before committing to higher education. It's known that a large number of people who enroll in college may have to take out loans to cover the cost of their education, there are also assumptions that the more expensive the school's fees are (meaning more debt acquired) could lead to a higher salary, but according to this analysis that is not the case.

To answer this question, I will be working with the *College Scorecard* dataset started by The Obama Administration in September 2015. Each row in this dataset contains information about a college in the USA. 




## The Verdict

The original question was: is there a relationship between debt and salary. After the analysis it can be said that there is a weak relationship between these two variables.

The R-squared of 0.17 means that 17% of the variation in salary can be explained by a linear model on debt. Said another way, a large amount of debt taken on does NOT correlate with a higher salary after graduation:

``
college_model <- lm(MD_EARN_WNE_P10 ~ GRAD_DEBT_MDN, data = college_reduced)
``

<img width="550" alt="Screen Shot 2021-10-27 at 2 55 23 PM" src="https://user-images.githubusercontent.com/84459190/139129093-b6815858-ed53-4bb5-aa98-7e837b0fd33b.png">

``
glance(college_model)
``

<img width="771" alt="Screen Shot 2021-10-28 at 3 46 31 PM" src="https://user-images.githubusercontent.com/84459190/139325009-5edc33a7-c815-45d5-8a73-9376072a56c5.png">


<img width="550" alt="Screen Shot 2021-10-27 at 12 07 21 PM" src="https://user-images.githubusercontent.com/84459190/139104508-d98a3b9c-0303-4484-8e01-a4a9a1b1f200.png">

The wider sections of the violin plot represent a higher probability that members of the population will take on the given value and illustrates that most of the colleges are clustered towards the left of the plot. There are a small number of colleges that have a high amount of median earnings that pull the tail of the plot farther to the right.


