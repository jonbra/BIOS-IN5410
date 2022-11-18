NB!: We not using tidyverse-style code here (e.g. the pipe). We use base R because this plays better with base R plotting. Later when we learn ggplot2 we will use the pipe.

- Make a scatterplot showing the relationship between gene length and count in the data located in "data_file_1.csv". Bonus: Can you change the names of the x and y axes?
```
plot(df1$length, df1$count) # The "$" sign means that we get the values of the column. I.e. length and count columns in this case. 
plot(df1$length, df1$count, xlab = "Gene length", ylab = "Gene count")
```
- Make a histogram showing the distribution of gene counts.
```
hist(df1$count)
```
- Try to add different values for the "breaks = " argument to the hist() function to increase or decrease the number of bins. How does this change the histogram?
```
hist(df1$count, breaks = 3)
``` 
