# Sports Betting & Financial Deterioration
This project aims to establish the causal relationship betwen the introduction of sports betting legalization and a depreciation in household financial outcomes.

# Overview
After the overturning of the Professional and Amateur Sports Protection Act (PASPA) in 2018, sports betting became legalized in 39 states. Coinciding with this new development has been the rise of online gambling. There being decreased friction in access to gambling services means that households have more of an opportunity to engage with potentially financially detrimental behavior. We study how the implementation of online sports betting has affected consumer’s financial health. We utilize household credit card delinquency rates as a proxy for the purposes of this paper as it measures an inability to pay off short term debt. Our data is primarily pulled from the New York Federal Reserve’s Consumer Credit Panel which collects data on a 5% sample of filings from Equifax. The main finding of our paper is that states that have legalized online sports betting saw a ~2% increase in credit card delinquencies compared to states that do not. This coincides with an increase in unemployment rates, and auto loan delinquencies as well. As consumers become more open to risk taking, they take on greater burdens on their finances. These results demonstrate that broad legalization of sports has harmed household financial health by reducing their ability to pay down debt.

# Data
## Source(s): 
[The New York Federal Reserve's Center for Microeconomic Data](https://www.newyorkfed.org/microeconomics/databank.html) - a 5% nationally representative sample of Equifax credit filings, providing annual state-level delinquency and balance data (2003–2024)

Bureau of Labor Statistics - state-level population, unemployment, and labor force data (2005–2024).

Bureau of Economic Analysis - state-level real GDP and income per capita (2005–2024).

## Time Period:
Trimmed to 2012-2024 (13 measured years).

## Sample Size:
559 observations. Final panel of 43 states plus Washington, D.C. (26 treated during the sample period).

## Key Variables:
| Variable | Variable Name | Description |
|---|---|---|
| Credit Card Delinquency | cc_delinq | Share of credit card balances 90+ days past due |
| Auto Loan Delinquency | auto_delinq | Share of auto loan balances 90+ days past due |
| Mortgage Delinquency | mort_delinq | Share of mortgage balances 90+ days past due |
| Unemployment Rate | unemp | State-level unemployment rate (BLS) |
| Real GDP (log) | lnrgdp |State-level economic output, log-transformed for percent-change interpretation |
| Income per Capita | ricapita | Real income per capita by state |
| Population | pop | State population level |
| Treated | treat | =1 if a state ever legalized online sports betting, 0 if never |
| Post-Treament | post | =1 in years at/after a treated state's legalization year, 0 otherwise |

# Methodology
### Step 1: Dataset Construction

All source data (NY Fed, BLS, and BEA) was downloaded manually as CSV files directly from each agency's website. All analysis was conducted in Stata. The individual datasets (credit delinquency, GDP, labor market, and income per capita) were each reshaped and trimmed into long-panel `.dta` files, then merged together on `state` and `year`. Legalization years were merged in separately to construct the treatment variable, after which non-comparable states were dropped and the panel was finalized.
 
States permitting only **retail** betting (Washington, New Mexico, North Dakota, South Dakota, Nebraska, Wisconsin, Mississippi) are dropped since the focus is specifically on *online* access, as are Puerto Rico (incomplete CCP coverage post-2017) and Nevada (legalized prior to the study period). The sample is restricted to 2012 onward to focus on relevant pre-treatment dynamics.
