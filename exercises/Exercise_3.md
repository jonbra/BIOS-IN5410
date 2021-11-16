Make sure that the packages `tidyverse` and `dslabs` are installed and activated.

A) Use the `select()` function to show only certain columns of the file `data_file_1.csv` that you imported in Exercise 2. 
- Select only the "Gene" column.
- Select the "Gene" and the "length" columns
- Find two ways of selecting the "length" column with the select() function.
- Can you use select() to reverse the order of columns?
- Can you use select() to drop columns instead of selecting them?

B) Use the `filter()` function to select the same data frame by rows.
- Show only the row containing information about Gene A.
- Which genes are longer than 200? Use filter() to show this. 
- How can you use filter() to show all genes _except_ gene A? (Hint: != is used in R to symbolize "not equal to).

C) Use `%>%` to combine the output of `select()` and `filter()` to show only the "Gene" and "count" columns and only genes with count >= 50.

D) Group_by
