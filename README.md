# Assignment A2: Bias in Data

This repository contains a report (ipynb), data sources and output files for Assignment A2: Bias In Data of the course DATA 512 of the 2021 fall quarter in MSDS at UW.

## Goal

The goal of this assignment was to explore the concept of bias using data on Wikipedia articles - specifically, articles on political figures from a variety of countries and the estimated quality of articles based on a machine learning service called ORES (originally an acronym for "Objective Revision Evaluation Service") and documented at https://ores.wikimedia.org/ .

## Files

This repository contains 1 jupyter notebook and 4 data files.

### hcds-a2-bias.ipynb
The data processing code and report of the analysis in the form of a jupyter notebook.

### pages_data.csv
A list of politician article names on Wikipedia, sourced from Figshare.

> Keyes, Os (2017): Politicians by Country from the English-language Wikipedia. figshare. Dataset. https://doi.org/10.6084/m9.figshare.5513449.v6

*Schema*

- page: the name of the Wikipedia article page
- country: the name of the country of origin of the politician
- rev_id: the revision id of the article


### WPDS_2020_data.csv
A list of countries and their corresponding population. The file obtained from the [assignment page](https://docs.google.com/spreadsheets/d/1CFJO2zna2No5KqNm9rPK5PCACoXKzb-nycJFhV689Iw/edit?usp=sharing) and was originally sourced from the Population Reference Bureau at https://www.prb.org/international/indicator/population/table/ .

*Schema*

- FIPS - unique code identifying the country or region
- Name - the name of the country or region
- Type - a type specifying whether the row indicates a country or region
- TimeFrame - the year in which the 
- Data (M) - the population of the country (in millions)
- Population - the population of the country

### wp_wpds_countries-no_match.csv
An output containing a list of countries for which no match was found between the country names listed on the WPDS data source and the Wikipedia data source.

*Schema*

- page: the name of the Wikipedia article page
- country: the name of the country
- revision_id: the revision id of the article
- population: the population of the country
- region: the geopolitical region of the country
- score: the estimated quality score of the article

### wp_wpds_politicians_by_country.csv
An output file containing a list of politician articles and the corresponding estimated article quality.

*Schema*

- country: the name of the country
- article_name: the name of the Wikipedia article page
- revision_id: the revision id of the article
- article_quality_est: the estimated quality score of the article
- population: the population of the country

## Licenses

The code provided in this repository (ipython) is released under the MIT License. The content accessed via the Wikimedia REST API is licensed under the CC-BY-SA 3.0 and GFDL licenses. Please read Wikimedia’s Terms of User and Privacy Policy. 
