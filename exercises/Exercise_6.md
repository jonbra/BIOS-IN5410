Create a piece of code that loops through the data in the file "data_file_1.csv" and for each gene prints the gene name and whether it is longer or shorter than 200. You can either create the code from scratch, or you can use the code below as a starting point:

```{r}
for (i in 1:nrow(...)){
  if(df$length[] > 200){
    print(paste0("...", df$Gene, " is longer than 200"))
  } else{
    ...
    }
}
```
