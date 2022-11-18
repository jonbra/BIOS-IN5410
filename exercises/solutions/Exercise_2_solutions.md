A) List the files in the *data* folder. How many files are there? Store the list of files as an object named *files* (add the argument `full.names = TRUE`) to the `list.files` function.

```
files <- list.files(full.names = TRUE)
```


B) Import the different csv files using the `read_csv` function and store them as different objects. You can read *data_file_1.csv* by indexing the first element of the list of filenames in *files* like this `read_csv(files[1])` (the [1] tells R to get the first element of the *vector* of file names that are stored in *files*).
```
df1 <- read_csv(files[1]) # The square brackets allows us to access a specific element of the files object. In this case element one (the first filename).
```

- How many columns and rows are in *data_file_1.csv*? (you can print the object, look in the Environment tab in RStudio, or click on the object in the Environment).  

We see that the data file contains three columns and six rows. 
```
df1
# A tibble: 6 x 3
  Gene  count length
  <chr> <dbl>  <dbl>
1 A         4    120
2 B        50    350
3 C        23    200
4 D       250   1230
5 E        15    180
6 F       170   1010
```

- How many columns and rows are in *data_file_2.csv*? (hint: you may need to change one of the default arguments of the `read_csv` function).
```
df2 <- read_csv(files[2], col_names = TRUE) # The file does not contain a header. The first line contains the actual data.
```
- Something looks a bit strange when reading *data_file_3.csv* using the `read_csv` function, what? Try to use the `read_delim` function instead and set the *delim* argument correctly. Are you able to make the file look like *data_file_1.csv*?
```
df3 <- read_delim(files[3], delim = ";") # The file has a semicolon separating the values and not comma. We need to tell this to R.
```
