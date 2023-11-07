Make sure that `tidyverse` is activated.  

NB: Remember to check the help menus for the different functions, and search the web.

A) Use the `select()` function to show only certain columns of the file `data_file_1.csv` that you imported in Exercise 2. 
- Select only the "Gene" column.
- Select the "Gene" and the "length" columns
- Find two ways of selecting the "length" column with the select() function.
- Can you use select() to reverse the order of columns?
- Can you use select() to drop columns instead of selecting them?

B) Use the `filter()` function to select the same data frame by rows.
- Show only the row containing information about Gene A (Hint: == means "equal to" in R).
- Which genes are longer than 200? Use filter() to show this. 
- How can you use filter() to show all genes _except_ gene A? (Hint: != is used in R to symbolize "not equal to").

C) The "pipe" 
- Use `%>%` to combine the output of `select()` and `filter()` to show *only* the "Gene" and "count" columns and *only* genes with count >= 50.

D) `mutate()` and `group_by()`
- Create a new column called "long_genes" using `mutate()`. The column should state whether each gene is either longer than 200 or shorter/equal to 200 (hint: you can use "> 200" in the mutate() function. This will give TRUE/FALSE whether a value fulfills the criterium).
- Group the genes into two groups whether they are longer than 200 or shorter/equal to 200 using `group_by()` (hint: pipe the output of the previous command into `group_by()`).
- Calculate the average length of the genes in the two groups using the `summarize()` function (hint: `mean(length)` can be used to calculate the average).
