# Crawling the Job Market
Authors: Sameer NANDIKAR, Byron ENG <br>
CS 5963 / MATH 3900 <br>


## Construct some sample data

This could be from as little as one of the web sites. I would like to have some code in place so we can test taking user input and mining the APIs for relevant data.

I received an API key for usajobs.gov but I don't know how to use it.

glassdoor.com would be good to do as one of the last sources. It will be good for pulling data about specific companies.

## ~~Add BLS (Bureau of Labor Statistics) to the table of sources~~

This could be a great source of data

## ~~First steps~~

I think one of our first steps should be to inventory which sites we can actually pull data from. For example, which ones have APIs and which ones can we crawl via search results based on user input (ie. User puts in "Mechanical Engineer", our program would need to crawl search results for "Mechanical Engineer".. I don't see that being possible from all sites.

Note from class: We may need to consider accounting for high demand jobs that will have a flux of offers at the end of semesters. These could be due to students being offered jobs, and companies "going through the motions" of posting the job.

#11.12.2016 Today I have got data from indeed api in xml format and I am looking into element tree libriary for extracting the data from it. 