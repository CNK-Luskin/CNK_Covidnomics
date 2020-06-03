[UCLA Center for Neighborhood Knowledge](http://knowledge.luskin.ucla.edu) <br />
COVID-nomics <br /> 
Project Documentation 

# About this project:

As part of the CNK "covid-nomics" research series, this map room visualizes how different communities in and around Los Angeles County are impacted by COVID-19. The project draws on data and research conducted during the COVID-19 pandemic by the UCLA Center for Neighborhood Knowledge, in partnership with Ong & Associates, the UCLA Latino Policy & Politics Initiative, the UCLA Ziman Center for Real Estate, and the UCLA Institute on Inequality & Democracy. The resulting [research briefs](http://knowledge.luskin.ucla.edu/news) show that different communities across the Los Angeles area are disproportionately burdened by the epidemic and face greater risks of income insecurity, job displacement, and hardship.

## How it works:

The map includes six different layers:

* Covid-19 Cases per 100K (as of May 14, 2020)
* Proportion of Workers at High Risk of Job Displacement
* Proportion of Workers not Covered by Unemployment Insurance
* Proportion of Individuals Unlikely to Receive CARES Act Individual Rebate
* Shelter-in-Place Burden Index
* Renter Vulnerable Neighborhood Index

The web map was built using Carto.Js and Leaflet to integrate data stored in the “uducla” CARTO account with interactive features built outside of the CARTO environment. The developer used an online programming environment, Glitch.com, to develop the interactive web map. The maproom on the [UCLA CNK webiste](http://knowledge.luskin.ucla.edu/news) is made possible through a grant from mapping platform, Carto.

## Data description and sources:

#### Proportion of Workers at High Risk of Job Displacement
This layer shows the proportion of workers in sectors that have been particularly hard hit by the closure of businesses due to the outbreak of COVID-19 - sales workers in retailing, service workers in hospitality, and workers in personal care and service occupations.

#### Proportion of Workers not Covered by Unemployment Insurance
The non-UI coverage layer includes estimates of workers that are excluded from the UI program. This includes low-wage workers and immigrants who do not qualify such as those that are undocumented that are currently prohibited from collecting UI, even though their employers may have contribute payments to the UI funds.

#### Shelter-in-Place Burden Index
The SIPB includes three variables that measure the relative difficulty or ease of complying with countywide shelter-in-place mandates: (1) the population density in an area (densely populated neighborhoods increases the odds and frequency of encountering people thereby decreasing the chances of maintaining social distancing); (2) availability of public-park space per person; and, (3) the relative number of households without access to a nearby supermarket.

#### Proportion of Individuals Unlikely to Receive CARES Act Individual Rebate
The layer in the map estimates the proportion of individuals in each neighborhood that are least likely to receive a CARES Act individual rebate. This information is reported at the ZCTA‒level (zip-code tabulation area, as defined by the U.S. Census Bureau) for all of Los Angeles County ZCTAs and estimated using a combination of 2017 IRS Statement of Income data and the 2013‒2017 5-year ACS.

#### Renter Vulnerable Neighborhood Index
The Renter Vulnerable Neighborhood Index is a composite of three dimension to identify vulnerable neighborhoods: (1) those with a disproportionate large number of renters on the edge of financial vulnerability due to high housing cost burden; (2) with a disproportionate large number of workers vulnerable to job displacement due to retail and service-sector closures; and (3) with a disproportionate number of people excluded from the federal Coronavirus Aid, Relief and Economic Security Act, known as the CARES Act.

Visit knowledge.luskin.ucla.edu/news to view the research briefs for more information on methodology.

## Data storage

The statistical and spatial analysis conducted draws on three geographies (census tracts, ZCTAs, and LA County Department of Public Health Communities ), and is therefore stored in three separate shapefiles: covid_nomics_tracts_v01, covid_nomics_zctas_v01, and lac_covidcases_may14th.

Each shapefile was zipped and uploaded to the “uducla” CARTO account as a dataset. Within the CARTO account, the developer turned these datasets into maps in order to do some initial styling using CartoCSS.

The rest of the webmap was built on an external site outside of the CARTO environment to add and style interactive features. Since the data remains stored in the “uducla” CARTO account, it is imperative to not remove nor rename any of the three datasets mentioned above from the uducla CARTO account in order for the web map to continue being able to pull and visualize data stored in these datasets (covid_nomics_tracts_v01, covid_nomics_zctas_v01, and lac_covidcases_may14th). However, data within each dataset can be added, edited, or removed, and the map will automatically update (ex: adding a row of data, or editing an existing cell).

## Interactivity

The following interactive features were added through custom code:

> > Dropdown menu to view different layers: the drop-down menu uses a simple “if/else” logic to display the correct layer (ex: if user selects “Proportion of Workers At High Risk of Job Displacement” from the drop-down menu, add that layer, otherwise, remove it)

> > Dynamic legends: similarly to the drop-down menu, the dynamic legends uses an “if/else” logic to hide or display legends based on the layer selected

> > Toggle buttons: Hide or show City Council and County Districts on click

> > Pop-up window: on the default layer (COVID-19 cases), an event listener was added to display the name of the community when the user clicks on a feature).

Troubleshooting: if any development issues arise, feel free to contact the developer, Manon Vergerio, at manonvergerio@gmail.com. General inquiries about the project can be directed to knowledge@luskin.ucla.edu.
