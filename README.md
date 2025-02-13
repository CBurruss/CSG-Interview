# New Orleans Calls for Service (2023) Analysis

This project analyzes patterns in New Orleans calls for service (CFS) data from 2023, examining how various risk factors and census characteristics relate to different types of service calls across neighborhoods.

## Research Questions

1. How do environmental risk factors and socioeconomic characteristics correlate with different CFS categories across geographic scales?
2. Which neighborhoods show the highest concentration of each call type, and what are their distinguishing characteristics?
3. How do different risk factors correlate with each CFS category?
4. Which socioeconomic factors show the strongest relationships with CFS patterns?

## Dependencies

### R Packages
- **Data manipulation/cleaning**: tidyverse, readr, janitor, lubridate, tidygeocoder
- **Geospatial data**: sf, geojsonio, tigris, spdep, FNN
- **Visualization**: ggplot2, ggthemes, viridis, gridExtra, knitr
- **API integration**: RSocrata

### Python Libraries
- **Data manipulation/cleaning**: pandas, siuba, coconut*
- **Machine learning**: scikit-learn
- **Natural language processing**: spacy
- **Visualization**: terminaltables
- **API integration**: pydrive

## Environmental Notes

- Project completed in a polyglottal Jupyter notebook utilizing the Script of Scripts (SoS) analysis framework
- Enables dynamic switching between sub-kernels (Python, R, etc.)
- Facilitates spatial file manipulation in R while allowing Python-based classification
- *SoS provides access to coconut compilation (see: https://coconut-lang.org/)

## Data Sources

- [NOPD Calls for Service (2023)](https://data.nola.gov/Public-Safety-and-Preparedness/Calls-for-Service-2023/pc5d-tvaw/about_data)
- [Code Enforcement Violations](https://data.nola.gov/Housing-Land-Use-and-Blight/Code-Enforcement-All-Violations/3ehi-je3s/about_data)
- [Chapter 66 Lot Abatements](https://data.nola.gov/Housing-Land-Use-and-Blight/Grass-Cutting-Lot-Abatement-Chapter-66-/xhih-vxs6/about_data)
- [311 Service Requests](https://data.nola.gov/City-Administration/311-OPCD-Calls-2012-Present-/2jgv-pqrq/about_data)
- Census Tract Data (ACS 2019-2023)
- Various spatial files (NOPD districts, neighborhoods, etc.)

## Methodology

1. **Spatial Data Processing**
   - Process GeoJSON files for districts and neighborhoods
   - Create standardized fishnet grid for analysis

2. **CFS Classification**
   - Implement logistic regression for categorization
   - Fine-tune with manual category mapping

3. **Risk Factor Analysis**
   - Process environmental indicators:
     - Code violations
     - Lot abatements
     - Market value assessments
     - Streetlight outages
     - Abandoned vehicles

4. **Census Integration**
   - Include demographic variables:
     - Population density
     - Median income
     - Poverty rates
     - Unemployment rates
     - Vacancy rates
     - Renter rates

5. **Statistical Analysis**
   - Correlation matrix between factors and call types
   - Local Moran's I for spatial clustering

## Contact

For questions or spatial file access, please contact: cburru2@gmail.com