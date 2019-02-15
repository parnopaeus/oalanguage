# README

## Project Information	

This repository contains text data and code for analysis of language used on Open Access websites. The project owners are Lauren B. Collister (lbcollister@pitt.edu) and Melissa Cantrell (melissa.cantrell@colorado.edu). 

### About the text files

The files found in the "texts" folder contain HTML from the main content pane of several websites. The HTML was obtained by hand by using "View Source" at each website. In some cases, PDF files that were on these websites were converted to text. 

The source URLs are contained in the CSV file "datasources_oalanguage.csv". Only the content from  "Definition", "Secondary Page", and "Tertiary Page" URLs are included in the "texts" folder. 

## Analysis 

The code for the analysis of the texts is included in the Jupyter Notebook file "Processing.ipynb". The code and output can be viewed in GitHub or run on your own machine after cloning the repository. 

The "textstat" package is required for running the analysis. More information about textstat can be found at https://pypi.org/project/textstat/ 

Outputs of the analysis were put into a spreadsheet for easier use and analysis. 

### Analysis spreadsheet

The raw numbers for our analysis are available in the spreadsheet titled "analysis_numbers.csv". There is also an Excel .xlsx file with the below information included as comments, and the publisher names in a different order to match other data collected for this project. 

The information in this spreadsheet contains the following columns: 
* Source for the texts 
* Link count 
	* Link counts were gained by counting the number of occurrences of "href" in the text. HREF indicates an active, clickable link in the text. For some of the files that were converted from PDF to Text, HREF links were manually added by the author to duplicate the active links found in the PDF file.
* Word count
	* Calculated using the textstat package in Python, on "cleaned" files with no HTML, and not counting any punctuation.
* Sentence count
	* Compiled using the textstat package in Python, on "cleaned" files with no HTML, with the command "sentence_count".
* Average words per sentence
	* Calculated by dividing Word count by Sentence count
* SMOG index
	* Calculating using smog_index in the textstat package in Python on "cleaned" files. Note that this measure is not effective for texts with fewer than 30 sentences. This measure was chosen because it was used in another study that we read.
* Flesch Reading Ease Score
	* Calculated using the flesch_reading_ease command in textstat package of Python on "cleaned" files. A score of 90-100 means that the text is very easy to read. A score of 50-59 means that the text is fairly difficult to read. A score of 0-29 is "Very confusing". A negative score is valid.
* Combined grade level
	* Calculated using the text_standard function in textstat package of Python on "cleaned" files. The number indicates the approximate grade level required to read the text, where "11" means 11th grade reading level.






