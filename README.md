# FIFA 21 Data Cleaning

## Project Background
This project focuses on cleaning and preparing raw data from FIFA 21 (now called EA Sports FC), a football simulator that's one of the most popular video games worldwide.

The dataset contains 18979 records, each representing a footballer with both real-life attributes(age, nationality, contract details, etc.) and in-game metrics(shooting, passing, dribbling, pace, etc.)
The goal of this project is to transform the raw dataset into a clean and structured format that can be used for meaningful analysis and visualizations.

## Data Structure
The dataset consists of a single table with 77 columns covering a wide range of player information. Although it is rich in detail, the raw data has many issues that make it unsuitable for further use without prior cleaning, such as inconsistent data types, unnecessary characters, concatenated values, duplicated rows, and poorly formatted numerical fields.

## Data Cleaning & Preparation
To prepare the data for meaningful insights, I performed the following cleaning steps:

1. **Removal of Unnecessary Information**:
      - Dropped irrelevant columns such as external website links that don't contribute to player analysis.
    
2. **Handled Duplicate Records**:
      - Identified and removed a duplicate entry using the player ID attribute.

    
3. **Fixed Inconsistent Data Types**:
      - Standardized each column to the correct format, e.g making sure ratings were stored as numbers, salaries as monetary values, and names as text.

    
4. **Organized Player Positions**
      - Split the "Positions Played" column into two new ones: Main Position and Secondary Positions.
      - Created a new column called **Role** that grouped players into Goalkeepers, Defenders, Midfielders or Forwards based on their main position.

    
5. **Cleaned up Contract Information**:
     - Extracted the team name from "Team & Contract" column
     - Split contract data into separate contract start and end years.
     - Calculated the length of each player contract.


    
6. **Standardized Text and Formatting**:
    - Cleaned up column names containing unnecessary symbols.
    - Trimmed extra spaces, tabs and newline characters from all data entries.


    
7. **Converted Units**:
      - Converted height to centimeters and weight to kilograms for easier comparison.

    
8. **Formatted Financial Data**:
      - Cleaned and structured financial figures like market value, release clause and wages into usable numeric formats.
  
  All transformations were done in Excel using a combination of Power Query, formulas and data formatting features.

## Sample Transformations
Before:
![EXCEL_gaOEAixCRT](https://github.com/user-attachments/assets/dd34dc6c-31b1-4fdf-b84c-574e59962c51)

After:

![EXCEL_wpkA8tsFFj](https://github.com/user-attachments/assets/4b08a2d1-51bb-41ab-b27f-091d4ad6320d)

-----------------------------------------------------------------------------------------------------------------

Before:

![EXCEL_jal5FvWHXR](https://github.com/user-attachments/assets/773108e7-815f-44e9-a338-bcd8b83b99e4)

After:

![EXCEL_57yVS2LPLt](https://github.com/user-attachments/assets/65e364e0-9b42-4cf3-a439-529a7635c0e6)



## Recommendations for future work
The dataset provides a good foundation for further exploration and analysis. Some project ideas include:
  * Comparing real world performance data with in-game stats to measure the accuracy of FIFA's ratings.
  * Tracking player progression across different editions of the game to analyze player development or decline over time.
  * Building a player recommendation model based on criteria like position, rating, budget and age.
