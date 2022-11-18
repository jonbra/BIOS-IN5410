A) Use the `select()` function to show only certain columns of the file `data_file_1.csv` that you imported in Exercise 2. 
- Select only the "Gene" column.
```
select(df1, Gene)
```

- Select the "Gene" and the "length" columns
```
select(df1, Gene, length)
```

- Find two ways of selecting the "length" column with the select() function.
```
select(df1, 3)

select(df1, starts_with("l"))
```

- Can you use select() to reverse the order of columns?
```
select(df1, length, count, Gene)

rev(df1 %>% select(everything())
```
- Can you use select() to drop columns instead of selecting them?
```
select(df1, -length)
```

B) Use the `filter()` function to select the same data frame by rows.
- Show only the row containing information about Gene A.
```
filter(df1, Gene == "A") # Notice the double equal sign
```
- Which genes are longer than 200? Use filter() to show this.
```
filter(df1, length > 200) # This works because the length column contains numbers (double)
```
- How can you use filter() to show all genes _except_ gene A? (Hint: != is used in R to symbolize "not equal to").
```
filter(df1, Gene != "A") # != is common in computer languange to specify not equal to
```

C) The "pipe" 
- Use `%>%` to combine the output of `select()` and `filter()` to show *only* the "Gene" and "count" columns and *only* genes with count >= 50.
```
df1 %>%
  select(Gene, count) %>%
  filter(count >= 50)
```

D) `mutate()` and `group_by()`
- Create a new column called "long_genes" using `mutate()`. The column should state whether each gene is either longer than 200 or shorter/equal to 200 (hint: you can use "> 200" in the mutate() function. This will give TRUE/FALSE whether a value fulfills the criterium).
```
df1 %>%
  mutate(long_genes = length > 200) 
```
- Group the genes into two groups whether they are longer than 200 or shorter/equal to 200 using `group_by()` (hint: pipe the output of the previous command into `group_by()`).

```
df1 %>%
  mutate(long_genes = length > 200) %>%
  group_by(long_genes)
```
- Calculate the average length of the genes in the two groups using the `summarize()` function (hint: `mean(length)` can be used to calculate the average).
```
df1 %>%
  mutate(long_genes = length > 200) %>%
  group_by(long_genes) %>%
  summarise(average = mean(length))
```
