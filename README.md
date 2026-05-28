# P3: Interactive Data Dashboard
## Overview
Project 3 (P3: Interactive Data Dashboard) offers a fully-interactive executive dashboard for the author's fictional B2B firm, "Grandiloquence," which provides "convoluted" tech services to companies in need. Grandiloquence's data was synthetically generated using Python's faker, random, and datetime (timedelta) libraries to simulate CRM behavior and intends to reflect realistic customer lifecycles, churn behavior, and usage measurements. Grandiloquence's dashboard, the focal point of Project 3, was developed in Microsoft Power BI and is directly connected to a PostgreSQL server hosting/storing the synthetically-crafted datatable. However, the datatable (as a CSV), example outputs, and a video walkthrough are all available for viewing in this repository. 

## The Why/For What
The creation of Grandiloquence's data dash aims to:
- Reflect the author's growing nag for data analysis/science
- Highlight the author's understanding of KPIs, customer lifecycles, and customer behaviors
- Put on display the author's intelligent (and slightly artsy) dashboard design

Moreover, Grandiloquence's dashboard intends to answer various questions internal/external stakeholders might have about the condition of the firm and its many clients, such as:
- How does usage vary from industry-to-industry and plan-to-plan?
- What demographics do the healthiest customers belong to?
- What companies/industries/plans create the most value?
- What companies/industries/plans cause the most burden on the support team?
- How does the company's success vary from region-to-region?
- How frequent is it that a company turns over (churn metrics)?

All of these questions can be efficiently answered via efficient navigation of Grandiloquence's new dashboard.

## Tech Stack
### Python - solely for data generation
- Pandas
- Numpy
- Faker
- Random
- Datetime
### Microsoft PowerBI
### GitHub 

## `10-grandiloquence.csv` Datatable Features
The synthetically-generated `10-grandiloquence.csv` datatable offers 12 columns:
- `customer` - the client's customer id no.
- `company_name` - the customer's actual firm name
- `industry` - the industry the customer belongs to (i.e. Finance, Logistics)
- `region` - the region from which the customer operates (i.e. Asia-Pacific, Europe)
- `signup_date` - the date which the customer shook hands with Grandiloquence
- `plan_type` - either "Free," "Basic," "Pro," or "Enterprise."
- `monthly_usage` - instances in which a company used Grandiloquence's convoluted service/site
- `support_tickets` - how many times a company has called in requesting assistance with their provided service
- `last_active_date` - last time which a customer used Grandiloquence's provided service/site
- `churn_flag` - whether or not the client has turned over (boolean)
- `lifetime_value` - total value a client has created for Grandiloquence from purchase of service(s)
- `nps_score` - net promoter score that measures how likely a company is to recommend Grandiloquence

#### If...
...you'd like to view the Grandiloquence datatable, feel free to do so & download from `10-grandiloquence.csv`. Moving forward, however, these are the features that will be pulled into Microsoft PowerBI (via a live PostgreSQL connection) for visualizing.

## Grandiloquence Dashboard Features
This dashboard features many useful metrics, calculated fields, and measures imperative to the storytelling of Grandiloquence's current state. The primary measure is that of `Customer Health Score`, which is merely a summation of four other weighted scores: `NPS Score`, `Usage Score`, `Churn Score`, and `Support Burden Score`. These measures are all based on percentiles; thus a customer with the BEST NPS score would receive the highest score in that category, whereas the customer with the highest usage score will receive the highest score in that category, so on and so forth. Customers with a `Customer Health Score` < 20 are labeled as "At-Risk" regarding their "health status." The status for customers with a score >20 & <40 is considered "Moderate." Customers with a score >40 are considered "Safe." Though, the dashboard dives deeper than health statuses and measures.

The Grandiloquence dashboard is segmented into 3 pages:
- Executive Overview
- Segments & Risks
- Company Drill-Down

### Executive Overview
The executive overview shows off a few different heavy-hitting metrics/KPIs:
- Overall/segment health score
- Overall/segment NPS and usage scores
- Overall/segment total lifetime value
- Overall/segment total support tickets
- `industry` vs. usage
- `plan_type` vs. usage

#### The executive overview tab (still-shot):

<img width="2506" height="1467" alt="Screenshot 2026-05-27 235730" src="https://github.com/user-attachments/assets/25f0f1ee-2ca7-440f-9eb6-a98aca61628f" />

### Segments & Risks
As it's name suggests, this section takes a deep-dive into particular segments and potentially associated risks, offering a few unique features:
- An industry/plan/health heat map that acts as a slicer for other features
- A `region` card that allows for region-based filtering
- Segment health score card
- Positive (optimistic) segment cards for:
  - Average value created by company
  - Usage percentage for companies
  - Total customer count
- Negative (pessimistic) segment cards for:
  - Churn rate
  - Average support tickets put in per company
  - Total count of "At-Risk" customers

#### The segments & risks tab (still-shot):

<img width="2498" height="1480" alt="Screenshot 2026-05-27 235741" src="https://github.com/user-attachments/assets/464b8ca1-0a89-412e-82fb-62c3ad59670c" />

### Company Drill-Down
The company drill-down section provides customer-specific details. Its key features include:
- A customer profile card that displays the client's industry and plan and whether the customer is active and healthy
- A customer "health status" card (whose values were explained earlier)
- A "value-created" card displaying how much the customer is worth
- A health breakdown card specific to the customer.

#### The company drill-down tab (still-shot), with 'Abott and Sons' selected:

<img width="2503" height="1482" alt="Screenshot 2026-05-27 235755" src="https://github.com/user-attachments/assets/7b55f42e-7de1-4c1f-afe4-0fc4cea97ddc" />

### Secondary Features
Less notable features include:
- Tooltips
- Hover-for-help buttons
- Hover-for-info buttons
- Back and forth arrows for ease-of-navigation
- Color-coding for contrast and ease-of-viewing
- Glow effects to lift each card and separate one from another
- Labels where needbe

## Repository Structure

### interactive_data_dashboard
10-grandiloquence.csv

20-dashboard_still_shots/

30-grandiloquence_dashboard.mp4

README.md

## Purely Optional: How to View Project (In Author's Intended Manner)
- Give `10-grandiloquence.csv` a quick scan to get a fair gauge of the quality/shape of the data used
- Ask the data whatever questions come to mind
- Peak at the still shots in `README.md` or `20-dashboard_still_shots/` as a reference to how the dash appears unfiltered/unsliced
- View `30-grandiloquence_dashboard.mp4` for a brief overview of how the slicing works, how to navigate the dash, etc. (stay for as long or as little as preferred)
- Assess whether the dash can answer key questions

## Future Improvements
- Increase depth, messiness, and variability of data
- Include a time-based variable on date-joined or sign-up date (perhaps "lifespan" of business variable)
- Expand dashboard into other realms of business intelligence beyond CRM and customer behavior

## The Author

### Edward Noonan
Data Analyst/Aspiring Data-Scientist with grounding experience in SQL, Python, R/RStudio, BI tools (PowerBI & Tableau), and overall analytics workflows.

This project was developed as part of a post-graduation portfolio to demonstrate real-world data analysis (and engineering) capabilities.

