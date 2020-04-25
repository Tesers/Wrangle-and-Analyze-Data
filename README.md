# Wrangle and Analyze Data

## Introduction

In this project, we wrangled the tweet archive data of Twitter user @dog_rates, also known as WeRateDogs. The main purpose of the data wrangling project is gathering data from different resources, assessing the data to find some problems and cleaning what we found already in the assessment part.

### 1. Gathering Data

The gathering process includes three parts for this project.

**a) The WeRateDogs Twitter archive file:** twitter_archive_enhanced.csv
    
**b) The tweeted image prediction file:** This file will be downloaded using the Requests library and the following URL:  https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv
    
**c) Twitter API and JSON file:** Each tweet's retweet count and favorite ("like") count at minimum, and any additional data you find interesting. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called tweet_json.txt file. Each tweet's JSON data should be written to its own line. Then read this .txt file line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count.
    
### 2. Assessing Data
After gathering data from different sources, I assessed them visually and programmatically for quality and tidiness issues.

**1) Visual Assessment:**

I used Jupyter Notebook and Google Sheets to see all data. 

**2) Programmatically Assessment:**

I used some functions from the Pandas library.
  - info,
  - value_counts,
  - describe,
  - sample,
  - duplicated, etc.
  
Using visual and programmatic assessment, I found out some quality and tidiness issues in my dataset and took some notes to keep them for the cleaning part. These notes are in the wrangle_act.ipynb.

### 3. Cleaning Data

This part includes three different parts for each quality and tidiness issues: **Define**, **Code** and **Test**. Before the cleaning process, the copies of all three data frames were created. Afterward, the steps of cleaning parts were applied iteratively for all quality and tidiness issues.

### 4. Storing, Analyzing, and Visualizing Data

- Save master dataset to 'twitter_archive_master.csv' file.
- The master dataset is analyzed using pandas in the Jupyter Notebook and at least three (3) separate insights are produced.
- Four different visualizations are produced in the Jupyter Notebook using Python’s plotting libraries.

### 4. Reporting

Two different report are created for this part.
- Wrangling efforts are briefly described in wrangle_report.pdf.
- The three (3) or more insights the student found are communicated in act_report.pdf including visualization.

## Used Technology Stack

You will need to install:
- Python 3.6
- Jupyter (notebook or lab)
- Pandas
- Numpy
- Matplotlib
- Seaborn
- requests
- json
- tweepy
- os.path
- timeit

## Summary of Findings

- Cooper, Tucker, Oliver, Charlie, and Lucy are the top 5 preferable names for dogs.
- The most popular dog type is a Golden Retriever and the following types are Labrador retriever, Pembroke, Chihuahua and Pug.
- In this dataset, there are some columns have a strong correlation to each other such as; retweet count and favorite count. This means they have a relationship in the same direction. When favorite_count variable decreases as the retweet_count variable decreases, or favorite_count variable increases while the retweet_count increases.
- Retweet count and rates have a positive correlation, but there is not a clear/strong relationship between each other.

