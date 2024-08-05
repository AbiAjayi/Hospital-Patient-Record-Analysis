# Hospital-Patient-Record-Analysis

### Business Challenge
A healthcare facility has requested an analysis of patient records to gain insights into patient admissions, average stay duration, cost per visit, and insurance coverage for procedures over time.

### Business Goals
To develop a comprehensive visualization dashboard with key performance indicators (KPIs) to improve patient management and financial planning.


![image](https://github.com/user-attachments/assets/eab28972-3ff1-4e45-9a92-de65872016fb)


### Objectives
- To track the number of patients admitted or readmitted over time.
- To determine the average length of hospital stays.
- To analyze the average cost per patient visit.
- To identify the number of procedures covered by insurance.

### Solution Delivered
An end-to-end business intelligence solution was designed and delivered using Power BI.

Step 1: Created a mock-up of questions to be answered on the dashboard
- How many patients have been admitted or readmitted over time?
- What is the average length of hospital stays?
- What is the average cost per patient visit?
- How many procedures are covered by insurance?

### DAX Calculations

- Average Length of stay = DATEDIFF(Start, Stop, Minutes) this DAX formular will extract the time difference from our date/time column
- Average cost per visit = AVERAGE(total claim cost)
- How many procedures are covered by insurance: To calculate this
   - Calculate the number of procedure = DISTINCTCOUNT(code)
   - Calculate the procedure covered by insurance = CALCULATE([No of procedure], payer coverage <> 0)
- Number of patient admitted  = DISTINCTCOUNT(Patient)
- Number of patient readmitted = CALCULATE([no of patient admitted], patient id > 1)

### Business Insights
- Number of Patients Admitted or Readmitted Over Time: The total number of encounters ranged from 1,336 in 2011 to 3,887 in 2014, with 2011 being the lowest and 2014 the highest.
The number of readmitted patients exceeds the number of new patients, with many patients being readmitted multiple times.
Fewer patients came for a single encounter compared to those who were readmitted several times.
- Average Length of Hospital Stays: For patients undergoing procedures, the average stay is approximately 15 minutes.
- Average Cost Per Patient Visit: The average cost per visit is about $279.
- Number of Procedures Covered by Insurance: Out of 157 procedures, approximately 138 are covered by insurance.
- Revenue Generated Over Time: Total revenue from 2016 to 2022 is approximately $102 million.
Revenue was the lowest in 2011 and peaked in 2014.








  
