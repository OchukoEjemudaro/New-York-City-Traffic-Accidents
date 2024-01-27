# NEW YORK CITY TRAFFIC ACCIDENTS ANALYSIS

A SQL and POWER BI project that examine New York City Traffic Accidents data, aiming to identify key patterns, contributing factors, and potential areas for improvement in New York City.

## Table of Content

- [Project Overview](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#project-overview)
- [Project Scope](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#project-scope)
- [Business Objective](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#business-objective)
- [Document Purpose](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#document-purpose)
- [Use Case](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#use-case)
- [Skills Demostrated](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#skills-demostrated)
- [Data Source](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#data-source)
- [Data Cleaning and Processing](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#data-cleaning-and-processing)
- [Data Analysis and Insight](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#data-analysis-and-insight)
- [Data Visualization](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents#data-visualization)
- [Recommendation](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#recommendation)
- [Conclusion](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents?tab=readme-ov-file#conclusion)

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

## Skills Demostrated

- Data Connection In SQL Server
- Data Cleaning and Preparation with SQL Server
- Data Analysis with SQL Server
- Data Connection in Power BI with SQL Server
- Data Visualization with Power BI

## Data Source
The project employs a dataset containing information on NYC traffic accidents, obtained from the [Maven Analytics](https://www.mavenanalytics.io/data-playground?page=8&pageSize=5) website, where datasets are made available for practice purposes. The dataset, available in CSV format, comprises a single table, encompassing 238,421 rows and 18 columns. This table captures comprehensive details about NYC traffic accidents, including information such as Collision ID, Date, Time, Borough, Street Name, Cross Street, Latitude, Longitude, Contributing Factor, Vehicle Type, Persons Injured, Persons Killed, Pedestrians Injured, Pedestrians Killed, Cyclists Injured, Cyclists Killed, Motorists Injured, and Motorists Killed.

Subsequently, this dataset was imported into SQL Server for further analysis.

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

For the complete data cleaning processes, Click [Here](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents/blob/main/Data_cleaning.pdf)

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

|Month_Name|Total_Accident|%_of_Total_Accident|
|----------|--------------|-------------------|
|January|23024|9.66|
|February|21207|8.89|
|March|25099|10.53|
|April|19180|8.04|
|May|19749|8.28|
|June|20079|8.42|
|July|18872|7.92|
|August|18801|7.89|
|September|18771|7.87|
|October|19148|8.03|
|November|17543|7.36|
|December|16948|7.11|

Based on the total number of accidents in each month and the corresponding percentages relative to the yearly total. 

- The percentage of total accidents varies from month to month, with some months having higher accident counts than others.
- March has the highest number of accidents with 25,099 and highest percentage relative to the total (10.53%), indicating it might be a month with increased risk or contributing factors.
- Other months with relatively high accidents include January, which has a total of 23,024 accidents (9.66%), February with a total of 21,207 accidents (8.89%), June with a total of 20,079 accidents (8.42%), and May with a total of 19,749 accidents (8.28%)
- December has the lowest total number of accidents and the lowest percentage relative to the yearly total (7.11%), followed by November with 17,543 accidents (7.36%). These lower counts in December and November might be influenced by factors like reduced outdoor activities, reduced travel during the holiday season, or increased awareness during the festive season.
- The accident counts in August, September, and October are relatively stable, ranging from 18,801 (7.89%) to 19,148 (8.03%).

**2. Break down accident frequency by day of week and hour of day. Based on this data, when do accidents occur most frequently?**

Breaking down accident frequency by day of the week and hour of the day helps to examining and analyzing the data to understand when accidents occur most often. This process aims to identify specific patterns and trends in terms of both the day of the week and the time of day when accidents are most likely to happen. By categorizing and analyzing the data in this way, it becomes possible to pinpoint certain days and times that exhibit higher accident rates.

To address this question, an extensive SQL query was executed to calculate the aggregate count of accidents occurring on a weekly basis, further categorized by different hours of the day.

```SQL
--Break Down of Accident Frequency by Day of the Week and Hour of the Day

SELECT       Week_Name,
             [0], [1], [2], [3], [4], [5], [6], [7], [8], [9], [10],
             [11], [12], [13], [14], [15], [16], [17], [18], [19], [20],
             [21], [22], [23]
FROM
(SELECT      Week_Name,
             Week_Number,
             [Hours],
             COUNT(Collision_ID) AS Total_Accidents
FROM         Tbl_NYC_Traffic_Accidents
GROUP BY     Week_Name,
             Week_Number,
             [Hours]) AS Derived_Table
			
PIVOT(       SUM(Total_Accidents)
             FOR [Hours]
             IN ([0], [1], [2], [3], [4], [5], [6], [7], [8], [9], [10],
             [11], [12], [13], [14], [15], [16], [17], [18], [19], [20],
             [21], [22], [23])) AS PIV_
ORDER BY     Week_Number
```
|Week_Name|0|1|2|3|4|5|6|7|8|9|10|11|12|13|14|15|16|17|18|19|20|21|22|23|
|---------|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|-|
|Sunday|2035|1377|1171|1127|1279|901|783|668|850|926|1057|1245|1363|1430|1659|1608|1683|1651|1599|1507|1412|1395|1296|1179|
|Monday|1495|753|573|465|563|700|999|1397|1949|1706|1572|1614|1645|1690|2004|2094|2150|2130|1875|1551|1301|1177|1015|915|
|Tuesday|1236|483|369|347|305|543|957|1341|2154|1803|1620|1661|1768|1850|2040|2253|2253|2277|2061|1664|1344|1183|1145|999|
|Wednesday|1231|533|433|358|364|532|1022|1376|2019|1690|1628|1668|1765|1802|2143|2253|2379|2261|2039|1701|1421|1227|1191|1017|
|Thursday|1346|603|433|387|425|556|943|1325|2045|1736|1676|1703|1762|1778|2124|2215|2314|2341|2101|1756|1487|1270|1221|1098|
|Friday|1532|717|594|511|534|580|993|1324|1957|1710|1588|1741|1982|1923|2164|2386|2447|2463|2216|1893|1625|1571|1534|1511
|Saturday|1883|1270|1118|1115|1097|869|775|779|1072|1111|1357|1452|1625|1637|1789|1768|1839|1815|1782|1620|1704|1523|1502|1535|

From the above analysis;

- Accidents consistently occur across all days, with notable peaks during rush hours. 
- Weekdays, from Monday to Friday, in the mornings from 7 am to 9 am and in the evenings from 4 pm to 6 pm, exhibit a clear pattern of increased accidents, indicating a correlation with rush hour traffic and commuting patterns. The spike in accidents during weekday mornings may be associated with increased vehicular activity as people head to work, school, or other obligations, while during the evening, it may also be linked to the period when individuals are returning home from work or school.
- Saturdays and Sundays showcase a shift in accident patterns, with higher accident frequencies observed during the afternoon and evening hours from 1 pm to 8 pm. This temporal shift suggests a potential association with weekend leisure activities or increased travel during these hours. 
- Both Saturday and Sunday between 12am and 4am show high accident counts during late-night hours, indicating potential issues related to nightlife and early-morning activities.
- Friday and Saturday nights from 9 pm to 11 pm also present high accident counts during late-night hours, possibly indicating a correlation with increased social activities or nightlife.

**3. On which particular street were the most accidents reported? What does that represent as a percentage of all reported accidents?**

This involves identifying the street where the highest number of accidents occurred and determining the percentage this count represents compared to the total number of reported accidents. To provide an answer to this question, a query is needed to pinpoint the specific street where the highest number of accidents were reported and calculate the percentage relative to the overall total number of reported accidents.

```SQL
-- Top 5 Streets with the most Reported Accidents

Select		Top 5
		Street_Name, 
		COUNT(Collision_ID) AS Total_Accidents,
		ROUND(CAST(COUNT(Collision_ID)AS FLOAT)/(SELECT CAST(COUNT(Collision_ID) AS FLOAT)
		FROM Tbl_NYC_Traffic_Accidents)*100,2) AS [%_of_Total_Accident] 
FROM 		Tbl_NYC_Traffic_Accidents
GROUP BY 	Street_Name
ORDER BY 	COUNT(Collision_ID) DESC
```

|Street_Name|Total_Accident|%_of_Total_Accident|
|----------|--------------|-------------------|
|Belt Parkway|3728|1.56|
|Broadway|2794|1.17|
|Atlantic Avenue|2230|0.94|
|Long Island Expressway|2165|0.91|
|Brooklyn Queens Expressway|2159|0.91|

From this analysis;

- The highest number of accidents occurred on Belt Parkway, accounting for 1.56% of the total reported accidents and Broadway follows closely behind with 1.17% of the total accidents.
- Atlantic Avenue, Long Island Expressway, and Brooklyn Queens Expressway have relatively similar accident counts, each representing around 0.91% to 0.94% of the overall total accidents.

Belt Parkway and Broadway experience a higher frequency of accidents compared to the other mentioned locations.

**4. What was the most common contributing factor for the accidents reported? What about for fatal accidents specifically?**

This first part of the question “What was the most common contributing factor for the accidents reported?” seeks to identify the factor that played the most significant role in the occurrence of reported accidents, helping to prioritize interventions or safety measures to address the common causes of accidents. To determine the most contributing factor, a query was executed to calculate the total number of accidents associated with each contributing factor and their respective percentages relative to the overall total number of reported accidents.

```SQL
--Top 5 Contributing Factor by Reported Accident

Select		Top 5
		Contributing_Factor, 
		COUNT(Collision_ID) AS Total_Accidents,
		ROUND(CAST(COUNT(Collision_ID)AS FLOAT)/(SELECT CAST(COUNT(Collision_ID) AS FLOAT)
		FROM Tbl_NYC_Traffic_Accidents)*100,2) AS [%_of_Total_Accident] 
FROM 		Tbl_NYC_Traffic_Accidents
GROUP BY	Contributing_Factor
ORDER BY 	COUNT(Collision_ID) DESC
```
|Contributing_Factor|Total_Accident|%_of_Total_Accident|
|----------|--------------|-------------------|
|Unspecified|59549|24.98|
|Driver Inattention/Distraction|58308|24.46|
|Failure to Yield Right-of-Way|16555|6.94|
|Following Too Closely|15519|6.51|
|Passing or Lane Usage Improper|10733|4.5|

From the above analysis;

- Accidents with an unspecified contributing factor account for the highest percentage (24.98%) of the overall total accidents. The term "unspecified" indicating cases where the contributing factor is known to be unspecified or unknown
- Driver inattention or distraction is the second most common contributing factor, causing 24.46% of the reported accidents. This highlights the critical role of attentiveness and focus while driving, indicating a potential area for targeted awareness campaigns or interventions to reduce distracted driving.
- Failure to yield right-of-way is a notable contributing factor, causing 6.94% of accidents. This emphasizes the importance of proper adherence to traffic rules and yielding procedures, suggesting potential areas for traffic education and enforcement.
- Accidents resulting from following too closely represent 6.51% of the total accidents. This indicates that maintaining a safe following distance is crucial to prevent rear-end collisions, suggesting educational initiatives on safe driving distances.
- Improper passing or lane usage contributes to 4.5% of accidents. This insight highlights the significance of proper lane discipline and safe passing practices, indicating a potential focus area for traffic safety measures.

The second part of the question, 'What about for fatal accidents specifically,' directs attention to incidents resulting in fatalities. The question aims to identify the total number of accidents caused by contributing factors where the outcome was fatal. To provide answer to this question, a query was executed to calculate the total number of accidents caused by these contributing factors specifically in cases where the outcome was fatal.

```SQL
-- Top 5 Contributing Factor Resulted to Fatal Accidents.

Select		Top 5
		Contributing_Factor, 
		COUNT(Collision_ID) AS Total_Accidents
FROM 		Tbl_NYC_Traffic_Accidents
WHERE 		Persons_Killed > 0
GROUP BY 	Contributing_Factor
ORDER BY 	COUNT(Collision_ID) DESC
```

|Contributing_Factor|Total_Accident|
|----------|--------------|
|Unspecified|185|
|Unsafe Speed|130|
|Driver Inattention/Distraction|74|
|Failure to Yield Right-of-Way|46|
|Traffic Control Disregarded|33|

From the above analysis;

- Fatal accidents with an unspecified contributing factor account for 185 cases. The high number of fatalities with an unspecified factor suggests a need for more detailed and precise reporting to better understand the root causes of fatal accidents.
- Fatal accidents attributed to unsafe speed amount to 130 cases. The association of speed with fatalities underscores the critical role of adhering to speed limits for overall road safety.
- Driver inattention or distraction contributed to 74 fatal accidents. This emphasizes the severe consequences of distractions while driving, highlighting the need for focused and attentive driving habits.
- Fatal accidents resulting from a failure to yield right-of-way total 46 cases. This insight underscores the importance of proper yielding procedures and adherence to traffic rules to prevent fatal collisions.
- Fatal accidents where traffic control was disregarded amount to 33 cases. Disregarding traffic control signals or signs contributes significantly to fatal outcomes, suggesting the need for enhanced compliance and enforcement measures.

## Data Visualization

This data visualization was created using Power BI, each visual created displays information for each question in the business objective.

![](https://github.com/OchukoEjemudaro/New-York-City-Traffic-Accidents/blob/main/Dashboard.png)

You can also interact with the report [Here](https://app.powerbi.com/view?r=eyJrIjoiMDllNGM1YzEtODkxZS00NTUxLWIxMTAtNDJmM2ExNGRhZDYwIiwidCI6ImRmODY3OWNkLWE4MGUtNDVkOC05OWFjLWM4M2VkN2ZmOTVhMCJ9)

## Recommendation
- Public awareness campaigns could be tailored to address specific months where accidents tend to be higher, encouraging responsible behavior and caution during those times.
- Consider reinforcing traffic enforcement measures during months with higher accident rates. This can include increased patrols, stricter adherence to traffic rules, and enhanced monitoring of high-risk areas.
- Develop and implement educational programs to inform the public about safe driving practices and potential risks during specific months. This can contribute to a culture of responsible driving.
- Collaborate with law enforcement agencies, local authorities, and community organizations to create a comprehensive approach to accident prevention. Joint efforts can have a more significant impact.
- Targeting safety campaigns and law enforcement efforts during identified peak hours, especially during rush hours on weekdays and weekend evenings, could lead to a significant reduction in accident rates.
- Implement community engagement programs to raise awareness about road safety and encourage responsible driving behaviors.
- Regularly review and update traffic infrastructure to align with the evolving needs of the community and advancements in safety standards.

## Conclusion

In conclusion, this analysis provides a foundation for evidence-based decision-making aimed at reducing traffic accidents, improving road safety, and enhancing the overall well-being of the community. The collaboration of various stakeholders, including city planners, law enforcement, and community organizations, will be essential for the successful implementation of recommended measures.

Thank You For Reading


---

I’m interested in a Data Analyst role in an organization where I can showcase my skills, take more responsibilities, continue to learn, an organization that I can grow with, where my work will be highly beneficial to the organization.

You can reach me on ochukoejemudaro@gmail.com or [Twitter](https://twitter.com/iamochuks/) or [LinkedIn](https://www.linkedin.com/in/ochukoejemudaro01)

THANK YOU

