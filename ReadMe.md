# Analysis of US County's net per capita and Covids mortality rate and how well of an indicator is ADI for predicting Covids mortality rate in a county.

Does a US county's net per capita earnings impact how many Covid deaths occur? How well of an indicator is ADI (Average Deprivation Index) for a communities Covid Impact?

* Hypothesis 1: As ADI increases, the Covid Mortality Rate in that community will increase. 
* Hypothesis 2: As net per capita increases, the Covid Mortality Rate in that community will decrease.

The data obtained was from Google public data hub via Big query. The driving query pulls in from three data repositories; Johns Hopkins COVID time-series, US County FIPs Census key, and the Beuro of Economic Analysis.

# Data Description:


# Data Sources
## **Datasets**
1. Johns Hopkins Covid Dataset: Covid data in time series by county
2. Area Deprivation Index (ADI)
3. Beueo of Economic Analysis 

Total rows: 3143

Total features: 8

### JHU COVID DATASET ## 

This is the data repository for the 2019 Novel Coronavirus Visual Dashboard  operated by the Johns Hopkins University Center for Systems Science and Engineering (JHU CSSE). The data include the location and number of confirmed COVID-19 cases, deaths, and recoveries for all affected countries, aggregated at the appropriate province/state. It was developed to enable researchers, public health authorities and the general public to track the outbreak. Additional information is available in the blog post, Mapping 2019-nCoV , and included data sources are listed here . -- Taken from google big querys dataset 
description 

### GDP and Income by County - Bureau of Economic Analysis

"This public dataset was created by the Bureau of Economic Analysis (BEA). It provides a county-level view of income, wages, proprietors' income, dividends, interest, rents, and government benefits, including several federal and state-level subsidies.

Per capita income is used to gauge the average financial health and associated social needs of an area.

economic indicators measured by the Department of Commerce or reported to other public agencies <a href="https://apps.bea.gov/regional/definitions/"> Economic accounts and definitions</a>
" -- Taken from google big querys dataset 
description 

### Area Deprivation Index (ADI)

"The Area Deprivation Index (ADI) can show where areas of deprivation and affluence exist within a community. The ADI is calculated with 17 indicators from the American Community Survey (ACS) having been well-studied in the peer-reviewed literature since 2003, and used for 20 years by the Health Resources and Services Administration (HRSA). High levels of deprivation have been linked to health outcomes such as 30-day hospital readmission rates, cardiovascular disease deaths, cervical cancer incidence, cancer deaths, and all-cause mortality. The 17 indicators from the ADI encompass income, education, employment, and housing conditions at the Census Block Group level."-- Taken from google big querys dataset 
description 

## Details
The Data consists of around 3,200 rows - one row per US county - and 8 columns.

#### state_fips_code
State Level FIPS codes defined by the US Census

#### state
* US State

#### fips
* FIPS codes defined by the US Census

#### area_land_meters
* Area in square meters for that areas FIPS Entry

#### total_deaths
* Total COVID deaths up to 12-31-20 grouped by county

#### total_recovered
* Total COVID recovery up to 12-31-20 grouped by county

#### population
* Total US population as calculated in the 5-year population estimate - as of March 2019 (note that this is not the most up to date population count)

#### Percapita_net_earnings
* Net earnings by place of residence of a given area divided by the resident population of the area. See "net earnings by place of residence."

### ADI
* ADI: An index of socioeconomic status for communities calculated in 2020 via 17 indicators from the American Community Survey (ACS)
* A low Average Deprivation index indicates that the community has lower deprivation & vice versa.

### Cause-specific mortality rate

*Cause-specific death rate Number of deaths assigned to a specific cause during a given time interval - in the case of this project were looking at Covid.
*(deaths by specific cause/total population of area) * 100,000