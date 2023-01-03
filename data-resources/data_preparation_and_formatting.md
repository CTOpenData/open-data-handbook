---
layout: page
title: Data preparation and formatting
parent: Data resources
nav_order: 11
---

This section provides guidance on preparing datasets for publication as open data and makes recommendations on the format and structure for open data. This section was adapted from the California Open Data Publisher’s Handbook.

Formatting your file
•	Publish data in the rawest form that is appropriate. Keep in mind that data may be useful to a variety of users and may have applications beyond what the originating agency imagines. Remember that raw data should not be published if it poses a risk of harm, as discussed in the Data Aggregation section.
•	Remove metadata, footnotes, disclaimers, or any other clarifying information from the spreadsheet before importing—all of this should be included in the dataset’s metadata, outside of the dataset itself.
•	If working with an Excel spreadsheet, make sure that all your data is compiled into one sheet and included in the first tab of the workbook, since the Open Data Portal only imports the first tab of an Excel workbook. 
Column headers and order
Column Headers
•	Name the columns clearly so non-subject matter experts can understand what the columns represent.
•	Keep column header names short and provide a full description with more detail in the metadata. 
•	Each header must be unique. 
Column Order
•	If your dataset includes unique identifiers, they should be in the left-most column.
•	For time series data, the date and time variables should be to the left of the columns containing the variable data.  
•	Columns with varying levels of specificity should be ordered with the highest-level variable on the left and the most granular variables on the right. 
Text formats
•	Avoid use of all caps except for in specific cases like acronyms (e.g. CT, OPM, etc.)
Numeric formats
•	Remove commas and symbols from numeric data (e.g. use “1000” instead of “$1,000”).
•	Don’t include units of measurement in the data itself—describe units in the metadata. 
•	Use full numbers like 1200000 instead of 1.2 million.
•	Percentages can be expressed either as a proportion our of 1 or 100.
•	Percentages can be expressed as either a proportion out of 1 or 100 (e.g. 20% can be expressed as 20 or 0.2 as long as the representation of percentages is consistent throughout your dataset).
