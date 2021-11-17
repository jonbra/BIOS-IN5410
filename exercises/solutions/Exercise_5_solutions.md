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
for (n in names(df)) {
  print(paste0(n, " (", nchar(n), ")"))
}
## [1] "Sepal.Length (12)"
## [1] "Sepal.Width (11)"
## [1] "Petal.Length (12)"
## [1] "Petal.Width (11)"
## [1] "Species (7)"
```
