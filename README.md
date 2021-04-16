# Correlation_Analysis_Feature_extraction

In this notebook, I'm striving to **build combined features as correlated as possible** with a particular target. To do so, I will first analyze correlation coefficients between features in the raw data space and then apply dimensionality reduction techniques such as **Principal Component Analysis (PCA) and Canonical Correlation Analysis (CCA)** to extract new combined features.

The final dataset (after cleaning and merging operations), contains for each country: its energy indicators (Energy Supply, % Renewable,...), its GDP and some statistics regarding energy-related documents that have been published by this country. In these statistics, there are the amount of released documents in Energy, the amount of citations that those documents have been subject to... The amount of documents is what we will target in a first place.

### Datasets :

- Statistics on Energy-related documents published by each country for the year 2013 from the [Sciamgo Journal and Country Rank data for Energy Engineering and Power Technology](http://www.scimagojr.com/countryrank.php?category=2102) and under the file `scimagojr-3.xlsx`.
The columns here are :

  - `Documents`: Number of documents published during 2013. It is usually called the country's scientific output.
  - `Citable Documents`: Selected year citable documents. Exclusively articles, reviews and conference papers considered.
  - `Citations`: Number of citations by the documents published during 2013. citations in years 2013, 2014, 2015...
  - `Citations per Document`: Average citations per document published during 2013
  - `Self Citations`: Country self-citations: Number of self-citations 
  - `H index`: Country's number of articles (h) that have received at least h citations. It quantifies both country scienti- fic productivity and scientific impact and it is also applicable to scientists, journals, etc


- `Energy Indicators.xls`, is a list of indicators of energy supply and renewable electricity production for +150 countries from the [United Nations](http://unstats.un.org/unsd/environment/excel_file_tables/2013/Energy%20Indicators.xls) for the year 2013

- GDP data from the file `world_bank.csv`, which is a csv containing countries' GDP from 1960 to 2015 from [World Bank](http://data.worldbank.org/indicator/NY.GDP.MKTP.CD). We will be interested by GDPs for the year 2013.
