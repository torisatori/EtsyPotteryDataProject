
# Title Of Your Project
Analysis of Handmade Pottery Listings on Etsy

# Introduction & Goals
- Introduce your project to the reader
- Orient this section on the Table of contents
- Write this like an executive summary
  - With what data are you working
  - What tools are you using
  - What are you doing with these tools
  - Once you are finished add the conclusion here as well
  
 Goal: Build an end-to-end pipeline in AWS using data accessed from Etsy’s open API. 
 Include a data model that returns meaningful business insight at the end of the pipeline.  
Analyzing most popular categories of pottery listings on Etsy using a clustering model.  
End result would be a visualization that could be used for production choices for a small business that wants to optimize their sales on Etsy. 

# Contents

- [The Data Set](#the-data-set)
- [Used Tools](#used-tools)
  - [Connect](#connect)
  - [Buffer](#buffer)
  - [Processing](#processing)
  - [Storage](#storage)
  - [Visualization](#visualization)
- [Pipelines](#pipelines)
  - [Stream Processing](#stream-processing)
    - [Storing Data Stream](#storing-data-stream)
    - [Processing Data Stream](#processing-data-stream)
  - [Batch Processing](#batch-processing)
  - [Visualizations](#visualizations)
- [Demo](#demo)
- [Conclusion](#conclusion)
- [Follow Me On](#follow-me-on)
- [Appendix](#appendix)


# The Data Set
- Explain the data set
- Why did you choose it?
- What do you like about it?
- What is problematic?
- What do you want to do with it?

The data used in this project was accessed via the open API (Application Programming Interface) provided by Etsy. 
The purpose of the API is to allow businesses that use Etsy to integrate and automate processes associated with the maintenance of product listings on Etsy.  For this project, the API was used to download recent listings and information about the shops that created those listings. 
The initial set of data was downloaded from the open Etsy API using the “findAllListingsActive” endpoint and includes attributes of recently updated listings such as titles, descriptions, number of favorers, tags, price, creation date and the shop ID of the shop that created the listing. This endpoint returns all active listings in reverse chronological order by their creation date and has a maximum value of 12,000 records that can be retrieved due to the limitation placed on the offset value.  
The offset value indicates to the API how far back in the records to retrieve when requesting information about listings that had been recently uploaded to the platform.  For instance, an offset equal to 10 would begin the search at the 10th most recent listings.  The maximum value allowed for the offset was 12,000 which means the initial dataset was limited to the most recent 12,000 records.  The first set of data was downloaded on February 25, 2022. Two additional sets of 12,000 listings were downloaded on March 31 and April 10, 2022.  
Keywords were added to the search parameters sent to the API to narrow down the request to listings that contained products of interest rather than all products on Etsy.  Determining the correct keywords was a manual process that required a review of the types of listings each set of keywords would return.  For instance, using the keyword “pottery” would return results involving polymer clays that are not of interest to a business making ceramic using a different process and different materials than those used for synthetic clays. Replacing “pottery” with a more specific term like “stoneware” returned listings that were made of natural clays and fired to a high temperature in a kiln. The keyword “handmade” was added to reduce the amount of vintage and machine-produced products that were returned.  The two keywords “stoneware” and “handmade” used together returned a set of results that would be of interest to a small pottery business.


# Used Tools
- Explain which tools do you use and why
- How do they work (don't go too deep into details, but add links)
- Why did you choose them
- How did you set them up

## Connect
## Buffer
## Processing
## Storage
## Visualization

# Pipelines
- Explain the pipelines for processing that you are building
- Go through your development and add your source code

## Stream Processing
### Storing Data Stream
### Processing Data Stream
## Batch Processing
## Visualizations

# Demo
- You could add a demo video here
- Or link to your presentation video of the project

# Conclusion
Write a comprehensive conclusion.
- How did this project turn out
- What major things have you learned
- What were the biggest challenges

# Follow Me On
Add the link to your LinkedIn Profile

# Appendix

[Markdown Cheat Sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
