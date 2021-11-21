## To this on Saga
### Part 1
- Type `module load R/4.1.0-foss-2021a`
- Use your favorite text editor (e.g. Nano or vim) to create a file with the following content:
```{r}
my_files <- list.files()
print(my_files)
```
- Save the file as *my_first_Rscript.R*
- Run the script in R by typing `Rscript my_first_Rscript.R`
- You should see a list of files printed to the screen. Type the `ls` command in the terminal and check that it prints the same files.
- Congratulations! You have just created your first R script!

### Part 2
- Create another file called *my_second_Rscript.R* with the contents:
```{r}
library(tidyverse)
df <- read_csv("~/BIOS-IN5410_H2021/data/data_file_1.csv")
# Plot gene length vs. count
pdf(file = "gene_length_vs_count.pdf")
plot(df$length, df$count)
dev.off()
```
