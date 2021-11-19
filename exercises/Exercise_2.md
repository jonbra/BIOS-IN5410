Make sure you have installed the `tidyverse` package (`install.packages("tidyverse")` and that it is loaded `library(tidyverse)`).  

Write down the answers to the different questions, or show a screen shot.

A) List the files in the *data* folder. How many files are there? Store the list of files as an object named *files* (add the argument `full.names = TRUE`) to the `list.files` function.

B) Import the different csv files using the `read_csv` function and store them as different objects. You can read *data_file_1.csv* by indexing the first element of the list of filenames in *files* like this `read_csv(files[1])` (the [1] tells R to get the first element of the *vector* of file names that are stored in *files*).
- How many columns and rows are in *data_file_1.csv*? (you can print the object, look in the Environment tab in RStudio, or click on the object in the Environment).  
- How many columns and rows are in *data_file_2.csv*? (hint: you may need to change one of the default arguments of the `read_csv` function).  
- Something looks a bit strange when reading *data_file_3.csv* using the `read_csv` function, what? Try to use the `read_delim` function instead and set the *delim* argument correctly. Are you able to make the file look like *data_file_1.csv*?
