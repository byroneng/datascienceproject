# Crawling the Job Market
Authors: Sameer NANDIKAR (u1010576), Byron ENG (u0824780)<br>
CS 5963 / MATH 3900 <br>
email id: sameer.nandikar@gmail.com 
          ; byron.eng@gmail.com

## Background and Motivation
We the authors of this project will be graduating in near future. Thus we need to look for jobs in our respective fields (which in our case is Mechanical Engineering and Atmospheric Sciences) or continue academics in a well-informed direction for better job opportunities. In either case a comperhensive analysis of the job market depicting trends and classifications can be really benificial. 

Motivation for this project comes from some obstacles encounterd in the job search, some of which we have tried to elaborate here. Though there are many job search websites which provide a plethora of information about jobs available, one can not draw useful conclusions about the job market such as density of reasearch and development jobs for a mechanical engineer in medical device sector in state of Utah, without analysis of that information. In addition to that, job openings in most of the industries related to Mechanical Engineering are requirement oriented and have very short lead times for joining thus it would be interesting to see if there are any trends in job openings and use the information to benefit the job seekers to decide when to graduate. These are just few queries among other problems we intend to solve. 

One more aspect of this project includes classification of jobs according to job function and sector, which will help an aspiring Graduate student to make an informed decision to select an area of interest (such as designing, manufacturing, robotics, energy systems).  

## Project Objectives
This project aims to be a tool for anyone entering the job market. The key objective of this project is the analysis of the job market which will include but will not be limited to
- Geospatial density of jobs
- Pay rates vs. experience level
- Pay rates vs. education level
- Classification of jobs on basis of sector (e.g.aerospace, automobile, medical device, energy, mining equipment etc)
- Classification of jobs on basis of job function (e.g. production, quality control, design, research and development etc)
- Annual trend of job openings for different sectors and job functions for different states 

## Data

At this stage we are looking from which websites we can scrap the data and which websites have APIs. Given below is the information of our current options

### Inventory of data sources

|Site|Comments|Allowed (scraping)|Disallowed (scraping)|API|API Reference|
|----|--------|:-----:|:--------:|---|---|
|Glassdoor.com|Has mostly disallows. Because we are going to be using the search, I don't think we are allowed to crawl.||x|Yes|https://www.glassdoor.com/developer/index.htm
|usajobs.com|Disallows scripts||x|Yes|https://developer.usajobs.gov/API-Reference
|dice.com|Disallows jobsearch||x|Yes|http://www.dice.com/common/content/util/apidoc/jobsearch.html
|snagajob.com|Disallows basically everything||x|No|-|
|simplyhired.com|Links to other sites, disallows job details but not job SEARCH||x|No|-|
|careerbuilder.com|Disallows everything unless you're the googlebot||x|Yes|Requested key
|careerinfonet.org|There's a lot that is disallowed, but I don't see anything that is clearly disallowing what we aim to do. Worth another look.||x|No|-|
|indeed.com|Mostly disallows everything ||x|Yes|Requested key|
|monster.com|Mostly disallows evferything||x|Yes|Regestration is required for access which is in progress|
|linkedin.com|Allows scraping with permission||x|Yes|https://api.linkedin.com/v1/people/~?format=json (but an access token is required which is requested)|

## Data Processing 

In addition to APIs, we will keep html scraping as an option. An html of a typical job search website has list of jobs and their links. A dataframe will be created by extracting the information about the jobs from the html page and from nested url links. We will use beautifulsoup and CSS selectors for this purpose. We expect much of the effort to be in data extraction and especially in data clean up because information about the jobs entered may not follow same format most of the times as it is entered by different users. We will be using classification methods to classify the jobs by the desired metrics (ie. degree requirement). Also we need to filter out the features which are out of our present scope of study.

## Exploratory Analysis

At this stage we intend to observe trends of job openings geographically as well as annually. Thus we will use scatter plots and other tools we have learned in this class for visualizations. Heuristic approach also seems appropriate for given purposes. For classification we intend to use SVM, Decision trees and k-NN and based on kind of results we get we will select best suitable method. 

## Analysis Methodlogy

We will first analyze the aggregated data to see geographical and annual trends. Also we will observe the effects of attributes over salary e.g. Pay rates vs. experience level and Pay rates vs. education level. 

Secondly, for classification purposes based on the size of the data we get from one website we will either divide one website's data into training and test data or use data from one website as training and data from another website as test data. We will use classification methods enlisted above and select the best suitable one to visualize the data in scatter plots

## Project Schedule

We have 5 weeks until the presentation date 

Week 1 - Data aquisition and cleaning

Week 2 - Data processing 

Week 3 and 4 - Exploratory analysis

Week 5 - Preperation for the Presentation
