# Movie Data Analysis Project
## Table of content : 
 - [Project Overview](#project-overview)
 - [Data Source](#data-sources)
 - [Tools](#tools)
 - [Data Cleaning and Preparation](#Data-Cleaning-and-Preparation)
 - [Exploratory Data Analysis](#Exploratory-Data-Analysis)
 - [Challenges in Analysis](#challenges-in-analysis)
 - [Excel Dashboard](#Excel-Dashboard)
### Project Overview
This data analysis project aims to provide insights into the performance and trends of movies from 2012 to 2016. By analyzing various aspects of the movie data, the goal is to identify patterns, make data-driven recommendations, and gain a deeper understanding of the industry's dynamics.

### Data Sources
The primary dataset used for this analysis is the [Movies Data Homework.xlsx](https://github.com/user-attachments/files/16405599/Movies.Data.Homework.xlsx) , 
containing detailed information about each movie's performance, actors, directors, and more.
Note: If you want to review the steps of the work, you need to use this file as the "Source."

### Tools
 - Power Query: Used for data cleaning.
 - Excel, Pivot Table: Used for data analysis, creating reports, and visualizations.
   
### Data Cleaning and Preparation
In the initial data preparation phase, I performed the following tasks:
 - Data Loading and Inspection: Imported the dataset into Power Query and performed an initial inspection to understand its structure and contents.
 - Handling Errors and Missing Values: Identified and addressed any errors or missing values to ensure data quality.
 - Data Cleaning and Formatting: Standardized formats, corrected data types, and ensured consistency across the dataset.
All Power Query steps are documented in the Excel file. The Excel file after the preparation process can be downloaded here: [Movies Data Work.xlsx](https://github.com/user-attachments/files/16405611/Movies.Data.Work.xlsx)


### Exploratory Data Analysis & Results and Findings
This dashboard is designed for in-depth analysis of movie data. You can download the Excel dashboard from the following link: Download Excel Dashboard. It offers a comprehensive view of various metrics, including box office revenue, ROI, and budget information. The dashboard features interactive elements such as filters for genres and directors, charts displaying trends over time, and tables highlighting the most and least profitable movies, as well as top actors by box office revenue.

![Movies Data Dashboard](https://github.com/user-attachments/assets/7ef93be4-8052-4f0d-918a-5d7f04dc223b)


  - Which genre generates the highest box office revenue?
    
    ![1](https://github.com/user-attachments/assets/784ea593-5093-47a9-81a3-928f6bf0bad1)

  - How has the box office revenue changed throughout the year?
    
    ![2](https://github.com/user-attachments/assets/cccf7522-9397-484b-8826-8f59377415a2)
    
  - Which movie has the highest ROI (return on investment)?
    
    ![3](https://github.com/user-attachments/assets/4f3a0c1f-1444-4cba-82d7-5044ddfc1618)

  - Which movie has the lowest ROI (return on investment)?
    
    ![4](https://github.com/user-attachments/assets/b21ba63c-adee-41e9-8dbf-613f27ec1776)
    
  - Which movies are in the top 5 by box office revenue?
    
    ![5](https://github.com/user-attachments/assets/0c8a220f-a138-40f9-983f-3238f94a1305)

  - What is the budget of the movies in the top 5 by box office revenue?
    
    ![6](https://github.com/user-attachments/assets/baafd6b6-5804-4701-99c0-1365e74f5d16)

  - Which movies are in the top 5 by budget?
    
    ![7](https://github.com/user-attachments/assets/483b55f5-4726-4a27-9a8c-397388fc2129)

  - Which actors are in the top 5 by box office revenue?
    
    ![8](https://github.com/user-attachments/assets/692b990f-e447-48c5-b2b1-3caad6eacbf6)

  - How do different directors influence box office revenues?
    
    ![9](https://github.com/user-attachments/assets/caa6e40b-2826-4611-8f81-707d80229f9d)
    You may notice that movies with big budgets do not always guarantee high revenues.


  - How do movie budgets correlate with their box office revenues?
    
    ![10](https://github.com/user-attachments/assets/59cbc29b-3a53-4d2c-88b8-a730471c0e3f)

  - #Which directors made the movies with the highest and lowest ROI?
    
     1:
    ![12 2](https://github.com/user-attachments/assets/80634939-63bc-4331-a025-be0b161171e0)
     2:
    ![12](https://github.com/user-attachments/assets/82213125-31bd-4a0f-b942-5520cfc96aab)



  - Is there a correlation between the movie genre and its budget?
  1:
    ![13](https://github.com/user-attachments/assets/a2128677-9a3d-46d5-8e6f-ef54063ebfff)

 2:
  ![13 2](https://github.com/user-attachments/assets/d585ca45-b97c-4d94-a459-e0ed46103f4e)
  
  Visualization by genre and budget can show this relationship. For example, action and adventure films often have larger budgets.
  

  - What trends can be observed in the popularity of genres throughout the year?
1: ![14](https://github.com/user-attachments/assets/5576f288-0032-4c16-8cdb-ef5558c46556)

2: ![14 2](https://github.com/user-attachments/assets/30f9acc8-079b-470b-a67f-34c47114ea38)

 
It can be seen that some genres are consistently popular, while others have seasonal fluctuations.
    

### Challenges in Analysis 
#### M language
One of the interesting features/challenges I worked on involved a specific code for grouping in M language, which enabled me to combine genres together for further analysis. I had two columns for genres, but I needed to combine them and ensure they had the same format. For example, I wanted the format to always be "Action/Comedy" and not "Comedy/Action".

--- 
```
 = Table.Group(#"Sorted rows", {"Movie Title"}, {{"Combined Genre", each Text.Combine([Concat Genre], " / "), type text},

            {"AllData", each _, 

                type table [Movie Title=nullable text, Release Date=nullable date, Wikipedia URL=nullable text, Concat Genre=nullable text, Director_First_ID=nullable number, Cast_First_ID=nullable number, Cast_Second_ID=nullable number, Cast_Third_ID=nullable number, Cast_Fourth_ID=nullable number, Cast_Fifth_ID=nullable number, #"Budget ($)"=nullable number, #"Box Office Revenue ($)"=nullable number, Director=nullable text, Actor 1=nullable text, Actor 2=nullable text, Actor 3=nullable text, Actor 4=nullable text, Actor 5=nullable text]}})

```
### Excel Dashboard
You can download the Excel dashboard that I created for analyzing movie data from the following link: [Movies Data Dashboard.xlsx](https://github.com/user-attachments/files/16405707/Movies.Data.Dashboard.xlsx). 
This dashboard provides a comprehensive view of various metrics, including box office revenue, ROI, and budget information. It features interactive elements like filters for genres and directors, charts displaying trends over time, and tables highlighting the most and least profitable movies, as well as top actors by box office revenue. The dashboard was designed to facilitate easy exploration and analysis of the movie data, making it a valuable tool for gaining insights into the film industry.

