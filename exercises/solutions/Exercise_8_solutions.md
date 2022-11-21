Basic plotting
- Make a scatterplot showing the relationship between gene length and count in the data located in "data_file_1.csv". Bonus: Can you change the names of the x and y axes?
```{r}
df1 %>% 
  ggplot(aes(length, count)) + 
  geom_point()
```
- Make a histogram showing the distribution of gene counts.
```{r}
df1 %>% 
  ggplot(aes(count)) + 
  geom_histogram()
  
df1 %>% 
  ggplot(aes(count)) + 
  geom_histogram(bins = 2)
```



