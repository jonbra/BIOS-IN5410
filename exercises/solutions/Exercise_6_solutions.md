This is one possible solution

```{r}
for (i in 1:nrow(df)){
  if(df$length[i] > 200){
    print(paste0("Gene ", df$Gene[i], " is longer than 200"))
  } else{
    print(paste0("Gene ", df$Gene[i], " is shorter than 200"))
    }
}
```
