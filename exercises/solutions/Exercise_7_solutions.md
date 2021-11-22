```{r}
# Usage: Rscript my_fourth_Rscript.R inputfilename.pdf data_file_1.csv
library(tidyverse)
args <- commandArgs(trailingOnly=TRUE) # Capture whatever you write on the command line after the script name

input_file <- args[2]
# Glue together the file path to the data folder with the name of the outputfile
df <- read_csv(paste0("~/BIOS-IN5410_H2021/data/", input_file))

# Create an object that stores the file name
name <- args[1]
# Plot gene length vs. count
pdf(file = name)
plot(df$length, df$count)
dev.off()
```
