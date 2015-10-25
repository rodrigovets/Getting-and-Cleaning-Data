# Getting and Cleaning Data - Course Project
## README

The present file explain how to get and store the data in your computer, and how to use  run_analsis.R script

1. Download and unzip the UCI HAR Dataset folder, with the data, from https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
2. Rename the "UCI HAR Dataset" folder to "UCI_HAR_Dataset"
3. Store the "UCI HAR Dataset" folder in your main directory
4. Create the run_analysis.R script and save in your main directory
5. Both "HCI_HAR_Dataset" folder and the run_analysis.R script should be in the current working directory.
6. Open the "run_analysis.R" script in RStudio
7. At the end of Step-5, two output files will be created in the working directory
- mergeddata.txt (8.3MB) - it contains a data frame called cleanedData with 10299*68 dimension.
- tidydataset.txt (224MB): it contains a data frame called result with 180*68 dimension.
8. Use UCI_HAR_tidy_dataset <- read.table("tidydataset.txt") command in RStudio to read the file.
