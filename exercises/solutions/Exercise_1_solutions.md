A) What is the sum of the first 100 positive integers? The formula for the sum of integers 1 through _n_ is _n_(_n_+1)/2. Define _n_ = 100 and then use R to compute the sum of 1 through 100 using the formula. What is the sum?  

```
n <- 100
n*(n+1)/2 # Notice that you need to enter the "*" (multiplication). n() is interpreted by R as a function
```

B) Now use the same formula to compute the sum of the integers from 1 through 1,000.

```
n <- 1000
n*(n+1)/2 
```

C) Look at the result of typing the following code into R:  
```{r}
n <- 1000
x <- seq(1, n)
sum(x)
```  

Based on the result, what do you think the functions `seq` and `sum` do? Which of the alternatives below are correct? (You can use `help`. Try also to print out the values of `x`)

a. `sum` creates a list of numbers and `seq` adds them up.  
b. `seq` creates a list of numbers and `sum` adds them up.  
**b. is correct. `seq` creates a vector (kind of like a list) of the numbers 1, 2, 3, .... 100. Sum just adds all these numbers together**
c. `seq` creates a random list and `sum` computes the sum of 1 through 1,000.  
d. `sum` always returns the same number.
