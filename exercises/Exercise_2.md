A) List the files in the *data* folder. How many files are there? Store the list of files as an object named *files* (add the argument `full.names = TRUE`) to the `list.files` function.

B) Import the different csv files using the `read_csv` function. Read *data_file_1.csv* by indexing the first element of the list of filenames in *files* like this `read_csv(files[1])` (the [1] tells R to get the first element of the *vector* of file names that are stored in *files*).
- lese inn filer (legge to filer i en data/ mappe. En med og en uten header. csv-filer). Be de forsøke å lese dem inn korrekt. 

Exercise 3:
B)
- velge kolonner, med navn, ranges, bytte rekkefølger, etc.
- filtrere rader med ulike kriterier (må gi dem litt hjelp).

C)
- Forsøke seg på group_by()
