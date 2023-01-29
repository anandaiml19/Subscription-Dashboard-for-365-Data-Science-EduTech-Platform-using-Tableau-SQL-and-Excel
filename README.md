<h1 align="center">Subscription / Sales Dashboard for Data science EdTech Platform using-Tableau-SQL-and-Excel <a href="https://public.tableau.com/app/profile/krishna.anand7092" target="_blank" rel="noreferrer"> <img src="https://github.com/anandaiml19/Subscription-Dashboard-for-365-Data-Science-EduTech-Platform-using-Tableau-SQL-and-Excel/blob/main/Images/Tableau.jpg" alt="tableau" width="55" height="40"/> </a> </h1>

  
**I am sharing 365 Data Science EdTech platform students engagement - A Data Analysis Project performed on Tableau & SQL in my journey into Data Science.** 

### __About Project👨‍💻__ 

•	The main objective is to build a single page dashboard with key metrics, insights and visualizations on student engagement in EdTech Platform.

•	My SQL & Excel is used for data preparation

•	Developed a Tableau Dashboard to perform analysis, producing quantitative visualization in Tableau to draw valuable insights based on different parameters affecting the company performance and determine what action can be undertaken to improve the company’s growth and deliver its students the best learning experience

__Technologies Used:⚙️__

•	My SQL

•	MS Excel

•	Tableau

 __Project - Subscription / Sales Dashboard for Data science 365 EdTech Platform performed on Tableau & SQL__
  
<p align="center"> 
  
[Tableau Dashboard link](https://public.tableau.com/app/profile/krishna.anand7092)

![https://public.tableau.com/app/profile/krishna.anand7092](https://github.com/anandaiml19/Subscription-Dashboard-for-365-Data-Science-EduTech-Platform-using-Tableau-SQL-and-Excel/blob/main/Images/Subscription_Dashboard.jpg)

__Problem statement:__

The CEO of the company interested to know the following insights from the dashboard:

•	Top 5 Most watched courses-based on minutes watched and rating.

•	Countries with most subscribed users and maximum minutes watched (Top5).

•	 Performance of the student engagement with EdTech platform and identify key areas of improvement.

•	How do the student engage with the platform based on the user type (free or paid), subscription type (monthly, quarterly, annual) and country?

•	Is student subscription seasonally dependent?

### Approach - Project Planning & Aims Grid
  
#### 1. Purpose: What? Why? What do we want to achieve?

student engagement with the 365 platform, and identify key areas of improvement.

#### 2.  Who will be involved?
- CEO 
- Director 
- Data & Analytics Team.

#### 3. End Result: What do we want to achieve?
Results and certain insights from the 365 data science Dashboard can determine what action can be undertaken to improve the company's growth and deliver its students best learning experience.

#### 4. Success Criteria: What will be our success criteria?
- CEO can gain insights for better decision making and further performance improvement
- Key metrics, country wise and periodic distribution of students can help to improve the course quality.
- Subscription details can give insights on students enrollement on different courses.

__Data Analysis – Approach__

<p  align="center"><a href="https://public.tableau.com/app/profile/krishna.anand7092"><img width="50%" src="https://github.com/anandaiml19/Subscription-Dashboard-for-365-Data-Science-EduTech-Platform-using-Tableau-SQL-and-Excel/blob/main/Images/data%20analysis%20approach1.jpg" /></a></p>


__Steps Involved:__

Step 1: Download file FROM EdTech platform

Step 2: Prepare Data using Excel and My SQL

Step 3: Download [Tableau Public](https://www.tableau.com/products/public/download) (Free) or [Tableau Desktop](https://www.tableau.com/products/desktop/download) (14 days trial) to perform Data Analysis

Step 4: Connect Tableau with MySql database or Excel database

Step 5: Save the file as (.twb or .twbx)

__Data Preparation using Excel__ 

•	Lookup Function, Index and match, SUMIFS, Pivot table are used.

![https://public.tableau.com/app/profile/krishna.anand7092](https://github.com/anandaiml19/Subscription-Dashboard-for-365-Data-Science-EduTech-Platform-using-Tableau-SQL-and-Excel/blob/main/Images/Excel_1.jpg)



__Data Analysis using SQL__

MySQL code to show the total minutes, total student count and avearge minutes watched:

``` 
with sales_sum as
(
SELECT course_id, minutes_watched,student_id,
SUM(minutes_watched) as total_minutes,
COUNT(student_id) as total_stud_counts
FROM 365_student_learning
group by course_id, minutes_watched,student_id
order by course_id, minutes_watched,student_id)
select s.course_id,
```

MySQL code to show the total rating, total rating count and avearge rating:__

```
with ratings_sum as
(select course_id,student_id,course_rating,
sum(course_rating) as total_rating,
count(student_id) as tot_stud_count
from 365_course_ratings
group by course_id,student_id,course_rating
order by course_id,student_id,course_rating)
select r.course_id,
ROUND(sum(r.total_rating),2) as tot_rating,
count(r.tot_stud_count) as total_rat_count,
ROUND(sum(r.total_rating)/count(r.tot_stud_count),2) as ave_rating
from ratings_sum as r
group by r.course_id
```

### Data Analysis using Tableau

Tableau Case  Code to calculate the subscription type:

```
CASE [Subscription Type]
WHEN "All" then ([Purc Type] = [Purc Type])
WHEN "Monthly" then ([Purc Type] = "0")
WHEN "Quarterly" then ([Purc Type] = "1")
WHEN "Annual" then ([Purc Type] = "2") 
WHEN "Free" then ([Purc Type] = "NULL") END
```

Tableau Case Code to calculate the subscription type:

```
CASE [User Type]
when "All" then ([Paid/Free] = [Paid/Free])
when "Free" then ([Paid/Free] = 0)
when "Paid" then ([Paid/Free] = 1) END
```
__Project reference__🔗
[365 Datascience](https://learn.365datascience.com/projects/)

### Liked my Contributions:question:[Follow Me](https://github.com/anandaiml19):point_right: [Nominate Me for GitHub Stars](https://stars.github.com/nominate/) :star: :sparkles:
##For any doubts/queries 🔗 👇
                                                                                                                            
[linkedin](https://in.linkedin.com/in/dr-krishna-anand-v-g-70bba623)
