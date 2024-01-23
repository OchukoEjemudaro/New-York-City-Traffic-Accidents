# ANALYSIS OF NEW YORK CITY TRAFFIC ACCIDENTS

A SQL and POWER BI project that examine New York City Traffic Accidents data, aiming to identify key patterns, contributing factors, and potential areas for improvement in New York City.

## Project Overview

Addressing the prominent issue of traffic accidents in New York City necessitates a comprehensive analysis of the underlying patterns and contributing factors associated with these incidents. This project is essential for the development and implementation of effective preventive measures aimed at enhancing overall safety within the city. 

This project seeks to undertake a comprehensive examination of New York City traffic accidents data, with the objective of identifying key patterns, contributing factors, and potential areas for improvement in New York City.
This project is centered on the analysis of motor vehicle collisions reported by the New York City Police Department, encompassing the data recorded from January 2021 to April 2023.

## Project Scope

This project entails a thorough analysis of NYC traffic accidents data, with a specific focus on motor vehicle collisions reported by the New York City Police Department. The analysis covers the period from January 2021 to April 2023 and incorporates data from all boroughs of New York City.

## Business Objective

The primary objective of this analysis is to explore how accidents are dispersed across months to identify any seasonal patterns. Additionally, it aims to dissect accident frequency by both the day of the week and the hour of the day to pinpoint when accidents occur most frequently. The analysis will further identify the specific street with the highest reported accidents, highlighting critical areas for potential safety improvements. Moreover, the project seeks to determine the most common factors contributing to accidents, with a specific focus on understanding those associated with fatal accidents.

## Document Purpose

This documentation serves as a guide for project stakeholders, providing insights into the project's objectives, data sources, data analysis, visualizations, and any other relevant information. 

## Use Case

Several stakeholders can benefit from the insights derived from this analysis of NYC traffic accidents. Here are key stakeholders who could make use of this analysis and benefit from it.

-	**Traffic Safety Authorities:** Traffic safety authorities can utilize the findings to target awareness campaigns, law enforcement efforts, and specific interventions in areas and times identified as having high accident frequencies.
-	**Law Enforcement Agencies:** Police departments can use the analysis to allocate resources effectively, plan for heightened enforcement during peak accident times, and prioritize areas with a high occurrence of accidents.
-	**Emergency Services:** Emergency service providers can benefit from the insights to optimize response times and resource allocation in areas prone to frequent accidents.
-	**Community Advocates:** Community groups and safety advocates can use the information to raise awareness, advocate for improvements in specific locations, and collaborate with authorities to enhance road safety.
-	**City Planners and Urban Developers:** City planners can use the analysis to identify high-accident areas and patterns, informing decisions about infrastructure improvements, traffic flow management, and safety measures to enhance overall urban planning.

## Data Source
The project employs a dataset containing information on NYC traffic accidents, obtained from the Maven Analytics website, where datasets are made available for practice purposes. The dataset, available in CSV format, comprises a single table, encompassing 238,421 rows and 18 columns. This table captures comprehensive details about NYC traffic accidents, including information such as Collision ID, Date, Time, Borough, Street Name, Cross Street, Latitude, Longitude, Contributing Factor, Vehicle Type, Persons Injured, Persons Killed, Pedestrians Injured, Pedestrians Killed, Cyclists Injured, Cyclists Killed, Motorists Injured, and Motorists Killed.

Subsequently, this dataset was imported into Microsoft SQL Server for further analysis.

## Data Cleaning and Processing

A thorough data cleaning and preparation process was executed on the key columns of the dataset involved in this analysis. This ensures that my analyses are based on a solid foundation, leading to more reliable results and informed decision-making. The following processes were undertaken on the key column of the dataset to ensure high data integrity, accuracy, and to enhance the overall quality of the dataset.

**1. Removing Duplicates** 

Duplicate entries can lead to inaccurate results and analyses, as they can compromise the integrity of the dataset, making it challenging to maintain consistency and reliability. While duplicate entries can compromise the integrity of the dataset, leading to inaccurate results and analyses, a comprehensive examination revealed that this dataset contains no duplicate records. This ensures the dataset's consistency and reliability.

**2. Handling Missing Values** 

Handling missing values is essential for maintaining data quality, ensuring accurate analyses, and extracting meaningful insights from the dataset. It is a critical step in the data cleaning and preparation process before conducting any robust data analysis.

After a comprehensive cleaning process, it has been revealed that the NYC traffic data includes 8,783 rows with missing values in one or more key columns. Missing values in the key columns of this dataset indicate incomplete information. Despite the incompleteness, the rows containing these missing values are crucial for this analysis. Therefore, they were addressed separately and were retained rather than deleted.

As they were addressed separately, it was determined that among the 8,783 rows with missing values in the NYC traffic accident data, 7,197 relate to the Borough column. These missing values signify that the borough where the accident occurred is unknown. Consequently, the missing values in the Borough column were substituted with the term 'Unknown'.

Additionally, in the NYC traffic accident data, it was identified that 363 out of 8,783 rows have missing values in the Street Name column. These missing values indicate that the street where the accident occurred is unknown. Therefore, the missing values in the street column were replaced with the term 'Unknown'.

Furthermore, in the NYC traffic accident data, it was observed that 1,287 out of 8,783 rows have missing values in the Contributing Factor column. These missing values signify that the factors contributing to the accident for the designated vehicle are unknown. Notably, the Contributing Factor column already incorporates the term ‘Unspecified,’ explicitly indicating cases where the contributing factor is known to be unspecified or unknown. Consequently, the missing values were replaced with the term ‘Unspecified’ instead of using 'Unknown'. This decision was made to eliminate ambiguity and potential misrepresentation of the nature of the missing values.

With the exception of a few specified columns, all other key columns in the dataset contain complete information.

**3. Validation of Spelling and Categorization** 

A meticulous review was conducted to validate the correctness of spellings and the accuracy of categorization in NYC Traffic Accident data, ensuring consistency and reliability.

**4. Correcting Data Types** 

Ensured that data types are appropriate for each field (e.g., converting date field to date data type and time field to time data type) to facilitate accurate analysis.

The following processes were also carried out on New York City Traffic Accident data during data processing.

- **Added New Columns**

New columns were added to NYC Traffic Accident data. These columns are Year, Month Number, Month Name, Week Name, Week Number, Hours and Minutes. These columns are important in this analysis. They helped in exploring how accidents are dispersed across months to identify any seasonal patterns. They also helped to dissect accident frequency by both the day of the week and the hour of the day to pinpoint when accidents occur most frequently.

- **Added Primary Key to the Collision ID Columns**

A primary key ensures that each record in the table is uniquely identified. This uniqueness prevents the occurrence of duplicate or identical records in the table, maintaining data integrity. Adding a primary key to a column is essential for maintaining data quality, optimizing query performance, and ensuring the overall integrity of a relational database.

After the execution of data cleaning and processing, the dataset for this analysis is now well-structured, consistent, and free from significant issues that could hinder analysis or interpretation. The data adheres to standardized formats and consistent naming conventions. All necessary data fields are present and well populated, the data values are accurate, data types are appropriately assigned to each column, and there are no duplicate records. 

## Data Analysis and Insight

The main goal of this analysis is to examine the distribution of accidents throughout different months, aiming to uncover any seasonal patterns. Furthermore, it seeks to analyze accident frequency based on both the day of the week and the hour of the day to pinpoint peak occurrence times. The analysis will also identify the particular street with the highest reported accidents, shedding light on crucial areas for potential safety enhancements. Additionally, the project aims to ascertain the prevailing factors contributing to accidents, with a specific emphasis on understanding those linked to fatal incidents.

This analysis provides answers to the following questions

**1. Compare the percentage of total accidents by month. Do you notice any seasonal patterns?**

This analysis involves the distribution of total accidents across different months and inquiring whether there are any discernible patterns that repeat throughout the year. To identify seasonal patterns in the NYC Traffic Accident data, an in-depth time-based analysis was conducted to uncover seasonal trends and patterns in the data, aiming to gain valuable insights into the overall patterns within the dataset over time. This endeavor involved the execution of a comprehensive SQL query designed to calculate the percentage of total accidents for each month relative to the overall dataset. By comparing these percentages, I was able to identify if there are recurring pattern in accident rates across different months.

```SQL
--Comparing the Percentage of Total Accidents by Month
SELECT    Month_Name,
          COUNT(Collision_ID) AS Total_Accident,
          ROUND(CAST(COUNT(Collision_ID)AS FLOAT)/(SELECT CAST(COUNT(Collision_ID) AS FLOAT)
          FROM Tbl_NYC_Traffic_Accidents)*100,2) AS [%_of_Total_Accident]
FROM      Tbl_NYC_Traffic_Accidents
GROUP BY  Month_Name,
          Month_Number
ORDER BY  Month_Number
```

















