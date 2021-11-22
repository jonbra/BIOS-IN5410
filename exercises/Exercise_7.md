## Do this on Saga
### Part 1
- Type `module load R/4.1.0-foss-2021a`
- Use your favorite text editor (e.g. Nano or vim) to create a file with the following content:
```{r}
my_files <- list.files()
print(my_files)
```
- Save the file as *my_first_Rscript.R*
- Run the script in R by typing `Rscript my_first_Rscript.R`  
 
You should see a list of files printed to the screen. Type the `ls` command in the terminal and check that it prints the same files.
Congratulations! You have just created your first R script!

### Part 2
- Create another file called *my_second_Rscript.R* with the contents:
```{r}
library(tidyverse)
setwd("~/")
df <- read_csv("~/BIOS-IN5410_H2021/data/data_file_1.csv")
# Plot gene length vs. count
pdf(file = "gene_length_vs_count.pdf") # This tells R that you want to make a pdf file, and what to call it
plot(df$length, df$count) # Make the plot
dev.off() # And save the plot
```
Run the script with `Rscript my_second_Rscript.R`. You should see the output of the messages when loading tidyverse, the output or reading the csv files as well as somehting like "null device 1" (this is from the pdf-plotting). In addition there should now be a new pdf file on Saga. Download it to your local computer and open it.

### Part 3
If you for example want to repeat the commands in *my_second_Rscript.R* on a different data file, or save the pdf with a different file name you have to open and change the script every time. But it's also possible to pass "arguments" when running the R script that allows you to create a more flexible script that can do different operations every time.
- Copy *my_second_Rscript.R* to a new file called *my_third_Rscript.R* using the Unix `cp` command.
- Change the contents to this:
```{r}
library(tidyverse)
args = commandArgs(trailingOnly=TRUE)
df <- read_csv("~/BIOS-IN5410_H2021/data/data_file_1.csv")
# Create an object that stores the file name
name <- args[1]
# Plot gene length vs. count
pdf(file = name)
plot(df$length, df$count)
dev.off()
```
If you run the script like this: `Rscript my_third_Rscript.R new_name.pdf`, `args[1]` takes whatever is written after the script name (i.e. the first argument) and passes it as a text string into the object `name`. 

### Part 4
Can you modify the script so that it takes a second argument that tells R which data file to read and store in `df`?
