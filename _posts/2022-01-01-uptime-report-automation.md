---
title: "Uptime Report Automation"
last_modified_at: 2022-1-1T16:22:02-05:00
categories:
  - Projects
tags:
  - Business Analyst
  - Automation
  - Software Development
  - Site Reliability Engineering
  - Internal Project
---
# Uptime Report Automation
### Project Summary
The goal of this project was to automate the data aggregation, presentation and sending of a monthly report detailing front end availability for the prior month. 

When the assignment was originally handed off, the data sources for the three front ends lived in separate places and often relied on Subject Matter Experts to compile and report the required metrics. This process was lengthy and typically required meetings increasing the effort needed to deliver the report. 

All said and done, the report creation processes was reduced from 3-4 days, involving meetings with four different senior engineers (~30 minutes to 2 hours) a month; to ~2-3 hours only impacting my day.  

| Role            | Old Cost     | New Cost    |  Reduction          | 
| --------------- | ------------ | ----------- | ------------------- | 
| Product Owner   | $1,907.84    | $178        | 90.67% (-$1,729.84) | 
| Senior Engineer | $641.52      | $0          | 100% (-641.52)      | 
| **Monthly Total**   | $2,849.36    | $178        | 93.75% (-$2,671.36) | 
| **Yearly Total**   | $34,192.32   | $2,136      | 93.75% (-$32,056.32)| 

*please note the above salary's were calculated using company averages per Glassdoor*
  [$124,000 PerYear](https://www.glassdoor.com/Salary/Rocket-Companies-Product-Owner-Salaries-E7856_D_KO17,30.htm) = $59.62 an Hour   
  [$166,800 PerYear](https://www.glassdoor.com/Salary/Rocket-Companies-Senior-Software-Engineer-Salaries-E7856_D_KO17,41.htm) = $80.19 an Hour
  

### Project Timeline
45 Days from start to sending out the first report using the new automated process

### Project Description
Utilizing Python to gather data from PagerDuty, Grafana and Dynatrace's API's. I was able to automate the collection and presentation of the Technical Incidents that effected specific Business Services in Pagerduty. To track individual user impact, I connected to different Grafana dashboards and Dynatrace data sources to track the 500 responses.

Once the data was collected, I performed a simple calculation reducing the total uptime for the three target front ends based on the time an Incident spent in a Severity 1 or 2 state, while highlighting the number of 500 responses outside of recorded incident time frames.

From here, the python script automatically created a .docx file containing a bar chart visualizing the downtime, and a section for each front end that detailed the incidents that impacted said front end. 

From here I verified the data, constructed an email communication that highlighted the important details. then sent the file as a PDF to leaders across the Organization


#### Skills and technology's
- Python
- Data Visualization
- Enterprise Wide Communications 