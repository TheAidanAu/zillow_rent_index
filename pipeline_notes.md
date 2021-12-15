
#### Sources (csv)

unemployment_csv
https://data.bls.gov/timeseries/SMS12000000000000001?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true

multifam.csv - email from Kyle

nonfarm.csv
https://data.bls.gov/timeseries/SMS12000000000000001?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true


FLSTHPI.csv
https://fred.stlouisfed.org/series/FLSTHPI


acs

This df was made by concatenating a bunch of acs_(year) dfs, which in turn were downloaded from BigQuery, specifically the census_bureau_acs database and tables zip_codes_(year)_5yr (confirmed by Aidan Dec 14)




#### Pipeline

From these files, Jacob created the total_df in the notebook "Rent Idx Initial EDA" and wrote the file total_df.csv

From here, John created ols models in one_model_per_year and First_cut_pred_model, though the latter used the data for all years to fit one ols, which at the moment does not seem to be the right choice, so that notebook is probably a dead end.

We also anticipate that Jacob and/or Jordan will have our first cut of a random forest shortly.

#### Features

see features.md

#### Models

one_year_one_model (ols)
full_df_modeling (rf)



