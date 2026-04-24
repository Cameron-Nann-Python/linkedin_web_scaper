# 🔄 LinkedIn Webscaper

## 📓 Project Overview

Searching through jobs and trying to find the right match can be tiresome. By automating aspects of navigating the job board, an applicant can have a more streamlined job search. 

This web scraper examines a LinkedIn page and extracts the following job information:
- job titles
- company names
- company LinkedIn pages
- job locations
- date when job was posted
- employment types (i.e. full-time, part-time)
- employment levels (i.e. entry-level, senior-level)
- salaries

The final result is a .csv file that can be readily used for data exploration to find trends or commonalities between job listings.

## 📄 Web Scraper Setup

### 📄 Generating URLs

- The `get_job` function takes in the job position and location and generates a LinkedIn url

### 🕸️ Scraping the Data

- A BeautifulSoup object holds the html content after a successful page response
- Card information and individual job descriptions are scraped for their content

### 🗄️ Generating the DataFrame

- The scraped job content is stored in lists that form the columns of a Pandas DataFrame

### 🧹 Cleaning the Data

- Salary information is normalized using the `re` library and string patterns
- Employment level is populated with null values for missing data

### 📁 Producing the CSV

- The final Pandas DataFrame is saved to a .csv file

## 💡 Technologies Used
- Python3.13
- BeautifulSoup: store html content
- requests: get webpage response
- re: find string patterns for new string generation
- urllib.parse: handle ASCII hex codes 
- pandas: structure data format
- ipkernel: Visual Studio Code extension for running Jupyter notebooks

## How to Run
1. Create virtual environment with Python3.13 (Anaconda Navigator is necessary for Visual Studio Code).
2. Install the dependencies above (2026 versions do not have dependency conflicts) into the virtual environment.
3. Open the lab notebook in an IDE that supports Jupyter (Visual Studio Code was used for the development of this scraper).
4. Connect the virtual environment as the kernel.
5. Use the "Run ALL" command to generate the csv.

## 🗨️ Considerations
There is no field for skills due to the variance in how employers define them. A more refined scraper could include more fields that could match with keywords on an applicants resume, similar to ATS software.

## 📂 Files Included
- `linkedin_webscraper.ipynb`: Jupyter notebook with full scraper logic
- `da_jobs.csv`: .csv file output after using the scraper
