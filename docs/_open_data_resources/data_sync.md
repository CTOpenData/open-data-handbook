---
layout: page
title: DataSync
parent: Automation guidance
permalink: /open_data_resources/automation_guidance/datasync
nav_order: 1
---

# DataSync 
Set-up Difficulty: 2 | Use Difficulty: 2 
 
## What it is 
DataSync is an executable Java application that provides replace, append, delete, and upsert capabilities on a dataset. This tool allows for automated updates when used alongside a task scheduler such as Windows Task Scheduler.  
 
## How it works 
Users can access DataSync processes through the graphical user interface (GUI) or in the command line. (This guideline only covers using the GUI.) DataSync allows for CSV or TSV file uploads from your local machine or a networked hard drive such as SharePoint. Once the user has set up their DataSync task, it can be saved as a .sij file. This file can then be used in a basic task in an application like Windows Task Scheduler.  
 
## Prerequisites 
* Computer or server running Java 8 or higher 
	* The latest version of Java can be downloaded here.
* Socrata account with the publisher or owner role 
* An app token for the desired dataset. (The app token will be the Socrata Dataset ID of your dataset. This can be found by accessing the Socrata API from the Open Data Portal. The ID will be in the form of xxxx-xxxx.) 
 
## When is this tool a good choice? 
DataSync is a great tool for someone who is looking to simply update a dataset. Furthermore, the set-up for this tool is very simple when compared to other tools in this document. One of the biggest issues, however, is that for this tool to automatically update, it must be run through a task scheduler. Windows Task Scheduler, for example, will not run tasks if the computer is not on, so this tool requires some level of user responsibility, even after set-up. For more information and to download DataSync, please visit the Socrata website here.

## Process Overview  
1.	Select the file from your local hard drive that you wish to upload to your data set. This must be a CSV or TSV file.  
2.	Enter the Socrata Dataset ID of your dataset. This can be found by accessing the Socrata API from the Open Data Portal. The ID will be in the form of xxxx-xxxx.  
3.	Choose from one of four update methods: replace, append, upsert, or delete.  
	* Replace will replace the current dataset on the Open Data Portal with the dataset from Step 1. 
	* Append will add all rows from the dataset in Step 1 to the end of the dataset on the Open Data Portal. 
	* Upsert will update the current dataset on the Open Data Portal as well as append any new rows from the dataset in Step 1. 
	* IMPORTANT: A Row Identifier must be in place within select columns of the dataset on the Open Data Portal. For more information about how to set up a row identifier on the Open Data Portal, refer to the Socrata support article Setting a Row Identifier in the Socrata Data Management Experience. 
	* Delete will remove all rows in the dataset on the Open Data Portal that match the Row Identifiers from the dataset in Step 1. Essentially, the dataset from Step 1 would be a single column containing the Row Identifiers to be deleted. 
	* As with the Upsert option, the Delete option also requires Row Identifiers to be in place in the dataset on the Open Data Portal. 
4.	Click the “Map fields” button to check that the columns from your dataset in Step 1 map to the correct columns in the dataset on the Open Data Portal. 
5.	Enter in the required information (domain, username, password) in the fields at the bottom. The domain will be https://data.ct.gov, and the username is your email for accessing the Open Data Portal and the password is your Open Data Portal password. 

![DataSync GUI](../assets/automation_1.png)
Screenshot of the DataSync GUI 