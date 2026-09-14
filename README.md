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
2012-2024 (13 measured years).
## Sample Size:
559 observations across 43 states. 
## Key Variables:
| Variable | Description |
|---|---|
| Credit Card Delinquency | Share of credit card balances 90+ days past due |
| Auto Loan Delinquency | Share of auto loan balances 90+ days past due |
| Unemployment Rate | State-level unemployment rate (BLS) |
| Real GDP (log) | State-level economic output, log-transformed for percent-change interpretation |
| Income per Capita | Real income per capita by state |
| Population | State population level |

# Methodology

## Step 1: Data Construction

