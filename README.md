# Forbes Top 100 Employers 2022 (in progress)
## Overview
This repository contains an exploratory analysis of the [Forbes 2022 list](https://www.kaggle.com/datasets/devrimtuner/worlds-best-employers-top-100) of the worlds best employers. 

It was initially submitted as a group project that required us to conduct an EDA of any public dataset to answer research questions of our choosing. I have extracted the bits of the project I worked on and am building it out to answer some further questions explained below. My intention is to combine each separate notebook in this repository into one summative analysis.

The original rankings were compiled by Forbes, and informed by Statista, who compiled qualitative responses from employees of multinational companies on employer tenets such as: social impact, talent retention, corporate responsibility, gender equality.

The initial research questions were:
1. What are the attributes of the world's best employers?
2. Do good employers make good investments?

### Part one 
Currently contained in the 'Forbes_EDA' notebook. Performs some basic cleaning and manipulation of the original csv file. Also merges it with Glassdoor Rating data and tests for correlation between 'Forbes Ranking' and 'Glassdoor employee rating.'

![rankings_count_by_size](images/download.png)

![Glassdoor vs Forbes ranking](images/GDscatter.png) 

*There is no correlation between Employee Glassdoor Rating (x) and the Forbes model (y). Most companies cluster in the high 3s, low 4s, regardless of ranking.*

### Part two
The notebook file 'FinanciaL_data_section_2' retrieves financial information on all public companies in the rankings using the yFinance wrapper library, which makes an unofficial API call to the yahoo finance server. A range of financial metrics are plotted against the ranking and glassdoor data for each company.

![company_loop](images/companyloop.png)
*Here, a 'for' loop iterates through the dataframe and returns the relevant financial information that is printed to the screen.*

![financial_analyses](images/finmetrics.png)

### Part three
Part three will explore whether external factors (such as unionisation rates, average wage, liveability) affect ranking, when looked at from HQ country. Some initial exploration of these factors is in the 'Country_data..' notebook.
