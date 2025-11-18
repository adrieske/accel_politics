# accel_politics

### Project summary: 

This study tests whether **local political leanings** predict district adoption of **middle-grades acceleration**, focusing on **H1: the availability of Algebra I in grades 7–8**. I link **Cook Partisan Voting Index (PVI)** at the U.S. Congressional District level to public **school districts (LEAs)** using an **enrollment-weighted crosswalk**, then model whether a district **offers Algebra I in 7th/8th grade** (from **CRDC 2021–22**) as a function of PVI. The main specification is a **logistic regression** with **state fixed effects** and standard controls (enrollment, %FRL, %ELL, racial composition, locale, charter share, teacher FTE per pupil), reporting **average marginal effects** and predicted probabilities across PVI bins. Robustness checks include single-CD districts only, area-weighted PVI, and replacing PVI with county vote share. Outputs are one results table and one figure showing the probability of offering Algebra 7/8 across the ideology spectrum.

Author:
Ashley Hill-Rieske University of Arkansas adhill\@uark.edu
Date of data collection: 11.7.2025
File:
Data it contains:
Date created: 11.7.25

------------------------------------------------------------------------
File: PVI2023.csv
Data it contains: Partisian Voting Index by Congressional District
Date downloaded: 11.7.2025
Source: <https://www.cookpolitical.com/cook-pvi/2023-partisan-voting-index/118-district-map-and-list>

*this is the most recent version of publicly available data*
------------------------------------------------------------------------
File: CDtoSD2020.txt
Data it contains: Congressional District to School District Relationship 2020
Date downloaded: 11.7.2025
Source: <https://www.census.gov/geographies/reference-files/time-series/geo/relationship-files.2020.html#list-tab-1709067297>


Description of methods for data collection or generation:

Description of methods used for data processing:

Packages Needed:

```{r load-packages}
library(tidyverse)
library(tidyr)
library(tibble)
library(Amelia)
library(rstatix)
library(readr)
library(data.table)
```
