### ACMT Information Page

**ACMT Installation and Architecture**

The ACMT and its dependencies are available on GitHub. The ACMT is packaged to be run using Docker, a technology that lets developers package and run virtual machines within another computing environment. 

The ACMT comprises two components: (1) a local geocoder, which identifies a latitude and longitude given a US street address and (2) a context measure assembler, which computes measures from publicly available data sources linked to a latitude and longitude. ACMT users access both of these components using an RStudio/RShiny-based web interface that is hosted within the Docker container.
 
Figure 1 below shows the flow of data in a typical use of the ACMT. First, a data analyst points their browser to the web interface (accessing the Docker container on their local machine). The R environment will be running in the web interface using RStudio/RShiny, depending on analyst preference. That R environment hosts logic that can convert an address (limited to the United States) to its corresponding latitude and longitude (the geocoder) and can download public data from the Internet to compile environmental context measures for a latitude and longitude (the context measure assembler). The address conversion is performed using the locally installed geocoder, thus preserving privacy. The analyst can then work with these context measures directly in the RStudio interface or can export them for use with other statistical software. The components are described in more detail below.

<img width="468" height="287" alt="image" src="https://github.com/user-attachments/assets/d2d77ab9-f53d-41e7-91c4-c402b8beb82a" />

**Datasets currently available in the ACMT**

The following datasets are currently set up in the ACMT: 
   -  [The American Community Survey](https://www.census.gov/programs-surveys/acs/about.html)
   -  [Walkability Index](https://www.epa.gov/smartgrowth/smart-location-mapping#walkability)
   -  [CDC PLACES data](https://www.cdc.gov/places/index.html)
   -  [National Land Cover Database](https://www.usgs.gov/centers/eros/science/national-land-cover-database)
   -  [Modified Retail Food Environment Index (mRFEI)](https://www.cdc.gov/obesity/downloads/census-tract-level-state-maps-mrfei_TAG508.pdf)
   -  [Trust for Public Lands' ParkServe](https://www.tpl.org/parkserve)
   -  [Sidewalk Score](https://journals.sagepub.com/doi/10.1177/0033354920968799)
   -  [Regional Price Parity](https://www.bea.gov/data/prices-inflation/regional-price-parities-state-and-metro-area)
   -  [Gentrification Measure](https://drexel.edu/uhc/resources/briefs/Measure-of-Gentrification-for-Use-in-Longitudinal-Public-Health-Studies-in-the-US/)

*Additional datasets may be added to the ACMT for use in generating environmental measures*

**Installation overview**
1. [Install Docker Desktop Software](https://docs.docker.com/desktop/setup/install/windows-install/)
2. [Download ACMT code frrom github repository](https://github.com/aybloom/acmt-network)
3. Run docker compose scripts to build ACMT Docker containers.
4. Run Rstudio in the ACMT Docker container (accessed via browser)
5. In Rstudio, runt he ACMT shiny app and follow the steps to generate geocodes and environmental measures for your dataset. 

**[Step-by-step installation instructions](https://aybloom.github.io/acmt-instructions/acmt_setup/ACMT-setup.html)**

### Support or Contact. 
If you run into any issues along the way, reach out to [Amy](mailto:aybloom@uw.edu)
