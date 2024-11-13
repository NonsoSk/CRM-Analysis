# CRM-Analysis

![Main back](https://github.com/user-attachments/assets/ab435edb-c92f-454a-9161-0dde72d136df)

# Introduction

This is a Google sheet based project on the Maven Tech sales dataset.  For clarity, Maven Tech is a company that specializes in computer hardware sales to large businesses. 
The purpose of this analysis is to develop a dashboard that provides Maven Tech’s sales managers with clear visibility of the team’s quarterly performance, particularly focusing on tracking won opportunities, identifying top-performing agents, and understanding overall win rates. 

In this analysis, we will show the number of sales opportunities won and lost by various sales agents across four quarters of the year 2017. Each quarter has detailed insights into both the number of opportunities won and lost, as well as a breakdown by each sales agent’s individual performance.
This visibility outside of the CRM (Customer Relationship Management) platform is intended to help managers make more informed decisions, identify areas for improvement, and optimize sales strategies.


## Problem Statement

The main goal is to create an interactive dashboard in Google Sheets, allowing sales managers to:
- Track won and lost opportunities by quarter.
- Identify the most effective sales agents.
- Analyze quarterly sales trends.
- Assess overall win rates and compare quarterly performance metrics.

## Overview

To address the need for sales performance tracking outside of the CRM, we have created an interactive Google Sheets dashboard. This dashboard consolidates CRM data into a single visual display, allowing managers to monitor key metrics across different quarters. The approach taken involved structuring the data in Google Sheets, designing charts to visualize key metrics, and setting up filters that allow for easy segmentation by quarter and by individual sales agents.

**In the course of this analysis, I demonstrated the following skills:**

- **Data Structuring in Google Sheets:** The data was organized in tables to enable easy referencing and visualization.
  
- **Data Visualization:** Created pie charts, bar charts, and scorecards within Google Sheets to represent key metrics such as win rate, individual agent performance, and quarterly won opportunities.
  
- **Dashboard Design:** The dashboard was designed with a clean and intuitive layout. Important metrics like total won opportunities, win rate, and agent-specific data were highlighted.
  
- **Interactive Filters:** Added Google Sheets filters to allow users to view data for specific managers, quarters, or regions, enhancing usability for decision-making.
  
- **Data Cleaning:** For accurate analysis and results, I cleaned the data and worked on missing values.
  
- **Critical Thinking:** This skill was applies as proper analysis needs great reflection and critical  thinking.

I obtained the data by downloading the archived files from the Maven Analytics platform and then imported into my Google sheet. 
It is a sample dataset on Maven Tech CRM sales information. The dataset was structured to provide a complete view of customer accounts, product sales opportunities, and team details, which helps analyze and optimize sales strategies


## Data Cleaning Process

To ensure the accuracy and reliability of the dashboard, the following data cleaning steps were taken within Google Sheets:

- **Duplicate Removal:** I checked for and removed duplicate values to avoid inflated performance figures.
  
- **Consistency in Sales Agent Names:** I ensured all agent names were standardized to avoid variations, such as different spellings or abbreviations.
  
- **Data Type Verification:** I ensured that all numeric data  were properly formatted as numbers in Google Sheets, preventing errors in calculations and chart generation.

## Data Modelling and Profiling

Having imported the dataset into  google sheet, I went further to profiling the data, and these were my findings. 

- **Opportunity_id:** The opportunity Id confirmed that there are 8801 rows of data and each value was unique
  
- **Sales Agent:** I discovered there are 30 sales agents, with Darcel Schlecht making the highest sales at 747 and Wilburn Farren making the least sales at 110
  
- **Product:** There are 7 Products with GTX Basic being the highest sold and GTK 500 being the least sold.
  
- **Account:** for the account column, I discovered that there are 1427 empty columns which meant that 1427 accounts were yet to be registered. Thus, to dig further, I filtered the empty columns and discovered that all the empty accounts had deals that were either engaging or prospective, so it was thus wise not to open accounts for deals like that.
  
- **Deal stage:** there are 4 stages in the deal process here which are:
 prospecting, engaging, won and lost. From the profiling, we discovered that won deals are 4238,  while lost deals are 2473, which is approximately half of won deals. Moving further, there are 1589 deals that are on the engaging deals and just 500 still in prospect. Another discovery is that deals in the engaging stage and deals in prospect do not have closing date and closing values, which is an evident that they have not been finalized.

- **ENGAED DATE:** The date of first engagement is 20th october 2016 and the most Recent date is DEC 27 2017.
  
- **CLOSED DATE:** deals were closed from march (march 1st 2017) to dec (dec 31st 2017). What this means is that deals were closed in the last three quarters of the year.
  
- **Closed values:** The maximum deal closed was 30288 and the minimum was 0 and total being 10005534.

To get a single table to aid my analysis, I had to merge the “Sales_pipeline Table” and “sales teams table”. Since the sales_pipeline table had all the necessary columns, I used the Xlookup function to extract the “Manager” and “Regional_office” column into the Sales_pipeline Table.
The functions below were employed:

<img width="344" alt="Modelling Regional" src="https://github.com/user-attachments/assets/c9b1b19d-2bdd-4581-832f-9d29dc320ac0">

<img width="347" alt="Modelling Manager" src="https://github.com/user-attachments/assets/e9683ae1-0543-4c91-af6e-ee69acb4f69d">


## The Analysis Proper

The Image below is the final result of the dashboard.

<img width="523" alt="Overall Dashboard" src="https://github.com/user-attachments/assets/0d29cef5-5836-4af9-9a0c-1bdfabfa7992">

You can also interract with the dashboard [**HERE**](https://docs.google.com/spreadsheets/d/1aZiI6wxn8Mymjrl1Ag_az-K8-pAFCnqVSoXZ0D7I1IE/edit?usp=sharing)

I moved on to carry out my analysis with the goal of uncovering meaningful insights into sales performance and agent contributions.

Steps Taken in the Analysis:

1. Quarterly Win and Loss Analysis:
   - Summed up the total number of won and lost opportunities by quarter as can be seen below:
     
<img width="635" alt="Lost and Won opportunities" src="https://github.com/user-attachments/assets/1986e7fd-a6a9-404d-8c01-489cfe5d1c07">


   - I Calculated the percentage of lost and won opportunities also as can be seen below:
     
<img width="628" alt="Percentage of lost and won" src="https://github.com/user-attachments/assets/315f3f9b-3928-4840-a9ed-80acb9248dc1">

2. Sales Agent Performance:
   - Ranked sales agents based on their won opportunities in each quarter to identify high and low performers. The visual below will be of help.
     
   <img width="254" alt="Sales Agents Ranking" src="https://github.com/user-attachments/assets/c669c2ff-3448-4a14-a3b1-81293345c56d">
   

3. Trend Analysis:
   - I Observed trends in performance across quarters to detect any seasonal or quarterly variations, particularly noting the decline in Q4 performance compared to Q3, as can be seen here:

   <img width="221" alt="Trend Analysis" src="https://github.com/user-attachments/assets/d6722b70-bb75-4b98-b629-840191d602e3">
 
4. Visualization:
      - I used a pie chart to represent win rate in the most recent quarter, that is the 4th quater, helping to visualize the proportion of won opportunities relative to total opportunities. as evident in the visual below:
       
   <img width="224" alt="Win Percentage" src="https://github.com/user-attachments/assets/9ceac786-0184-4054-8a2f-bb5fa0dda4e3">
   
   - Secondly, I used bar charts to showcase individual agent performance in the most recent quarter also making it easy to compare contributions side by side. The image below says it all.

   <img width="259" alt="SALES AGENTS OPPORTUNITIES WON" src="https://github.com/user-attachments/assets/b317516c-7fc7-4765-9f0d-9441c63e35c8">



## Findings

1) **Overall Win Rate:**
   
<img width="628" alt="Overall win rate" src="https://github.com/user-attachments/assets/0ea37aea-6add-4e42-b28c-0b84f568ea25">

 The win rate stands at 63.15%,suggesting a fairly positive outcome, though there is room for improvement.
   
2) **Quarterly Trends:**
   
<img width="221" alt="Trend Analysis" src="https://github.com/user-attachments/assets/0b58917b-4e0a-43f5-a8d3-0cecf7bf9a7d">

We can notice the drop in won opportunities by 61 in the 4th Quarter when compared to the 3rd Quarter, indicating a potential issue in the later part of the year that may need to be addressed.

3) **Top Performing Agents:**
   
<img width="635" alt="Sales agent analysis" src="https://github.com/user-attachments/assets/185be6df-70e1-461e-8efc-4bd6df64c6f2">

Darcel Schlecht” emerged as the top performer in terms of won opportunities with 349 won opportunities, followed by “Vicki Laflamme” and “Kary Hendrixson” who had 221 and 209 won opportunities respectivelly

4) **Lost Opportunities:**
   
<img width="623" alt="Lost deals" src="https://github.com/user-attachments/assets/73c4a197-7311-452f-be70-4bab1a8f0a5e">

There were notable numbers of lost opportunities each quarter, which may highlight the need for further investigation into sales strategies or client engagement practices.

Conclusion

The analysis successfully provided insights into the quarterly sales performance of Maven Tech’s sales team. The interactive Google Sheets interactive dashboard also brings all the important numbers together, so sales managers can see trends, find top performers, and track win rates over time. This dashboard is a helpful tool outside of the CRM, making it easier to make informed decisions.


## Recommendations

Based on the insights from the analysis, here are my recommendations for Maven Tech:

1) Address Q4 Performance Drop: Investigate potential causes for the decline in won opportunities in Q4 and explore strategies to maintain consistent performance throughout the year.
   
2) Training for Low-Performing Agents: Consider additional training or support for lower-performing agents, as well as strategies to replicate the successes of top performers.
   
3) Improve Pipeline Efficiency: Look closely at why sales were lost to find common issues and make improvements. This can help turn more potential sales into actual sales.
   
4) Set Performance Goals: Establish specific performance targets for each quarter and individual agents to improve accountability and motivate continuous improvement.

# Thanks for reading.








