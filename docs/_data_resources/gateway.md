---
layout: page
title: Gateway
parent: Automation guidance
grand_parent: Open data resources
nav_order: 3
---

# Gateway 
Set-up Difficulty: 4 | Use Difficulty: 1 
 
## What it is 
Socrata Gateway is a tool that has been directly integrated into the Socrata Dataset Management Experience (SDMX). This tool is set up and used within the Open Data Portal itself which allows for a one-time set up for scheduled updates.  
 
## How it works 
Gateway is used on the Open Data Portal and can be set up for already existing datasets as well as new ones. A server connection, called an Agent, is downloaded by the user onto the server or computer they are connecting to Socrata. Essentially, this Agent sets up a connection between the dataset on Socrata and the file directory on the user’s server or computer. Once this Agent connection is set up and working, the user can simply use Plug-ins to choose what types of files will be uploaded/updated on the Open Data Portal. Some useful plug-ins include CSV, TSV, and Excel; these are likely the most common plug-ins that are necessary for most datasets on the Open Data Portal. Unlike other tools, Gateway has a scheduler built in, meaning that daily, weekly, monthly, or annual updates can be scheduled. The scheduler allows the user to enter a specific time for updates as well. Once the scheduled update time is determined and entered, the user will have automatic updates set up that will perform a replace on the data.   
 
## Prerequisites 
* Socrata account with the publisher or owner role 
 
## When is this tool a good choice? 
Socrata Gateway is one of the best choices in this guideline document for just about every data set on the Open Data Portal. Although the set-up difficulty and time are higher than other tools, the ease of use heavily outweighs that set-up difficulty. Since Gateway is directly integrated into the Socrata framework used by the Open Data Portal, setting scheduled updates is extremely easy and intuitive. For most, the set-up time will take around 30 minutes or so However, this set-up is a one-time process for each data set you wish to automate. If the Open Data Portal continues to use Socrata services, Gateway is likely to be the most up-to-date and seamless option for automation.  

A log of known issues with Gateway is available on the Socrata website [here](https://support.socrata.com/hc/en-us/articles/360038535274-Gateway-Known-Issues){:target="_blank"}. 
 
## Process Overview  
To set up a Gateway connection for a CSV based dataset on the Open Data Portal, follow the instructions below.

To access the Gateway page on the Open Data Portal for a: 
 
### New dataset 
1.	Once logged onto the Open Data Portal, click the Create tab on the menu bar at the top of the screen. 
2.	Select the Dataset option. 
3.	Enter the name of your dataset. 
4.	Select the Add Data option on the homepage of your new dataset. 
5.	Select the third option down on the menu at the left of the screen – Connect to an External Data Source (Socrata Gateway). 
6.	You are now ready to set up your Gateway connection for this dataset. 
  
### Existing dataset 
1.	Once logged onto the Open Data Portal, go to the homepage of the dataset for which you would like to setup a Gateway connection.
2.	Click the Edit button near the top right of the homepage. 
3.	Select the Review & Configure Data option on the homepage of your dataset. 
4.	At the top left of the screen, click the Choose Data Source link – At the top left of the screen it will look like: Choose Data Source > Preview. 
5.	Select the last option on the menu at the left of the screen – Connect to an External Data Source (Socrata Gateway). 
6.	You are now ready to set up your Gateway connection for this dataset. 
 
To create a new agent and plugin for your Gateway connection follow the steps below: 

1.	Once on the Gateway page for your dataset, select the Provision new agent option at the top right of the screen. 
2.	Fill out the Agent Name field.
	* Suggested convention for naming the agent: Name of the person who is responsible for the agent + The data source type (e.g. Zaldonis_CSV).
3.	After you have named the agent, click the Download Agent button. 
4.	Allow the agent to download. 
5.	Select the agent and extract/unzip the compressed folder to the location of your choice. 
6.	FOR WINDOWS – Open the unzipped agent folder and right click the install.bat file (Windows batch file). 
7.	Select Run as Administrator. 
8.	The command prompt will open; give a name to your service, selecting a name that makes sense to you. 
9.	Press enter to submit your service name and press any key to close the command prompt once the job is complete. 
10.	Go back to your browser tab on the Open Data Portal and refresh the “Am I Connected?” box at the bottom of the Provision Agent pop-up. 
11.	Your agent should now be connected. 
12.	Click the Next button. 
13.	Select the Set-up a plugin bubble and click the Next button. 
14.	On the next page, you should see the CSV plugin; click the Set-up button. 
15.	After reading the overview page for the CSV plugin, click the Next button. 
16.	Fill out the Plugin Name field.
	* Suggested convention for naming the plugin: Name of the person who is responsible for the agent + The data source type.
17.	Click the Next button. 
18.	Follow the Set-up instructions on the next screen – this requires you to locate your data path of you agent as well as use the command prompt to run a single command. 
19.	After the command has been run, a new window will open, once here, simply select the root directory for all CSV files that are accessed by your dataset. 
20.	Your Gateway agent and plugin should now be connected! 

For additional resources on setting up Socrata Gateway, refer to the Socrata support article [Gateway Overview](https://support.socrata.com/hc/en-us/articles/360033395434-Gateway-Overview){:target="_blank"}.