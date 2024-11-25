# Kickstarter Crowdfunding Analysis

## Table of Contents

- [Project Overview](#project-overview)
- [Recommendations](#recommendations)
### Project Overview

This data analysis project aims to analyze crowdfunding dynamics on platforms like kickstarter, focusing on key areas such as project success rates, geographic distribution, successful projects based on backers count and category popularity.

### Data Sources

Crowdfunding data : The primary dataset used for this analysis is the “crowdfunding_data.csv” file, containing detailed information about project status, backers, geographical data of successful projects, and categories.

### Tools

- Excel – Used for Data Cleaning 
- MySQL -  Data Analysis
- Power BI – Creating KPI’s and Dashboard

### Data Cleaning

In this phase, I identified and corrected errors in the raw data, such as:
- Handling missing values
- Removing duplicates
- Standardizing formats
- Correcting erroneous data entries

### Exploratory Data Analysis

EDA involved exploring the crowdfunding data to answer key questions, such as:
-	What is the overall successful projects?
-	What is the percentage of successful projects by category?
-	What is the percentage of successful projects by year, quarter and month?
-	Top successful projects based on backers count and Amount raised?

### Data Analysis

Performed comprehensive data analysis using MySQL, focusing on Project status, geographic distribution, and total projects based on category.

**To find the total projects status**

```sql
select State,
count(*) as total_projects
from projects
group by state;
```

**Geographic distribution of projects**

```sql
select 
     location_id
     count(*) as total_projects
from
     projects
group by
    location_id
order by
    total_projects DESC;
```

**Projects based on Category**

```sql
select
category_id,
       count(*) as total_projects
from
       projects
group by
       category_id
order by
       total_projects DESC;
```

## Power BI Dashboard

Here is a preview of the dashboard that visualizes key insights from the crowdfunding data:



### Results

The analysis results are summarized as follows:
-	Among crowdfunding projects, the success rate was significant, with 140.31k projects succeeding, while 188.24k projects failed to meet funding goals. A smaller proportion (32.5k projects) were canceled.
-	The United States dominated crowdfunding activities, hosting the majority of projects compared to other countries.
-	Categories like Product Design, Music, and Tabletop Games were the most prominent, indicating their popularity among backers and creators.
-	Crowdfunding activities peaked in 2015 but have shown a decline since, suggesting the need for innovation in platform strategies to reignite interest.

### Recommendations

Based on the analysis, we recommend the following actions:
-	Categories like Product Design and Music are highly popular, creators and platforms should focus on supporting these areas by offering targeted resources or promotional opportunities.
-	Due to the dominance of U.S.-based projects, there is an opportunity to expand crowdfunding efforts internationally by improving accessibility and awareness in other countries.
-	Platforms could consider new incentives, updated marketing strategies, or collaboration with influencers to attract new creators and backers.
-	A large number of projects fail to meet their funding goals, platforms could introduce pre-launch evaluation tools, mentorship, or educational resources to help creators better prepare for successful campaigns.

### References

[Epoch Time](https://www.epochconverter.com/)




