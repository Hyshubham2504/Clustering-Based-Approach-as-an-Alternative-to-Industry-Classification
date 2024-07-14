Link to the latest Google Colab where we can edit together: https://colab.research.google.com/drive/1Ju6XtVf3VGDIqfLtXRdgFisjajzWIGvo#scrollTo=wz5w3X49OU4Y

Some notes:
- We used to only have GEV and SOLV having no data at all for this 20-year period, but now there's a new one called SW. SW seems to be a very new company (?) according to Yahoo Finance
- Cleaned daily returns dataframe is df
- GICS dataframe is gics_df
- The different periods are defined in this way:
  - pre_financial_crisis: 2004-01-01 to 2006-12-31
  - financial_crisis: 2007-01-01 to 2009-06-30
  - post_financial_crisis: 2009-07-01 to 2019-12-31
  - covid_period: 2020-01-01 to 2022-12-31
  - post_covid_period: 2023-01-01 onwards
- I updated some notes on Jamboard: https://jamboard.google.com/d/13BWRG236EF7aWxrnhi-JCuZ1tOTGAd7toGYV45SmaR8/viewer?pli=1&mtt=fhsgn8vofbir&f=0 . Specifically, I don't use GridSearchCV because apparently it doesn't make sense to do cross validation on clustering (unsupervised model).
- For hierarchical clustering with correlation matrix, using method 'average', 'single', and 'complete', will always result in very imbalanced clusters (2 clusters with 1 super big cluster and 1 almost-empty cluster, thus very sensitive to outliers, or just in general produce clusters where 1 cluster has 10 times the size of the other cluster). So I only use 'ward' with 'euclidean', and only do "hyperparameter tuning" on n_clusters.
