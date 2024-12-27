# Google Sheets documentations

This documentation will track changes and activities made to Google Sheets. This practice will not only enhance my documentation skills but also foster good habits for myself and future employers, coworkers, and managers. They will be able to monitor the modifications I've made to Google Sheets or other programming languages.

**IMPORTANT NOTE:** This dataset covers the period from November 1990 to March 2022, and therefore does not include any information or an updated dataset after 2022.

**IMPORTANT NOTE:** The 'Sales' column does not indicate the amount of money earned. Instead, it represents the total number of game copies sold.

## Documentation Begins here

### 1. Data Cleaning and Preparation

**Handle missing values:** 32% of the 430 Genre values (rows) were missing. I used Google and Gemini AI to determine the genre for the Games column and fill them up.

**Data type consistency:** In order to keep columns cleaned with one data type individually, I clicked on column A to select all range in column A -> Format -> Plain text because column A, **Game**, is a string. Same goes for all columns except **Sales** and **Release Date** columns. **Sales** column is a number type, and **Release Date** is a date type. I also caught an error on date column for *Super Scope 6 game*; therefore, I fixed it, and input the best estimate for release date which is 2/1/1992. I also select all cells and then click on Data -> Data cleanup -> Trim whitespace AND Remove duplicate to remove whitespaces and duplicates.

As I am editing on December 24, 2024, I noticed there are mistakes in string for **Publisher** column. The Pokémon Company is responsible with brand management while Nintendo publish worldwide; therefore, it should be typed "The Pokémon Company, Nintendo" instead of "The Pokémon Company" or "Nintendo, The Pokémon Company". I also doubled checked on google to see if any of Pokémon game series is either made by Nintendo as single, or both The Pokémon Company and Nintendo (The Pokémon Company, Nintendo)

On December 26, 2024, I observed that the Genre column contained two entries for the same genre with different spellings: 'Platform' and 'Platformer'. To ensure data consistency, I standardized the spelling by replacing all instances of 'Platform' with 'Platformer' in the Genre column.

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

Finally, I downloaded my cleaned dataset as a .csv file and saved it to my folder for further data visualization and in-depth analysis using Python. Check out a file called [nintendo.ipynb](https://github.com/erickarambulo/nintendo/blob/main/nintendo.ipynb) that is attached to main branch. That file contains a showcase of my data visualization and coding skills. I recommend to keep reading documentation.md file for both data visualizations and analyses without code. If you want to view the code without analyses, please refer to [nintendo.ipynb](https://github.com/erickarambulo/nintendo/blob/main/nintendo.ipynb).

---

# Python documentations and analysis

This documentation will track changes and activities made to Python code in Jupyter Notebook. This also display my data analysis skill.

**Data Visualization:** 

- Line plot: Sales Over Time

![download](https://github.com/user-attachments/assets/315398bb-0ef1-4120-8459-ebcccbc97f79)

The year 2006 saw the highest sales, primarily driven by the release of the Wii, the first motion-controlled gaming console, which was bundled with the popular Wii Sports game.

- Bar Chart: Top 10 Selling Games

![download](https://github.com/user-attachments/assets/314c186c-3025-499d-b4b6-84508e38fe42)

Notice that Wii Sports, Wii Sports Resort, and Wii Play comprised the largest sales within the sports genre. Most of the top-selling games belong to the Mario series, which consistently enjoys high popularity within the Mario franchise. Zelda also made a strong showing, securing a place within the top 10.

- Bar Chart: Top 10 Developers

![download](https://github.com/user-attachments/assets/06d41d7b-0550-49bd-aae5-89b2a1a871f9)

Looking at this chart of Top 10 Developers, we see the top 3 are very close in ranking. Nintendo EAD and EPD are quite similar, as both produce major titles like the Mario and Zelda series. Game Freak, renowned for the Pokémon series, occupies the second position.

- Bar Chart: Top 10 Publishers

![download](https://github.com/user-attachments/assets/9fe14328-533b-4190-bee7-63be90788026)

Unsurprisingly, Nintendo ranks as the top publisher. Notably, the top two positions are held by The Pokémon Company and Nintendo, reflecting their close collaboration on most of the Pokémon game series.

- Histogram: Analyze the distribution of sales and release dates

![download](https://github.com/user-attachments/assets/54c773f6-eb5f-4a49-8956-44178ea6bb5f)

This chart is somewhat similar to line plot, just the only difference is line plot makes more sense than histogram when it comes to Sales (y-values) vs. Years (x-values).

![download](https://github.com/user-attachments/assets/34d6282f-f427-4e15-9834-870c217c89df)

The common number of game copies sold is between 1 million and 3 million. The highest number of game copies sold is 82.9 million, achieved by Wii Sports.

- Scatter plots: Explore relationships between variables, such as sales vs. release year

![download](https://github.com/user-attachments/assets/9841215d-ce35-49ae-ab18-481e12d7c2a3)

Above here, a chart of scatterplot indicates there is no correlation between Sales and Release Date.

- Identify the most popular genres

![download](https://github.com/user-attachments/assets/890b3f6f-0ac1-4be7-9985-2b88ecf724fe)

Platformer is the most popular genre due to the success of the Mario series, which features extensive platforming elements in most of its games. Role-playing games (RPGs) rank second in popularity, likely due to players enjoying the immersive experience of embodying a character and embarking on an in-game adventure. Sports came in third, which is somewhat surprising. However, this is likely due to the exceptionally high sales of Wii Sports, Wii Sports Resort, and Wii Play which significantly contributed to the overall success of the sports game genre.

- Analyze sales trends for different genres over time

![download](https://github.com/user-attachments/assets/ab9ea349-1711-4831-a021-d102269048d1)

I selected the top three genres, Platformer, Role-Playing, and Sports, for this part. This decision was made to avoid overcrowding the line plot with ten lines. By focusing on the top three, I aim to enhance clarity for both myself and others when analyzing the trends.

- Determine the best-selling platforms for Nintendo.

![download](https://github.com/user-attachments/assets/27babe76-6e0c-48b7-8755-3bf6de03c054)

Based on this chart, the Wii currently holds the top spot. However, I suspect that Nintendo Switch would likely retain the first-place position if the dataset were updated regularly, as the last update occurred three years ago.
