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

### OA Definitions Spreadsheet

Qualitative analysis of Open Access definitions found on web pages for all source groups are available on the spreadsheet titled “OADefinitions_GitHub_20190220.csv”.

The information in this spreadsheet contains two tabs:

*  Data Sources - this tab includes links to the source pages on which definitions were found. The information in this tab contains the following columns:
	* Group - lists source groups
	*  Definition - link to web page on which definition used for analysis was found. Not all links may be currently active.
*  Definitions - this tab includes the qualitative analysis of definitions completed by Lauren Collister and Melissa Cantrell. The information in this tab contains 32 columns:
	*  Group - lists source groups
	*  Definition - text of definition copied from link in Data Sources tab.
	*  Free Access (Columns C-E) - Column C indicates whether definition includes concept of “Free Access” (Yes, No, or Maybe). If Yes, indicative text is listed in Column D. If Maybe, indicative text is listed in Column E.
	*  Read (Columns F-H) - Column F indicates whether definition includes concept of “Read” (Yes, No, or Maybe). If Yes, indicative text is listed in Column G. If Maybe, indicative text is listed in Column H.
	*  Re-Use (Columns I-K) - Column I indicates whether definition includes concept of “Re-Use” (Yes, No, or Maybe). If Yes, indicative text is listed in Column J. If Maybe, indicative text is listed in Column K.
	*  Redistribute (Columns L-N) - Column L indicates whether definition includes concept of “Redistribute” (Yes, No, or Maybe). If Yes, indicative text is listed in Column M. If Maybe, indicative text is listed in Column N.
	*  Remix (Columns O-Q) - Column O indicates whether definition includes concept of “Remix” (Yes, No, or Maybe). If Yes, indicative text is listed in Column P. If Maybe, indicative text is listed in Column Q.
	*  Immediate (Columns R-T) - Column R indicates whether definition includes concept of “Immediate” (Yes, No, or Maybe). If Yes, indicative text is listed in Column S. If Maybe, indicative text is listed in Column T.
	*  Permanent (Columns U-W) - Column U indicates whether definition includes concept of “Permanent” (Yes, No, or Maybe). If Yes, indicative text is listed in Column V. If Maybe, indicative text is listed in Column W.
	*  Online (Columns X-Z) - Column X indicates whether definition includes concept of “Online” (Yes, No, or Maybe). If Yes, indicative text is listed in Column Y. If Maybe, indicative text is listed in Column Z.
	*  Unrestricted (Columns AA-AC) - Column AA indicates whether definition includes concept of “Unrestricted” (Yes, No, or Maybe). If Yes, indicative text is listed in Column AB. If Maybe, indicative text is listed in Column AC.
	*  Scholarly Literature (Columns AD-AF) - Column AD indicates whether definition includes concept of “Scholarly Literature” (Yes, No, or Maybe). If Yes, indicative text is listed in Column AE. If Maybe, indicative text is listed in Column AF.


###  OA Choice Spreadsheet

Qualitative analysis of choice language as well as qualitative analysis of the costs of Open Access publishing are included on the spreadsheet titled “OAChoice_GitHub_20190220.csv.”

The information in the spreadsheet contains five tabs. The first tab contains data sources, the second tab contains the analysis of choice language, and the last three tabs contain the analysis of costs related to Open Access.

*  Data Sources - this tab includes links to all of the source web pages from which data was gathered for both the choice and cost analysis. Each of these analyses used a total of three webpages as the source data. Not all links may be currently active. The information in this tab contains the following columns:
	*  Group - lists source groups
	*  Definition - link to web page on which definition used for analysis was found.
	*  Secondary Page - link to second of three pages used in data sample. 
	*  Tertiary Page - link to third of three pages used in data sample. Tertiary page is only used in data sample if a “Dedicated Page” is not present (indicated by Columns E or F) and serves as the default third page.
	*  Choice OA - Dedicated Page - link to a web page dedicated to topic of Choice (typically related to hybrid Open Access). The Dedicated Page, if present, is used as the third of three web pages in the data sample. “Use Default” listed in this column indicates that no Dedicated Page was found, and the Tertiary Page is used instead.
	*  Cost of OA - Dedicated Page - link to a web page dedicated to topic of Cost. The Dedicated Page, if present, is used as the third of three web pages in the data sample. “Use Default” listed in this column indicates that no Dedicated Page was found, and the Tertiary Page is used instead.
*  Choice Language - this tab includes the qualitative analysis of Choice language completed by Lauren Collister and Melissa Cantrell. The information in this tab contains the following columns:
	*  Group - lists source groups
	*  Choice Language - language that contains the words “choice,” “option,” or derivative words is copied from the three source web pages.
	*  Choice/Option - this column indicated whether or not choice language was found to be present in the source web page sample. “Non-relevant” indicates that the words “choice” or “option” were present in the sample but were not found to be relevant to the analysis.
*  Cost Coding -  this tab includes the qualitative analysis of language about the costs of Open Access completed by Lauren Collister and Melissa Cantrell. The information in this tab contains the following columns:
	*  Group - lists source groups; each source group is listed four times, divided by page type - Primary, Secondary, Dedicated, and Tertiary.
	*  Cost of OA - text from each page related to costs of Open Access is copied and listed in this column. 
		*  NoData1 = Page does not exist; i.e. when NoData1 is listed for the Dedicated page, the Tertiary Page is used instead.
		*  NoData2 = Page exists but has no language relevant to the analysis.
	*  OA=Pay (Always, Usually, Sometimes, Never) - Analysis of whether text from “Cost of OA” column indicates that there are payments associated with Open Access publishing.
	*  Alternative Pay Models - Text that indicates methods of payment for fees associated with Open Access publishing is copied and listed here.
*  Alt. Cost Recovery Matrix - Using text from “Alternative Pay Models” Column in the “Cost Coding” tab, this tab indicates which cost recovery models for payments are indicated by each source group. If a cost recovery model is mentioned, the matrix is marked with an “X” in the relevant field. A grey row indicates that no cost recovery model was mentioned by that source group.
*  Cost Recovery Chart - Results from the Alt. Cost Recovery Matrix tab are summarized and displayed in chart form in this tab.





