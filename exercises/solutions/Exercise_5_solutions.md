These are just suggestions, there are probably many ways to do this

A)
```{r}
for (i in 1:7) {
  print(i^2)
}
```

B)
```{r}
df <- read_csv("data_file_1.csv")
for (n in 1:ncol(df)) {
  print(paste0(names(df[n]), " (", nchar(names(df[n])), ")"))
}
```

To put the result into a vector instead:
```{r}
# Create an empty vector 
my_vector <- vector("character", ncol(df))
for (n in i:ncol(df)) {
  my_vector[n] <- paste0(names(df[n]), " (", nchar(names(df[n])), ")")
}
my_vector
```
