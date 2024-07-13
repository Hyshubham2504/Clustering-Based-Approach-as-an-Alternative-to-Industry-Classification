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
