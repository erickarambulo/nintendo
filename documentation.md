# Google Sheets documentations

This documentation will track changes and activities made to Google Sheets. This practice will not only enhance my documentation skills but also foster good habits for myself and future employers, coworkers, and managers. They will be able to monitor the modifications I've made to Google Sheets or other programming languages.

## Documentation Begins here

### 1. Data Cleaning and Preparation

**Handle missing values:** 32% of the 430 Genre values (rows) were missing. I used Google and Gemini AI to determine the genre for the Games column and fill them up.

**Data type consistency:** In order to keep columns cleaned with one data type individually, I clicked on column A to select all range in column A -> Format -> Plain text because column A, **Game**, is a string. Same goes for all columns except **Sales** and **Release Date** columns. **Sales** column is a number type, and **Release Date** is a date type. I also caught an error on date column for *Super Scope 6 game*; therefore, I fixed it, and input the best estimate for release date which is 2/1/1992. I also select all cells and then click on Data -> Data cleanup -> Trim whitespace AND Remove duplicate to remove whitespaces and duplicates.

**Outlier detection:** There is no outlier for any columns especially **Sales** column.

Here is the [link](https://docs.google.com/spreadsheets/d/1pn3tIEid7--GiC5ISr4tvLBWt_l0clf9GftTPZzfBN0/edit?usp=sharing) to see a clean dataset.

### 2. Exploratory Data Analysis (EDA)

**Basic statistics:** I created a pivot table that contains basic statistics, such as finding total (sum), mean (avg), max, min, median, mode, and standard deviation for **Sales** column. Note that **Sales** column is the only numerical column out of 7 columns in dataset.

- SUM of **Sales**: 1956055840
- AVERAGE of **Sales**: 4548967
- MAX of **Sales**: 82900000 (Wii Sports is the highest number of game copies sold!)
- MIN of **Sales**: 1000000
- MEDIAN of **Sales**: 2060000
- MODE of **Sales**: 1000000 (Note: I didn't do MODE on pivot table; however I did the calculation on different sheet... it was already obvious to me that the common number of game copies sold is going to be 1000000)
- STDEV of **Sales**: 7123725.629

Finally, I downloaded my cleaned dataset as a .csv file and saved it to my folder for further data visualization and in-depth analysis using Python.

---

# Python documentations

This documentation will track changes and activities made to Python code in Jupyter Notebook.

**Data Visualization:** 

**Correlation analysis:**
