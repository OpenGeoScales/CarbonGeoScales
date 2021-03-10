> This document presents the CarbongeoScales project: A framework for standardizing available GHGs emissions data at multiple geographical sclaes. A complementary technical report presenting a comprehensive cartography of GHGs emissions open data with our first explorations and modeling is available [in this link](https://opengeoscales.github.io/CarbonData/).
>
> Key words: `Open Data`, `Geospatial scales`, `Climate Change`, `GHG emissions`, `Standardization`, `Open Source`
>
> Author and project manager: [Saif Shabou](https://saif-shabou.netlify.app/)
> 
> Date: 10/03/2021
> 


## Context

Environmental issues are becoming increasingly important in public policies as well as in our daily life. Knowledge of the state of our planet and the assessment of climate impa t impact of human activities require **free and easy access to reliable, accurate, aggregated and documented data**.
While several open data platforms and portals are engaged in publishing relevant environnmental data (air quality, greenhouse gas emissions, natural hazards, energy resources...), the use of this data remain oftne complex and tedious, especially for non-data specialist. Identification and mapping of the different sources as well as cleaning, recoding, normalization, cross-referencing, consolidation and aggregation at different geographic scales is often necessary before being able to use the available data.

To remedy these difficulties, as part of the OpenGeoScales project, we are proposing to build **a centralized access point to standardized and aggregated environmental data at different geographic scales**. In addition to providing reliable and standardized environmental data, OpenGeoScales offers **free access to processing** implemented on raw data collected from various sources and aims to federate **an open source community** participating in the production of data and tools needed to explore them.

## CarbonGeoScales project

Greenhouse gas (GHGs) emissions from human activities are considered as the most significant driver of observed climate change since the mid-20th century. In order to better mitigate climate change impacts, policy makers, scientists, carbon and environment consultancy specialists, data journalists and citizens need easy free access to relevant and accurate data on GHGs emissions at various spatial scales.
In accordance with the Paris Agreement, countries are required to submit transparent, comparable and complete reporting of GHGs inventories based on the methodologies developed by the IPCC. In addition to these Top-Down approaches, Bottom-Up methods are being used for completing emissions estimates based on satellite imagery and carbon monitoring stations at different spatial scales. At subnational scales, important efforts and specific protocols are deployed for measuring city emissions since they represent a large percent of energy-related GHGs emissions.
The collected GHGs emissions datasets are shared through multiple open data platforms built by different organisms. However, it remains complex and time consuming to use it and combine it due to different formats, standards, scales, protocols, units, data definitions… 

### Objective

The main goal of CarbonGeoScales consists of **providing a centralized access point to accurate, harmonized, and aggregated GHGs emissions data at multiple geographical scales**. As an open source and collaborative project, different data processing treatments are accessible in order to inform users on transformation and cleaning and transformation processes implemented on raw collected data. The resulting compiled database is accessible by download and through specific API for querying and integrating aggregated data into potential applications. Resulting harmonized GHGs emissions data are completed with consistent documentation, articles and dashboard for exploring its content.
By facilitating access to GHGs emissions open data, CarbonGeoScales is participating to help policy makers to build more effective emissions reduction strategies at different territorial scales and to track their progress more accurately. 

### Outputs

### Used datasets

Data provider | Description | Geoscale | Data sources | Access |
---|---------|---|---| ---| 
The World Bank | The World Bank Group publishes various indicators on world development through its [open data platform](https://data.worldbank.org/). Provided aggregated [GHG emissions data](https://data.worldbank.org/indicator/EN.ATM.GHGT.KT.CE) is based on the Emission Database for Global Atmospheric Research (EDGAR)   | `World scale` <br /> `Country scale` | `EDGAR`| [Get data](https://data.worldbank.org/indicator/EN.ATM.GHGT.KT.CE) | 
The World Resources Institute (WRI) | The World Resources Institute compiles various sources of GHG emissions and provide access to this data through a specific tool: [CLIMAT WATCH](https://www.climatewatchdata.org/data-explorer/historical-emissions?historical-emissions-data-sources=cait&historical-emissions-gases=&historical-emissions-regions=&historical-emissions-sectors=&page=1). Provided [GHG emissions data](https://www.climatewatchdata.org/data-explorer/historical-emissions?historical-emissions-data-sources=cait&historical-emissions-gases=&historical-emissions-regions=&historical-emissions-sectors=&page=1) is based on various data sources: CAIT database, UNFCCC, PIK.  | `World scale` <br /> `Country scale`|  `CAIT` `UNFCCC` `PIK`  | [Get data](https://www.climatewatchdata.org/data-explorer/historical-emissions?historical-emissions-data-sources=cait&historical-emissions-gases=&historical-emissions-regions=&historical-emissions-sectors=&page=1) |
The United Nations Framework Convention on Climate Change (UNFCCC) | The UNFCCC compiles and shares national annual greenhouse gases inventories submitted in accordance with with the reporting requirements adopted under the Climate Change Convention | `World scale` <br />  `Country scale`| `UNFCCC` | [Get data](https://di.unfccc.int/time_series) |
Potsdam Institute for Climate Impact Research (PIK) | The Postdam Institute provides the **PRIMAP-hist dataset**, which combines several published datasets to create a comprehensive set of greenhouse gas emission pathways for every country and Kyoto gas covering the years 1850 to 2017, and all UNFCCC (United Nations Framework Convention on Climate Change) member states, as well as most non-UNFCCC territories.| `World scale` <br /> `Country scale`| `UNFCCC` `EDGAR`  |[Get data](https://dataservices.gfz-potsdam.de/pik/showshort.php?id=escidoc:4736895) |
The Joint Research Center of Euorpean Commission | The Joint Research center produces the Emission **Database for Global Atmospheric Research (EDGAR)**. EDGAR provides independent estimates of the global anthropogenic emissions and emission trends, based on publicly available statistics, for the atmospheric modeling community as well as for policy makers. This scientific independent emission inventory is characterized by a coherent world historical trend from 1970 to year x-3, including emissions of all greenhouse gases, air pollutants and aerosols. Data are presented for all countries, with emissions provided per main source category, and spatially allocated on a 0.1x0.1 grid over the globe  | `World scale`  <br />  `Country scale`  <br />  `Grid scale`| `EDGAR` | [Get data](https://data.jrc.ec.europa.eu/collection/edgar) |
The Organization for Economic Co-Operation and Development (OECD) | The OECD publishes datasets presenting trends in man-made emissions of major greenhouse gases and emissions by gas. | `OECD scale` <br /> `Country scale`|`UNFCCC`|   [Get data](https://stats.oecd.org/Index.aspx?DataSetCode=AIR_GHG) |
European Environmental Agency (EEA) | The EEA compiles and provides data on greenhouse gas emissions and removals, sent by countries to UNFCCC and the EU Greenhouse Gas Monitoring Mechanism (EU Member States).| `Europe scale` <br /> `Country scale`| `UNFCCC`| [Get data](https://www.eea.europa.eu/data-and-maps/data/national-emissions-reported-to-the-unfccc-and-to-the-eu-greenhouse-gas-monitoring-mechanism-16) |
Eurostat | Eurostat (European Statistical Office) is a Directorate-General of the European Commission. It provides statistical information to the institutions of the European Union (EU) such as a comprehensive set of climate change-related data including GHG emissions statistics. Eurostat maintains a [data portal](https://ec.europa.eu/eurostat/databrowser/view/sdg_13_10/default/table?lang=en) for exploring emissions data. | `Europe scale` <br /> `Country scale`| `EEA` `UNFCCC`| [Get data](https://ec.europa.eu/eurostat/web/climate-change/data/database) |
Our World In Data | Our WOrld In Data compile, maintain and shares CO2 and GHG emissions data. It is updated regularly and includes data on CO2 emissions (annual, per capita, cumulative and consumption-based), other greenhouse gases, energy mix, and other relevant metrics. | `World scale` <br /> `Country scale`| `GCP` <br /> `CAIT` |[Get data](https://github.com/owid/co2-data) |
Global Carbon Project (GCP) | GCP is a global research project that seeks to quantify global greenhouse gas emissions and their causes. It provides data on carbon fluxes resulting from human activities and natural processes and a platform to explore and visualize the most up-to-date data ([Gloabl carbon Atlas](http://www.globalcarbonatlas.org/en/content/welcome-carbon-atlas)) | `World scale`<br />`Country scale`<br /> `City scale`| `GCP` |[Get data](https://www.globalcarbonproject.org/carbonbudget/20/data.htm) |
Carbon Disclosure Project (CDP) | The CDP is an international non-profit organisation that helps companies and cities disclose their environmental impact and GHG emissions. CDP provides [an open data protal](https://data.cdp.net/) for exploring companies and city-wide collected data. | `City scale`| `CDP` | [Get data](https://data.cdp.net/browse?category=Emissions)|

## Users

CarbonGeoScales aims at providing various GHGs emissions data users profiles with consistent and harmonized open data:

- **Data journalists** specialized in climate change issues who need ...
- **Policy makers** for better mitigating climate actions in various scales
- **Scientists** working in downscaling GHGs emissions estimates 
- **Carbon consultancy specialists** for better accounting carbon footprint
- **NGOs**


## Contributers

CarbonGeoScales is a collaborative project open to contribution from every person interested in GHGs emissions data modeling and processing depending on their expertise:

- **Data experts::
- **GHGs emissions use case experts**
- **Scientists**

## Roadmap


## Partnerships



## Project management
