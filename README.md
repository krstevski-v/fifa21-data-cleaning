# FIFA 21 Data Cleaning

# 1. Project Background
This project focuses on cleaning raw data from FIFA 21 (now called EA Sports FC), a football simulation video game which is one of the most popular games worldwide.

The goal of the project is to transform the raw dataset into a clean and structured format that can be used for meaningful analysis and visualizations.

# 2. Data Structure

The dataset consists of **18979 records**, each one representing a football player available in-game. 

The scraped data contains information regarding the player's **real-life attributes**(age, nationality, contract details, etc.) and **in-game abilities**(shooting, passing, dribbling, pace, etc.) Each record has 77 attributes, making the dataset very rich in detail.


# 3. Data Cleaning & Wrangling

Steps taken to clean and enrich the data:

* Removed duplicate records
* Removed several attributes which provided no analytical value, such as external image links.
* Properly formatted all textual values, removing various extraneous characters and symbols, newline and tab characters, blanks and improperly rendered unicode characters.
* Created a new column "Main Position" to separate each player's strongest position from the other positions available to him.
* Built a look-up table and created a new column "Role", segmenting players into four categories based on their main position.
* Split the "Team & Contract" attribute into three separate columns: Team, Contract Start Year and Contract End Year.
* Calculated contract length for each player.
* Standardized and converted height & weight values to the metric system.
* Formatted textual financial data into proper numeric values expressed in Euros.


## Recommendations for future work
The dataset provides a good foundation for further exploration and analysis. Potential project ideas include:
  * Comparing real world performance data with in-game stats to measure the accuracy of FIFA's ratings.
  * Tracking player progression across different editions of the game to analyze player development over time.
  * Building a player recommendation model based on criteria like position, rating, budget and age.
