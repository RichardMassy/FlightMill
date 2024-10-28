# FlightMill
Code to operate and analyse flight mills

A study comparing the flight activity of migratory and non-migratory Episyrphus balteatus in flight mills.

-----------------
Contents:
-----------------

1_Flight_mill_running_code.py
A python script to be run in terminal to record photointerruptor input using a Raspberry Pi.

2.1_Data_extraction.py
A python script to interpret, clean and collate flight mill data into an analysable format.
NOTE: requires specific folder structure to function

2.2_Data_concatenation.R
An R script to collate flight mill data from different experiments into a single file, and combine it with fly information.
NOTE: requires specific folder structure to function

3.1_Mill_Analysis.R
Regression models and graphs of distance, mean speed, flight initiation, flight distance, speed and flight activity.

3.2_Morphometrics.R
Regression of hoverfly size and weight metrics against measured values of weight and wing length & graphing.

Fly information.csv
Information on fly sex, size and weight.

Morphometric information.csv
Data of hoverfly size and weight metrics with measured values of weight and wing length.

RD All flights.csv
Individual flight event data.

RD Flight_stats.csv
Overall flight data.

RD Transects.csv
Flight mill data sampled for 1s every minute.

RD Errors.csv
Errors fixed and unfixed of erroneous direction changes.


------------------------
The data extraction pipeline - dependencies in the order in which data were created and analysed
------------------------

Raw data (inputed manually):
Fly information.csv - Information for each fly (condition, sex, size etc)
Morphometric information.xlsx - Raw morphometric data

Raw data (created by Code S3/1_Flight_mill_running_code.py):
21 Autumn/Mills/[mmdd] - Raw data for flight mill experiments on autumn migratory population
22 Summer/Mills/[mmdd] - Raw data for flight mill experiments on summer non-migratory population

Processed data (created by Code S3/2.1_Data_extraction.py):
Data S2/[Experiment season]/All flights.csv - Flight metrics on individual flight events
Data S2/[Experiment season]/Flight_stats.csv - Flight metrics per fly
Data S2/[Experiment season]/Transects.csv - Time transect (requires aggregation before analysis)
Data S2/[Experiment season]/All flights.csv - Information on individual flight events

Aggregated processed data (created by Code S3/2.2_Data_concatenation,R):
Data S2/RD All flights.csv - Flight metrics on individual flight events
Data S2/RD Flight_stats.csv - Flight metrics per fly
Data S2/RD Transects.csv - Time transect
Data S2/RD All flights.csv - Information on individual flight events

Statistical analysis and graphs (created by Code S3/3.1_Mill_Analysis.R)
Morphometric analysis and graphs (created by Code S3/3.2_Morphometrics.R)

##############
Morphometric information

Size:
Manuscript levels = small, moderate, large.
Data & analysis code levels = small, average, large
