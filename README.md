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

# Conclusion

#Contact
