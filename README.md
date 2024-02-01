# Take-home Exercise - BI Analyst 

## Summary
At Accredible, you will be responsible for data models that cover use cases spanning across multiple teams, from go-to-market, to product, to finance. In this take-home exercise, we wanted to give you a small taste of what a day in the life of a BI Analyst at Accredible looks like whilst getting to know your skills and ways of working better. 

None of your work will be used by Accredible, the goal of this exercise is to showcase the way that you approach your work, and to build your understanding of our expectations in the role.

For this take home exercise, you will be working on a critical problem for our go-to-market team - the Sales Funnel. This data model should enable our key business stakeholders to understand how many deals have progressed through each stage of the sales cycle. In our case, we’ll be focusing on a single pipeline which consists of six distinct stages:
1. Discovery
2. Qualified
3. Proof of Value
4. Proposal/Pricing
5. Procurement/Negotiation
6. Closed Won / Closed Lost

A single deal should move through these stages in a chronological order, but it can go from any stage to Closed Lost. 

## Data

In this repository, you will find an excerpt of example data from our CRM. This data includes the following tables:

**deal_pipeline_stages:**
- **deal_id** - a unique identifier assigned to each deal in a pipeline 
- **stage_created_at** - the timestamp at which a deal_id entered that particular stage
- **pipeline_id** - the identifier of the pipeline (in this dataset, you will only see default as a value)
- **pipeline_name** - a string representing the human-readable pipeline name (in this dataset, you will only see Mid Market Pipeline as a value)
- **deal_stage_id** - the identifier of the stage a deal has entered
- **stage_name** - a string representing the human-readable stage name
- **stage_display_order** - an integer representing the order of each stage in the pipeline (in this dataset, the values cover a range from 5-10) 

This table is unique on the **deal_id** and **stage_created_at** columns.

**deals:**
- **deal_id** - a unique identifier assigned to each deal in a pipeline 
- **pipeline_id** - the identifier of the pipeline (in this dataset, you will only see default as a value)
- **pipeline_name** - a string representing the human-readable pipeline name (in this dataset, you will only see Mid Market Pipeline as a value)
- **stage_name** - a string representing the human-readable stage name
- **amount_in_home_currency** - a number representing the monetary value of a deal in USD ($).
- **created_at** - a timestamp at which a deal was first created
- **close_date** - a timestamp at which a deal has been closed
- **deal_source_type** - a string representing the channel from which a deal was sourced (eg. Website, Sales Outbound, Webinar, Tradeshows and Events)

This table is unique on the **deal_id** column.

## Expected Output
For this exercise, we would like you to build us a funnel visualization which represents the:
- Count of deals that have entered into each stage of the pipeline
- Monetary value of deals that have entered each stage of the pipeline in USD ($)

We should be able to filter / slice this funnel by close date and deal source type. 

Feel free to display this data in any visualization format you’d like - this is an opportunity for us to understand what your best practices are for displaying quantitative data.

We have no strict requirements on what tools you use to achieve this output, other than the fact that the data modeling should be done in SQL and the results presented in a Business Intelligence tool of your choice. 

Below is a list of free SQL and BI tools which you may find useful to complete this exercise (these are just suggestions, we don’t mind what tools you use):
- [Preset](https://preset.io/) (BI)
- [Tableau Public](https://public.tableau.com/app/discover) (BI)
- [Looker Studio](https://cloud.google.com/looker-studio?hl=en) (BI)
- [PostgreSQL](https://www.postgresql.org/) (SQL database)
- [Clickhouse](https://clickhouse.com/) (SQL database)
- [DuckDB](https://duckdb.org/) (SQL database)

We’d like you to submit this exercise before the final interview (at least 2 working days) to allow for our team to review and formulate their questions. During the panel interview, we’d like you to walk through your work with our team. We’ll be asking questions to understand:
- The assumptions you have made of the source data
- The SQL query/s you have written 
- The presentation of the data to a non-technical audience

Our expectation is that this exercise should take approximately 2 hours to complete thoroughly. Most importantly, we’d like to understand how you would tackle the data problem and present the results to a key business stakeholder. Thus, the final model and visualizations do not have to be perfect. Finally, have fun and we look forward to talking through your solutions! 
 
