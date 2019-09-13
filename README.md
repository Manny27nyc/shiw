# Pre-processing script: Survey of Household Income and Wealth (Bank of Italy)

The Bank of Italy makes anonymised microdata available from its Survey of 
Household Income and Wealth. Further information about the data and the 
conditions for use is available [here](https://www.bancaditalia.it/statistiche/tematiche/indagini-famiglie-imprese/bilanci-famiglie/distribuzione-microdati/index.html).

For many applications, it is useful to have a unique identifier for individuals 
across waves of the survey (from 1989 and onwards). Unique identifiers are 
not provided in the original data, however they can be inferred somewhat 
reliably using Stata code developed by [Simona Baldi and Michele Pellizzari](https://web.archive.org/web/20190913054023/http://www.frdb.org/language/eng/page/data/scheda/bank-of-italy-survey-of-households-income-and-wealth/doc_pk/9019).

This repository contains an R script which is inspired by the Stata code 
referenced above. It downloads the historical database from the Bank of 
Italy's website, extracts the "Components" data set, infers unique 
identifiers and saves the result to disk as a CSV file. Further information 
about the "Components" data set is available in the [documentation](https://www.bancaditalia.it/statistiche/tematiche/indagini-famiglie-imprese/bilanci-famiglie/documentazione/Shiw-Historical-Database.pdf?language_id=1) (p. 14-19) 
published by the Bank of Italy.
