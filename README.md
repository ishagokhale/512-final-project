# 512-final-project

# Goal 
The goal of this project is to understand how wildfire smoke affects respiratory health. Specifically, I'm looking at whether higher smoke levels lead to more deaths from respiratory diseases in the county of Dayton, Ohio. By analyzing smoke data and death rates, the project aims to find out if there's a connection between the two. The hope is that the findings will help guide policies and actions to protect people's health from the harmful effects of smoke, especially as wildfires become more frequent and intense.

## Licensing and Source Data
The yearly respiratory disease mortality rate came from the CDC WONDER page: https://wonder.cdc.gov/controller/datarequest/D74 

Centers for Disease Control and Prevention. CDC WONDER. U.S. Department of Health and Human Services, 2024, https://wonder.cdc.gov/cmf-icd8.html. 

The data for this project looks at the impact of wildfires, especially their effects on air quality in the western US. This dataset was collected and aggregated by the US Geological Survey. The dataset provides fire polygons in ArcGIS and GeoJSON formats. 
The source data is from https://www.sciencebase.gov/catalog/item/61aa537dd34eb622f699df81  

I used FIPS code, latitude and lognitudinal data for the city I was analyzing: Dayton, Ohio, which I got from its Wikipedia page linked here: nhttps://en.wikipedia.org/wiki/Dayton,_Ohio  

I found information on how to calculate AQI estimates through the following link: https://www.epa.gov/outdoor-air-quality-data/how-aqi-calculated  

I also used sample code in my notebookfrom Dr. David McDonald which is licensed through CC-BY, linked here:
https://creativecommons.org/licenses/by/4.0/

# Model Documentation
Below is the link and citation for the ARIMAX model documentation. 

"ARIMAX." PyFlux Documentation, PyFlux, 2024,
https://pyflux.readthedocs.io/en/latest/arimax.html.


# Data Files
# Input Files 
`estimate.csv`: File with article quality and last revision ID. It is an output file from a function in my notebook from part 1.  

## Data Schema 
The data schema of the `estimate.csv` file is as follows with columns being `Year` and `Estimate`:  
```
Year	Estimate
0	1962	0.000413
1	1963	0.000217
2	1965	0.000082
3	1966	0.000003
4	1967	0.000128
```  
`resp_16.txt`, `resp_78.txt`, and `resp_98.txt` are my health data files exported from the CDC WONDER website.  
The original data schema of my respiratory disease data is as follows with colums being `Year`, `Deaths`, `Population`, and `Crude Rate` which is the number of deaths by respiratory diseases per 100,000 people in Montgomery County, Ohio. I only ended up using the `Year` and `Crude Rate` columns. 
```
Year	Deaths	Population	Crude Rate
0	1968.0	301.0	616097.0	48.9
1	1969.0	281.0	611701.0	45.9
2	1970.0	287.0	609489.0	47.1
3	1971.0	241.0	604330.0	39.9
4	1972.0	256.0	600878.0	42.6
```
# Steps for Reproducibility
Make sure to have the latest python version (Python 3.10) or later so that installing the libraries is easy. Also you will need to refer to [Part 1: Common Analysis](https://github.com/ishagokhale/data-512-homework_3/). 



