# group10finalproject

#Group 10 - This is the step by step explanation of extracting HIV data from the CDC website. 

## Scraping data from CDC HIV website - A python script for the scraping surveillance data from CDC HIV webpage. 

### Setup - You need `python>3.5` to run this script. 

The project depends on the `pandas` library,  

install it with pip:`pip install pandas` 

Other libraries needed include 

import urllib 

import bs4 as bs 

from bs4 import SoupStrainer 

from bs4 import BeautifulSoup 

import urllib.request, urllib.error, urllib.parse 

import csv 

 

## How to run?You can run the script from jupyter notebook  

Open the Scrape_Diseases python notebook to run python codes and obtain all CDC diseases and corresponding links- confirm initial website and insert in code as URL. 

Follow steps on python file to save all diseases and links to a csv file. Change the path to save the file to your preffered location. 

Open the Scrape_PDF python notebook to run python codes and obtain all the reports from HIV webpage. 

Save all files to a preferred location. 

 
## Extracting from PDF
Using Google Colab, install tabular-py and use the following codes to extract tables from the pdf into dataframes and then use previous codes to save to csv. 

‘import tabula’ 

pdf_path = "https://drive.google.com/file/d/1yYfDzeu6L3Kb9SbzO3TiXGo-I0xOyE5D/view?usp=sharing" 

 
dfs = tabula.read_pdf(pdf_path, stream=True, pages="all") 

# read_pdf returns list of DataFrames 

print(len(dfs)) 

dfs[0] 

Convert to csv 
