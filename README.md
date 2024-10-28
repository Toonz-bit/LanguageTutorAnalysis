# LanguageTutorAnalysis

### Table Of Content

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning / Preparations](#datacleaning/preparations)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Data Analysis](#data-analysis)
- [Results / Findings](#results/findings)
- [Recommendations](#recommendations)
- [Limitations](#limitations)
- [References](#references)

### Project Overview

The company has an online platform where students can register and receive online tutorials, the platform offers various Disciplines. Examples include Hausa, Yoruba, Igbo, ijaw etc. Here I did an analysis on the platform usage and below were the questions answered.

### Data Sources

Data was given Online in an excel format. I downloaded the csv file, and extracted it into Power BI for cleaning, analysis and visualization. The data contains a sheet/table called Data Association with 12,500 rows and 14 columns.

### Tools

- Excel - Data Cleaning
- Power bi - Data Analysis And Visualization

 ### Data Cleaning/Preparation

I cleaned the data efficiently and did some transformations with the Power Query Editor of Power BI.
Some of the applied steps included:

-	Created new column for date from the payment date wich came with time and named: [Date] Datatype then changed from 'TEXT' TO 'DATE'.

-	I created a Date table to allow me to slice and dice the data by date attributes such as weekday, month, and quarter if needed. Power BI automatically created a one-to-many relationship between the [Date] and [Data Association] tables resulting in a star schema model.

  ### Exploratory Data Analysis

  EDA involves exploring the tutors data to answer key questions, such as :

  -  The Total Request for the Month
  -  The Total Classes Held in the Month
  -  The Total Classes Terminated in the Month
  -  The Completion Rate for the Month
  -  The Number of Total Request by Level
  -  The Number of Total Request by Language
  -  The Total Request by Status
  -  The Student Feedback Percentage ratio

### Data Analysis

I added some measures to help in my Analysis

#### Measures that was added are shown below

- Total Classes = COUNT('Data Association'[Request Number])
- Total Classes Held = COUNTROWS('Data Association') - COUNTROWS(FILTER('Data Association'[Status] <> "Classes"))
- Classes Terminated =  COUNTROWS('Data Association') - COUNTROWS(FILTER('Data Association'[Status] <> "Terminated"))

  ### Results/Findings
 From the dashboard, it is observed that;
 
- Total Request made for May 2022 = 12500
- Total Number of request made from 1st May to 31st of May = 12500
- Total Classes Held = 8403
- Total Classes Terminated = 4097
- Completion Rate = 67%

### Recommendations

To improve the completion rate, focus on better tutor-student matching, enhance tutor training and incentives, boost student engagement with personalized support, leverage data insights for strategic adjustments, and offer rewards to encourage both tutor and student retention.

### Limitations

Limitations include data quality issues, scheduling constraints, external student factors, scalability of personalized support, reliance on honest feedback, and potential training costs.

### References

For an in-depth understanding of data-driven improvements and limitations in educational or tutoring analysis, here are some general references:

Student Motivation in Learning Retention:

Schunk, D. H., & Zimmerman, B. J. (2012). Motivation and Self-Regulated Learning: Theory, Research, and Applications. This book provides insights into the complexities of student motivation and retention in educational settings.






    


 

   
