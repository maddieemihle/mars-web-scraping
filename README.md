# Mars Web-Scraping Challenge
## Background 
In this challenge, a full web-scraping extraction and analysis of cleaning and visualizing data regarding weather on Mars in multiple news articles was performed. The assignment consisted of two technical products: deliverable one and deliverable two. Various skills, including collecting data, organizing, storing data, analyzing data, and visually communicating insights, were used during this challenge. More specific techniques include identifying HTML elements on a page, identifying their ID and class attributes, using the knowledge to extract information via automated browsing with Splinter, and HTML parsing with Beautiful Soup. 

## Challenge 
### Part 1: Scrape Titles and Preview Text from Mars News 
#### Step 1: Visit The Website 
Using the starter code, a Jupyter Notebook was created, and dependents were imported. The website provided was set up and inspected to establish what elements to scrape. 

#### Step 2: Scraping 
Next, using Beautiful Soup object, the textual elements were extracted from the website. 

#### Step 3: Storing Results 
Lastly, extracting the titles and preview text of the news articles was taken of what was scraped. The results were then stored in Python data structures using dictionaries and keys. After, the data was exported to a JSON file and saved. The browser was closed. 

### Part 2: Scrape and Analyze Mars Weather Data
#### Step 1: Visit The Website
Using the automated browser, the webpage to [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html) was utilized to inspect and identify which elements to scrape. This was mostly done with Chrome DevTools to discover whether the table contained usable classes.

#### Step 2: Scraping 
A Beautiful Soup object was created and used to scrape the data in the HTML table. 

#### Step 3: Storing Data 
All of the scraped data was assembled into Pandas DataFrames. The columns were utilized using the same headings as the table on he website. For reference, they are listed below: 
* 'id': the identification number of a single transmission from the Curiosity rover
* 'terrestrial_date': the date on Earth
* 'sol': the number of elapsed sols (Martian days) since Curiosity landed on Mars
* 'ls': the solar longitude
* 'month': the Martian month
* 'min_temp': the minimum temperature, in Celsius, of a single Martian day (sol)
* 'pressure': The atmospheric pressure at Curiosity's location

#### Step 4: Preparing Data for Analysis
The data types associated with each column were examined using _dtypes_. They were converted to the appropriate data types using Pandas. 

#### Step 5: Analyzing the Data
After all the steps were taken, a series of five questions were asked and answered using analysis skills learned. The questions are listed below for reference: 
1. How many months exist on Mars?
2. How many Martian (and not Earth) days’ worth of data exist in the scraped dataset?
3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    * Find the average the minimum daily temperature for all of the months.
    * Plot the results as a bar chart.
4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    * Find the average daily atmospheric pressure of all the months.
    * Plot the results as a bar chart.
5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    * Consider how many days elapse on Earth when Mars circles the Sun once.
    * Visually estimate the result by plotting the daily minimum temperature.

This was all done via various calculations and analytical observations. 

#### Step 6: Saving the Data
The DataFrame was exported to a CSV file. 

## Results: 
In Part 2: Scrape and Analyze Mars Weather Data, questions were asked within the analysis section. The results are listed as follows: 
1. How many months exist on Mars? 
    * There are 12 months on Mars. 
2. How many Martian (and not Earth) days’ worth of data exist in the scraped dataset?
    * There are 1867 sols worth of data. 
3. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    * Based on the data in the previous graph of temperature analysis, it was found that the coldest month on Mars is Month 6 at a temperature of -83.3 °C. The hottest month is Month 8, with a temperature of -68.9 °C.
4. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    * Based on the data given, the lowest pressure month is Month 6 at 745.05, and the highest pressure month is Month 9 at 913.30.
5. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    * Based on the data, we can use the graph above to estimate the number of terrestrial days by observing the peak-to-peak and trough-to-trough. This can help understand in correlation to the number of Earth days since the number of cycles are related to the number of sols in a Martian year, representing the time it takes for Mars to complete one full orbit around the sun. The distance between the peaks and troughs is approximately 670 sols. This was found by calculating the peak-to-peak: 
        * 800 - 150 = 650 
        * 1500 - 800 = 700 

    * And calculating the trough-to-trough: 
        * 1200 - 525 = 675

    The average of all of these values is roughly around 675 days (Source: [NASA](https://science.nasa.gov/mars/facts/)). This number is very close to the actual number of earth days (687). Therefore, there are approximately 670 sols in a Martian year.

## Methods Used
* Python 
* Pandas 
* Jupyter
* Matplotlib 
* JSON  
* HTML parsing
* Web-scraping
* Beautiful Soup
* Splinter
* CSV conversion 

## Software Used 
Coding was performed via VSCode using Jupyter notebooks.

## References
Data for this dataset was given by _edX Boot Camp LLC_ (2025), and is intended for educational purposes only. The Mars News website is operated by _edX Boot Camps LLC_ for educational purposes only. The news article titles, summaries, dates, and images were scraped from NASA's Mars News website in November 2022. Images are used according to the JPL Image Use Policy (courtesy NASA/JPL-Caltech).