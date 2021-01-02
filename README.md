# Welcome 
###### Electricity dataset analysis in a Zip...!

This project is a Python script that runs to visualize electricity datasets and complile the results into a Microsoft Word document.

# REPORTING PROCESS Examples

Your Microsoft Word Doc Report will contain all the following information:
###### PLOT OF ENTIRE DATASET
![Alt text](https://github.com/bbartling/zip/blob/master/images/1.PNG)

###### SUMMARY STATISTICS
![Alt text](https://github.com/bbartling/zip/blob/master/images/2.PNG)

###### BOX PLOTS PER MONTH
![Alt text](https://github.com/bbartling/zip/blob/master/images/10.PNG)

###### POWER CONSUMPTION TRENDS
![Alt text](https://github.com/bbartling/zip/blob/master/images/11.PNG)

###### HIGHEST RANKED CHANGES FOUND IN DAILY ELECTRICAL LOAD PROFILES
Functions within Zip break the dataset down to individual daily datasets where a Python package called `ruptures` is utilized to compute changepoints found in each daily electrical load profile. The `pandas` computing library is then used to rank the top 15 days in the datatset.

![Alt text](https://github.com/bbartling/zip/blob/master/images/3.PNG)

###### DAILY UPPER AND LOWER QUANTILES (ELECTRICITY HIGH & BASELOAD LOAD VALUES)
![Alt text](https://github.com/bbartling/zip/blob/master/images/4.PNG)

###### DAILY MAX DEMAND AND HOUR
![Alt text](https://github.com/bbartling/zip/blob/master/images/5.PNG)

###### ROLLING KWH 7 DAY AVERAGE
![Alt text](https://github.com/bbartling/zip/blob/master/images/7.PNG)

###### DEMAND PLOTS BY MONTH
![Alt text](https://github.com/bbartling/zip/blob/master/images/9.PNG)

###### CHANGE POINT ALGORITHM PLOT ON MAX DEMAND DAY
![Alt text](https://github.com/bbartling/zip/blob/master/images/8.PNG)




###### How do I get started with Zip for my electricity dataset analysis? 
(1) Git clone the Zip repo. For anyone not familiar with Github see this tutorial.
https://packaging.python.org/tutorials/installing-packages/


(2) Download and install Python. I have tested the scripts out on Windows 10 environment on Python 3.7.
https://www.python.org/downloads/


(3) Make sure that you `pip` install all necessary packages to run Zip. Anyone not familiar with `pip` see this tutorial.
https://packaging.python.org/tutorials/installing-packages/

All packages can be installed at once with the `requirements.txt` file. On Windows in the Zip folder directory from the command prompt run:
`py -m pip install -r requirements.txt`,


(4) A tip on how to open up the command prompt in the Zip folder directory with a Windows 10 environment:
 ![Alt text](https://github.com/bbartling/zip/blob/master/images/One.PNG)
 
 
(5) Type `cmd` and hit `ENTER`:
 ![Alt text](https://github.com/bbartling/zip/blob/master/images/cmd.PNG)
 
 
(6) Next type `py -3.7 main.py City_Library_2019` in the command prompt with the name of the CSV file to analyze and hit `ENTER`. Note this is the name of the CSV file without the .csv extension. CSV files are a requirement see note 7 for pre data processing in Excel prior to using Zip. All data files must be placed in the `sample_data` directory prior to running the script `main.py`.
 ![Alt text](https://github.com/bbartling/zip/blob/master/images/app.PNG)
 

(7) NOTE - Modify as necessary in Excel your utility provider supplied data files prior to running the script `main.py`. Only run 1 year of data at a time with Zip. Make the name of the CSV file simple that utilizes an `_` character instead of a ` ` (space) character. The Excel CSV file needs to be formatted that the time stamp column is named `Date` and the electricity column is named `kW` as demonstrated below. 

![Alt text](https://github.com/bbartling/zip/blob/master/images/excel.PNG)

If your utility provider dataset has the time and date stamp in seperate columns use this as a reference for combining date and time into one column.

https://www.extendoffice.com/documents/excel/1538-excel-combine-date-and-time.html

The file format requires a CSV file type extentions, make sure in Excel to save the file as a CSV as shown below.

![Alt text](https://github.com/bbartling/zip/blob/master/images/CSV.PNG)

Zip data analysis uses the `ruptures` package to calculate changepoints in the electricity interval data. See https://github.com/deepcharles/ruptures for more detail about the change point process. Zip uses the dynamic programming method provided by Ruptures.




Please send me some feedback on how this tool can be improved! bbartling@slipstreaminc.org
Thank you for using zip. Feel free to send me an email if you are new to Python and would like some help getting setup.
