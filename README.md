# Projeto SUS Mortalidade

Project status: In progress

# Project objective

This project was developed with the goal of better understanding the health conditions of the states and cities of Brazil, in order to be able to perform comparative analysis between them and generate insights. 
# Methods

* List comprehension
* Zip
* for loop
* try, except
* Drop methods
* Merge datasets
* Loc
* Regex - findall
* Python dataset analysis (verifyng nulls percentage, head, tail, shape, info, describe, etc.)
* Pd.to_datetime
* Visualization


In this project several different cleaning data approaches were used, all of them are explained in detail  in the jupyter notebook archive - Projeto SUS.ipynb (in portuguese).

# Technologies

* Python
* Pandas
* dbfread library
* Tableau

# Project description

The SUS makes the files available in the dbc format on the website: https://datasus.saude.gov.br/transferencia-de-arquivos/ by clicking in:

SIM - Sistema de Informação de Mortalidade -> Dados -> DO - Declarações de Óbito - 1979 a 2021 -> Selecionar Ano desejado -> Selecionar estados -> Download -> arquivo.zip.

All the terms of the project relating to race, sex and other categorizations were taken unaltered from the SUS database.

The dataset obtained has 80+ columns and millions of lines, making it impossible to clean with excel. Several of the columns were dropped as they are not relevant for the analysis.

# Steps

* Data Engineering

The project started with a challenge, which was to convert dbc files to csv. After searching, I found the TabWin program to convert dbc to dbf, after this development, I made a code using the dbfpy library to make the conversion. The conversion worked but was inefficient as it added spaces and punctuation which were not needed and some of the archives returned an error, as the codec used changed from ascii to asciii. After another search, I found a code using de dbfread library to read the archive and use the csv library to transform it in text and transform to_csv. After some testing, the results were better than the last code as the size of each csv was 3 times smaller. Because of hardware and time limitations, I made slight alterations to the code, I needed it to be in a loop (as I had several different dbfs) and to print any errors that may appear so I could let the code run throughout the night.

After the code run, I had to concat each year in a different csv as there were one csv to each state of Brazil in all years. Checking the result of the concat, I discovered that in some cases there were a few extra lines, so as a security measure, I droped the duplicated lines in the dataset then transfomed to csv to be read in Tableau.

I started analysing the database and discovered that important columns had brazil's IBGE codes in them, for location and age. So I after some thought, I decided to make another csv file with the IBGE codes for location so that later Tableau could relate the code in SUS spreadsheets to the IBGE spreadsheets. Continuing the analysis, the columns that had 15+ percentage of nulls were dropped (after deciding if they were useful or not to the objective) and that made the dataset have 42 columns.




* Data Analysis


# Conclusion

# Contact
