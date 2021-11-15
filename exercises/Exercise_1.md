Exercises taken from [here](https://rafalab.github.io/dsbook/r-basics.html#exercises)

A) What is the sum of the first 100 positive integers? The formula for the sum of integers 1 through _n_ is _n_(_n_+1)/2. Define _n_ = 100 and then use R to compute the sum of 1 through 100 using the formula. What is the sum?  

B) Now use the same formula to compute the sum of the integers from 1 through 1,000.

C) Look at the result of typing the following code into R:  
```{r}
n <- 1000
x <- seq(1, n)
sum(x)
```  

Based on the result, what do you think the functions `seq` and `sum` do? (You can use `help`.)

a. `sum` creates a list of numbers and `seq` adds them up.  
b. `seq` creates a list of numbers and `sum` adds them up.  
c. `seq` creates a random list and `sum` computes the sum of 1 through 1,000.  
d. `sum` always returns the same number.
