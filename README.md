# nyt-nlp
Resources for NLP / NYT Headlines 

File Directory:
There are 12 NYT API Data Collection files collecting monthly data for each month from 1981-2021.
Each of these files generates a csv for that month's data for 41 years (not included in repository).
01 Master files calls on these 12 files, prepares / cleans / tokenizes the data, followed by sentiment assignment and analysis.
02 file serves as a deep-dive into one category (World in this case), exploring insights there.


Additional notes:

Files & Roles

UNDERLYING FILES (outputs of individual month's notebooks)
/constitutes the data collection from the New York Times API

	- NYT API Data Collection - January.ipynb —> creates January 1981-2022.csv
	- NYT API Data Collection - February.ipynb —> creates February 1981-2022.csv
	- NYT API Data Collection - March.ipynb —> creates March 1981-2022.csv
	- NYT API Data Collection - April.ipynb —> creates April 1981-2022.csv
	- NYT API Data Collection - May.ipynb —> creates May 1981-2022.csv
	- NYT API Data Collection - June.ipynb —> creates June 1981-2022.csv
	- NYT API Data Collection - July.ipynb —> creates July 1981-2022.csv
	- NYT API Data Collection - August.ipynb —> creates August1981-2022.csv
	- NYT API Data Collection - September.ipynb —> creates September 1981-2022.csv
	- NYT API Data Collection - October.ipynb —> creates October 1981-2022.csv
	- NYT API Data Collection - November.ipynb —> creates November 1981-2022.csv
	- NYT API Data Collection - December.ipynb —> creates December1981-2022.csv


01 MASTER FILE 
/constitutes data prep, analysis, and visualization:

	- Preparing Data Language Set & Analysis notebook
		- Section 1: Importing necessary tools
		- Section 2: Collecting raw data file from individual API exports
	`	- Section 3: Cleaning data
    			* Altering necessary feature dtypes & names
			* De-duplicating headlines 
    			* Removing nulls
			* Removing unnecessary features
    			* Removing erroneous headlines based on abnormal word counts (EDA)
			* Identifying & filtering to top news sections (EDA)
			* Adding custom date features for analysis
		- Section 4: Applying vaderSentiment & polarity scores   
		- Section 5: EDA
   			* High-level plots / trends
    			* Exploring score ‘migrations’ over time
		- Section 6: Analysis I (News Section Hypothesis Testing)
    			* Visualizing trends across news sections
    			* Linear Regressions across news sections
		- Section 7: Analysis II (Single Section Deep Dive & Vectorization)
			* Overall `scorecard` / high-level views
			* Vectorizing / tokenizing news section data subsets
			* Identifying top / bottom tokens
