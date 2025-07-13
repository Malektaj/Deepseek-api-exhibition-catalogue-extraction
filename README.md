# Deepseek-api-exhibition-catalogue-extraction
Extract, interpret and structure data from Historical exhibition catalogues for the purpose of research using Deepseek's LLM capabilities

# **Quick overview**

This GitHub repository was made as supplement to my Master’s thesis and contains 3 files.
1. The python code for the pipeline used to extract, interpret and structure data from 19th century Dutch exhibition catalogues. 
2. a raw output example (small)
3. The final dataset used throughout my thesis, after manual cleaning and manual data addition.


---



## **Aim**

The aim of the pipeline is to use LLMs (in this case DeepSeek’s reasoner model accessed through their API) to extract, interpret and structure data about art exhibitions from digitized exhibition catalogues in PDF format (text extractable). With the purpose of creating a dataset compatible with statistical analysis of catalogue data. 

---

## **Dependencies**

- pandas
- PyMuPDF (fitz)
- tqdm
- openai
- csv
- os
---

## **Output**

After inputting a PDF folder of Dutch exhibition catalogues, the pipeline output will consist of an Excel file with the following columns:
-	Catalogue identifier
-	Year
-	Duration
-	Institution
-	Type
-	Catalogue price
-	[Weekday] open
-	[Weekday] time
-	[Weekday] lowest price
-	[Weekday] highest price
-	Membership available
-	Membership price
-	Membership benefits
-	Competition
-	Lottery ticket price
-	Minimum age
-	Total entries
-	Misc.
-	Reasoner


---

# **How to use**

Whilst the data in the repository is specific to my case study, the methodological model can be reproduced for other kinds of digitized (historical) documents and is guided by the following steps: 
1.	Identifying categories and standardizing formatting rules for the data.
2.	Running the pipeline after adjusting columns and the prompt  in accordance with the standardization rules.
3.	Manual validation, fixing and amendment of missing data 
4.	Cleaning the data 
5.	Performing statistical analysis



To run the code locally make sure to:
-	Load **your own API key** and preferred model
-	Load your own input folder 
-	Adjust the columns and prompt to suit your own data needs
-	Check whether your PDF files contain extractable **machine readable text**
