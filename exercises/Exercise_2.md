Make sure you have installed the `tidyverse` package (`install.packages("tidyverse")` and that it\`s loaded `library(tidyverse)`).  

Write down the answers to the different questions, or show a screen shot.   

NB: We're increasing the difficulty here, but don't worry if this is difficult. We will go through everything together. **And don't be afraid to ask your fellow students for help!**  

A) Where on your file system is R currently working? (working directory). Use an R function to show this. 

B) Change the working directory to the `BIOS-IN5410` repo that you downloaded.  

C) List the files in the *data* folder. How many files are there?  

D) Make a list of _only_ the `csv` files and store the list of files as an object named *files* (store full file paths by adding the argument `full.names = TRUE` to the `list.files` function).  

E) Import the different csv files using the `read_csv` function and store them as different objects. You can read *data_file_1.csv* by indexing the first element of the list of filenames in *files* like this `read_csv(files[1])` (the [1] tells R to get the first element of the *vector* of file names that are stored in *files*).
- How many columns and rows are in *data_file_1.csv*? (you can print the object, look in the Environment tab in RStudio, or click on the object in the Environment).  
- How many columns and rows are in *data_file_2.csv*? (hint: you may need to change one of the default arguments of the `read_csv` function).  
- Something looks a bit strange when reading *data_file_3.csv* using the `read_csv` function, what? Try to use the `read_delim` function instead and set the *delim* argument correctly. Are you able to make the file look like *data_file_1.csv*?
