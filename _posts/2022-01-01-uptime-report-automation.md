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
The goal of this project was to automate the data aggregation, presentation, and sending of a monthly report detailing front-end availability for the prior month.

Initially, the data sources for the three front ends lived in separate places, and compiling the required metrics often required the input of Subject Matter Experts, leading to lengthy processes and increasing the effort needed to deliver the report.

Through this project, I was able to reduce the report creation process from 3-4 days and involving meetings with four different senior engineers (30 minutes to 2 hours) a month, to only ~2-3 hours impacting my day.

| Role              | Old Cost     | New Cost    |  Reduction          | 
| ----------------- | ------------ | ----------- | ------------------- | 
| Product Owner     | $1,907.84    | $178        | 90.67% (-$1,729.84) | 
| Senior Engineer   | $641.52      | $0          | 100% (-$641.52)     | 
| **Monthly Total** | $2,849.36    | $178        | 93.75% (-$2,671.36) | 
| **Yearly Total**  | $34,192.32   | $2,136      | 93.75% (-$32,056.32)| 

*please note the above salaries were calculated using company averages per Glassdoor*
  [$124,000 PerYear](https://www.glassdoor.com/Salary/Rocket-Companies-Product-Owner-Salaries-E7856_D_KO17,30.htm) = $59.62 an Hour   
  [$166,800 PerYear](https://www.glassdoor.com/Salary/Rocket-Companies-Senior-Software-Engineer-Salaries-E7856_D_KO17,41.htm) = $80.19 an Hour

### Project Timeline
45 Days from start to sending out the first report using the new automated process

### Project Description
Using Python, I gathered data from PagerDuty, Grafana, and Dynatrace's APIs to automate the collection and presentation of technical incidents that affected specific Business Services in Pagerduty. To track individual user impact, I connected to different Grafana dashboards and Dynatrace data sources to track the 500 responses.

After collecting the data, I performed a simple calculation to reduce the total uptime for the three target front ends based on the time an incident spent in a Severity 1 or 2 state, while highlighting the number of 500 responses outside of recorded incident time frames.

The Python script then automatically created a .docx file containing a bar chart visualizing the downtime and a section for each front end that detailed the incidents that impacted said front end.

I verified the data, constructed an email communication that highlighted the important details, and sent the file as a PDF to leaders across the organization.

#### Skills and Technologies
- Python
- Data Visualization
- Enterprise-Wide Communications 