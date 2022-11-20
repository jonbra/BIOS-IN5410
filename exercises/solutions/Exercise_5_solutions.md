These are just suggestions, there are probably many ways to do this

A)

Write a for loop that iterates over the numbers 1 to 7 and prints the square (square is denoted like this: ^) of each number using print().
```{r}
for (i in 1:7) {
  print(i^2)
}
```

B)
- Make a for loop that iterates over the column names of the dataset in *data_file_1.csv* and prints each name (`names(dataframe)` will show the column names of a dataframe).
```{r}
df <- read_csv("data_file_1.csv")
for (n in 1:ncol(df)) {
  print(names(df[n]))
}
```
- Change the code so that it prints the number of characters in each column name instead (`nchar()` can be useful).
```{r}
df <- read_csv("data_file_1.csv")
for (n in 1:ncol(df)) {
  print(nchar(names(df[n]))
}
```
- Can you combine the codes to print both the column names with the number of characters in parenthesis after each name? (`paste0()` is useful for joining strings together).
```{r}
df <- read_csv("data_file_1.csv")
for (n in 1:ncol(df)) {
  print(paste0(names(df[n]), " (", nchar(names(df[n])), ")"))
}
```

- Finally, save the results of the for loop into a vector instead of printing to screen.
```{r}
# Create an empty vector 
my_vector <- vector("character", ncol(df))
for (n in i:ncol(df)) {
  my_vector[n] <- paste0(names(df[n]), " (", nchar(names(df[n])), ")")
}
my_vector
```
