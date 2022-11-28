# 2022_HIA_AP
This folder contains code for computing the health burden of air pollution with example data [^1]. The `.Rmd` file format displays your code, notes, and results simultaneously. 

## How to use this code

#### Go through the code and sample data
- Run the code in `2022_HIA_all.Rmd` by either
  - clicking the blue `Knit` button on top of the document, OR
  - run individual code-chunks by clicking on the green play button within each section

- Examine the format of outcome and exposure data files. Ensure that your exposure and outcome data are in the same format  

#### Replace sample data with your own data
- Replace following files in the `Sample Data` folder with your files with same format and same names 
  - `exposure.csv`
  - `outcome.csv`
  
- Open the `2022_HIA_all.Rmd` file. Click the blue `Knit` button on the top of the document. This will generate a default HTML report with the same name. And, the results will be saved in the `Results` folder. 

## Frequently Asked Questions

- The code is for .csv data file format. All my data is in excel format. Can I still use the code?
  - Yes. You can use the `readxl` package to read excel files. In the `loading files` section, replace lines with `read_csv` with the appropriate function from the `readxl` package. 
 
- Why do we need to join the files? 
  - Typically, the air pollution concentration  data and health outcomes data are from different sources and hence in different files. We need to combine the epxosure and outcome information along with the concentration response function to in a single dataset or table to compute the air polution burden.

- What does `left_join` do?
  - `left_join` combines two data frames `x` and `y` in such a way that all rows from `x` are included in the final dataset. `x` and `y` are joined based on keys. Keys can be any number of variables/columns that are common in both the joining data frames. For example, in the `Joining Data` section, we join exposure data with exposure-response table using the `pm25` column. Before joining ensure, that they "key" columns in joining datasets are formatted the same way i.e. same column names, class, significant digits, etc. 

- The default report is in HTML format. How can i generate a pdf or Word report with this code?
  - Click the dropdown menu next to the Knit button on top of the .Rmd file and click on `Knit to PDF` or `Knit to Word`.


[1]: This code and sample data has been adapted from work done by Ginanjar Syuhada for Indonesia Air Quality Project
 
