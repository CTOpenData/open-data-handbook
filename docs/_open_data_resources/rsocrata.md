---
layout: page
title: RSocrata
parent: Automation guidance
permalink: /open_data_resources/automation_guidance/rsocrata
nav_order: 19
---

# RSocrata (R) 
Set-up Difficulty: 2 | Use Difficulty: 3

## What it is
RSocrata is a package developed by the City of Chicago that allows the user to pull data sets from the Open Data Portal as well as write R data frames to the Open Data Portal. This tool does require some familiarity with the R programming language.

## How it works
The RSocrata package contains many functions and capabilities, two of which are almost always necessary when using this tool for data set automation. The read.socrata function lets the user read in a data set from the Open Data Portal to their local R environment (e.g. R Studio). The write.socrata function, on the other hand, allows the user to upload an R data frame to a data set on the Open Data Portal. The user has multiple options for update functions, which include append, replace, and upsert. The user must provide a Socrata username and password before receiving access to read in a private data set from the Open Data Portal; credentials are not required to read in a public dataset. Once the user’s R file contains all desired transformations and functions, a task scheduler such as Windows Task Scheduler can be used to automate the data set through regular updates. 

## Prerequisites
* Socrata account with the publisher or owner role
* Computer running a currently supported version of R
	* The latest version of R can be downloaded [here](https://www.r-project.org/){:target="_blank"}. 
* A currently supported R IDE, we recommend using RStudio
	* The latest version of RStudio can be downloaded [here](https://www.rstudio.com/products/rstudio/download/){:target="_blank"}. 

## When is this tool a good choice?
Using the RSocrata package is a great way to apply your own personal transformations to a data set for upload to the Open Data Portal. As mentioned before, users will need to be familiar with the R programming language to get the most out of the RSocrata package. Luckily, there is lots of documentation on basic R capabilities available online. Again, like other issues with some tools in this guideline, to automate this tool, you must use a task scheduler. Windows Task Scheduler, unfortunately, will only run tasks when the computer is on, so the user must still be vigilant with some regard to keeping updates, or the script may be run on a server that is always on. 

## Process Overview
How to set up your R script to be able to use RSocrata functions:
1.	Once you have RStudio open, click the File tab, and select New File > R Script. This will open a blank R script where you will write your code.
2.	At the bottom of your screen in the Console, write install.packages(“RSocrata”).
3.	Once the Console is done running installation, write “library(RSocrata)” at the top of your R script and run this line.
4.	On the next two lines of your R script, write the following:
socrata_username <- Sys.getenv("SOCRATA_EMAIL", "EMAIL_GOES_HERE")
socrata_password <- Sys.getenv("SOCRATA_PASSWORD", "PASSWORD_GOES_HERE")
Enter your Open Data Portal email and password where indicated above. 
5.	Run these two lines of code.
6.	If there are no errors, then your R script is set up and ready to use all RSocrata functionalities!

For more information and examples on how to use the RSocrata package, see the documentation for the package [here](https://github.com/Chicago/RSocrata){:target="_blank"}. 