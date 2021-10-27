---
author: Ben Taft
copyright: (C) 2021 by Higher Expectations for Racine County
title: List of Sources for Census Data
---

## Basic API Calls

the URL is:
```{python}

def acs_table_api_url(year: int,
                      estimate_duration: int,
                      table: str,
                      geography: str,
                      key: str) -> str:
    r"""Build a call to the Census's REST api for ACS data."""
    root_url = f'https://api.census.gov/data/{year}/acs/acs{estimate_duration}'
    query = f'get=group({table})&for={geography}'
    return f'{root_url}?{query}&key={key}'

```

## Tables of Interest

### ACS 1-Year Tables

Educational Attainment
: Table S1501

Employment Status
: Table S2301

### ACS 5-year Tables

#### Employment Status `x` Sex `x` Age
Table B23001

#### Employment Status for the Population 16 Years and Over
Table B23025

#### Sex by Age by Race by Employment Status
Table C23002
## Other census-like data sources

Local Area Unemployment Statistics
: [Wisconomy LAUS](https://jobcenterofwisconsin.com/wisconomy/pub/laus.htm)
