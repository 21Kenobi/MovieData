# Movie Data Analysis Project
## Table of content : 
 - [Project Overview](#project-overview)
 - [Data Source](#data-sources)
 - [Results](#results-and-findings)
 - [Challenges in Analysis](#challenges-in-analysis)
### Project Overview
This data analysis project aims to provide insights into the performance and trends of movies from 2012 to 2016
By analysing various aspects of the movie data, we seek to identify patterns, make data-driven recommendations, and gain a deeper understanding of the industry's dynamics.

### Data Sources
Movie Data : the primary dataset used for this analysisis the "Movie Data Homework.xmls" file, containing detailed information about each movie's performance, actors, directors etc.
[Movies Data Homework.xlsx](https://github.com/user-attachments/files/16405599/Movies.Data.Homework.xlsx)

### Tools
 - Power Query - I used Power Query for Data Cleaning
 - Excel, Pivot Table - I used them for Data Analysis, Creating Reports and visualizations
   
### Data Cleaning and Preparation
In the initial data preparation phase, we performed the following tasks:
 - Data loading and inspection.
 - Handlinng errors, missing values.
 - Data cleaning and formating.
All Power Query steps is here.The excel file after preparation process can be downloaded here  [Movies Data Work.xlsx](https://github.com/user-attachments/files/16405611/Movies.Data.Work.xlsx)


### Exploratory Data Analysis
 - Which genres were the most profitable these years?
 - Which actors were the most succesfull ?

### Results and Findings
 - Best profitable movie was: with Budget of.... Box Office Revenue was 102 000 000 USD. The genre of this movie was....
![Best Profitable Movie](https://github.com/user-attachments/assets/fd37798a-6de0-495e-b543-2393b8223067)


 - The best actor was...
![Movies Data Dashboard](https://github.com/user-attachments/assets/b24e4466-139e-4263-87ae-1e5108a5c971)



### Challenges in Analysis 
#### M language
One of interesting features/challenges I was working with a specific code for Grouping in M language with enabled me to Combine genres together for further analysis.
I had 2 column for genres, but I needed to combine them and have the same format, for example action/comedy, not comedy/action

--- 
```
 = Table.Group(#"Sorted rows", {"Movie Title"}, {{"Combined Genre", each Text.Combine([Concat Genre], " / "), type text},

            {"AllData", each _, 

                type table [Movie Title=nullable text, Release Date=nullable date, Wikipedia URL=nullable text, Concat Genre=nullable text, Director_First_ID=nullable number, Cast_First_ID=nullable number, Cast_Second_ID=nullable number, Cast_Third_ID=nullable number, Cast_Fourth_ID=nullable number, Cast_Fifth_ID=nullable number, #"Budget ($)"=nullable number, #"Box Office Revenue ($)"=nullable number, Director=nullable text, Actor 1=nullable text, Actor 2=nullable text, Actor 3=nullable text, Actor 4=nullable text, Actor 5=nullable text]}})

```
### Excel Dashboard
Can be downloaded here  [Movies Data Dashboard.xlsx](https://github.com/user-attachments/files/16405707/Movies.Data.Dashboard.xlsx)

