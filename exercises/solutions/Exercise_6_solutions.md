This is one possible solution

```{r}
for (i in seq_along(df$Gene)){
  if(df$length[i] > 200){
    print(paste0("Gene ", df$Gene[i], " is longer than 200"))
  } else{
    print(paste0("Gene ", df$Gene[i], " is shorter than 200"))
    }
}
```
