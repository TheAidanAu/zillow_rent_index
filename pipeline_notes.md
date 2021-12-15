
#### Sources (csv)

unemployment_csv
https://data.bls.gov/timeseries/SMS12000000000000001?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true

multifam.csv - email from Kyle

nonfarm.csv
https://data.bls.gov/timeseries/SMS12000000000000001?amp%253bdata_tool=XGtable&output_view=data&include_graphs=true


FLSTHPI.csv
https://fred.stlouisfed.org/series/FLSTHPI


acs

This df was made by concatenating a bunch of acs_(year) dfs, which in turn were downloaded from BigQuery, specifically the census_bureau_acs database and tables zip_codes_(year) (5yr) (confirmed by Aidan Dec 14)

Update Dec 14: we changed the data source to be the tables zcta_(year) (5yr) instead.




#### Pipeline

From these files, Jacob created the total_df in the notebook "Rent Idx Initial EDA" and wrote the file total_df.csv

From here, John created ols models in one_model_per_year and First_cut_pred_model, though the latter used the data for all years to fit one ols, which at the moment does not seem to be the right choice, so that notebook is probably a dead end.

We also anticipate that Jacob and/or Jordan will have our first cut of a random forest shortly.  Dec 14: Aidan seems to have working RF model.

#### Features

see features.md

#### Models

one_year_one_model (ols)
full_df_modeling (rf)

TODO:

John - ARIMA-ish, time series models
Jordan - clustering
Jake - tree boost models
Aidan - RF

#### Outstanding Issues / Notes:



1. Important - Feature list.  We have some record now of our data sources, but still very little documentation of the features.  I'll do this unless somebody else wants.

2. Aidan's RF works, at least to the point of generating reasonable #'s.  I put his model into the consolidated folder and took out Jordan's.

3. Minor: Aidan/Jake verify they downloaded the zcta files from BQ as the starting point, plus a query file would be helpful.

4. Minor: zips - Aidan is getting zips as the subset of the zri data matching certain counties in 01_Target_Cleaning.  I don't think he has enough counties, and we're prob missing zips.

This is getting merged into the acs data later downstream, and I'm not sure how this is affecting things.

We could add more counties to aidan's list, or alternatively we could match w some census bureau files I just uploaded.

5. Minor: No concatenation to make the acs file read by the Read Idx Initial EDA notebook.  this should be a small change 

6. Models to iterate on:

John - ARIMA-ish, time series models
Jordan - clustering
Jake - tree boost models
Aidan - RF

7. Predictions - in a qualitative sense.  I don't think we understand really how we intend to generate predictions from presumably working plausible models.  I don't know if there's anything to do here at the moment, but this is coming soon.

8. Target data.  So far we've been using the multifamily data from zillow.  But there were other zillow files as well.  So we should understand and justify what we're doing there.

