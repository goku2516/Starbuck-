# Starbuck-


# Introducing a Dataset
This data set contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). Some users might not receive any offer during certain weeks.

Not all users receive the same offer, and that is the challenge to solve with this data set.

# Project Motivation
I chose this project to understand the success rate of offers being sent and analysis is done through addressing the following questions.

How many customers were provided with a specific offer?
What's the performance level of an offer?
Data Preparation
There are three datasets provided and each dataset is cleaned and preprocessed for further analysis. The target features for analysis are offer_success, percent_success.

Portfolio - renaming id column name to offer_id, one-hot encoding of channels and offer_type columns
Profile - profile: renaming id column name to customer_id, replacing age value 118 to nan, creating readable date format in became_member_on column, dropping rows with no gender, income, age data, converting gender values to numeric 0s and 1s, adding start year and start month columns (for further analysis)
Transcript - renaming person column name to customer_id, creating separate columns for amount and offer_id from value col, dropping transaction rows whose customer_id is not in profile:customer_id, converting time in hours to time in days, segregating offer and transaction data, finally dropping duplicates if any

# File Descriptions
master_offer_analysis.csv file contains the details about the offer ids and meta data about each other (duration, type), demographic data for each customer and 
records for transactions, offers received, offers viewed, and offers completed
