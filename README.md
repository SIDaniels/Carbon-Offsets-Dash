# Trends in the Voluntary Carbon Offset Market 
## Abstract
There is a new awakening of climate action in the corporate world. Investors, customers, and regulators have built momentum in pressuring companies to make pledges to target “net zero” emission in the coming decades. Achieving net zero requires negating anthropogenic greenhouse gas (GHG) emissions through avoidance (i.e., modifying company operations) or through “offsetting” the emissions by funding the reduction and removal of GHG from the atmosphere. The accounting process for offsetting GHG is usually in carbon-based units, as carbon dioxide is the GHG with the highest atmospheric concentrations and is directly associated with warming of the planet. Therefore, for every metric ton of carbon released by a company, an equivalent metric ton of carbon can be offset through carbon reduction/removal projects to ultimately attain a net zero target. Total metric tons of reduced/removed carbon are estimated for each carbon offset project and exchanged 1:1 as carbon credits within the so-called “voluntary market.” Within this voluntary market, credit allocations from each verified project is placed on sale (i.e., “issued”)  and can be purchased (i.e., “retired”) by GHG emitting entities. 

## Design
The voluntary carbon market has four major carbon registries that all have three main objectives: 
1) develop eligibility criteria for accepting new projects
2) assign third-party validators to verify the project’s methods
3) issue the carbon credits for accepted projects and track them throughout their lifetime on the market
UC Berkeley’s Carbon Trading Project has consolidated all project activity from these four registries into [a database](https://gspp.berkeley.edu/faculty-and-impact/centers/cepp/projects/berkeley-carbon-trading-project/offsets-database), which includes specific dates (i.e., the year the project began, the year the carbon credits were issued and retired)  as well as specific aspects of the project (i.e., number of carbon credits allocated to the project, the project scope, the country/state). 
Even though each carbon credit is considered equal in value, unfortunately the quality and caliber of each carbon offset project varies and, therefore, more desirable credits tend to be those that are associated with higher quality projects. The research team included categorical features to help infer a project’s relative quality.  For example, one feature describes the project activity; “temporary removal,” “reduction”, or “mixed.” Removal efforts are superior to reduction efforts because carbon is taken from the atmosphere (i.e., reforestation) as opposed to simply reducing the amount of emissions (i.e., preventing deforestation). In another example, there’s been heightened interest from the California Air and Resource Board (ARB) to migrate high-quality carbon credits into this highly-regulated “compliance market.” Projects (specifically those in the American Climate Registry and Climate Action Reserve Registry) that have passed a certain threshold of quality and moved to ARB thus far have been tagged by the researcher team as well. 
While there is no necessity for carbon offset projects to be within proximity to the source of the greenhouse gas emissions, certain countries/states that have greater emissions may have more motivation to produce meaningful offset projects. Therefore, a second data set on annual fossil CO2 emissions per country was obtained from the Global Carbon Project for 2019 and state-level, energy-related carbon dioxide  emissions (accounting for 84% of total carbon emissions in the US) from 2019 was obtained from the US Energy and Information Administration.
While there is no necessity for carbon offset projects to be within proximity to the source of the greenhouse gas emissions, certain countries/states that have greater emissions may have more motivation to produce meaningful offset projects.  Two additional datasets were acquired to examine the distribution of carbon credits in relation to carbon emissions per location. [Annual fossil CO2 emissions per country](https://zenodo.org/record/5569235#.YxaGAuzMJ9v) was obtained from the Global Carbon Project for 2019 and [state-level, energy-related carbon dioxide emissions](https://www.eia.gov/environment/emissions/state/) was also obtained for 2019 from the US Energy and Information Administration.(Energy-related CO2 emissions account for 84% of total carbon emissions in the US.) 

## Objectives
1) determine locations with greatest potential for an influx of carbon credits supply to meet the growing demand based on national and global trends in issuances and retired credits
2) Identify project scopes with growing popularity based on national and global trends in issuances and retired credits
3) Find most probable characteristics of high quality projects

## Data
The original Voluntary Carbon Offset dataset from UC Berkeley’s Carbon Trading Project was in wide format and contained 6081 projects with 148 features. The dataset includes variables on the voluntary registry for the project, project location (world region, country, and, if relevant, state and exact locale), project developer, project scope, detail on project type and methodology used, as well as carbon credits issued/registered/retired each year (since 1996). Data on the global and U.S. CO2 emissions were filtered for only year 2019.

### Data Cleaning
Data cleaning was limited to data transformation (from wide to long) for the voluntary carbon market registry data and some manually resolving of country names to merge country/state level carbon emission data with the voluntary carbon market registry data. After transforming the data to long format there were 17 categorical variables and 6 continuous variables of potential interest. As 2457 projects listed had no carbon credits issued yet, a remaining 3624 entries for projects were used for years 2011 to 2020. 
### Aggregation
For overall annual trends of carbon credits issued, annual credits were aggregated by scope and voluntary registry. For annual global or national dashboards, carbon credits issued were aggregated across particular locations, given the project scope, type, contributions to carbon reductions or removal, and ARB status. 
### Visualization
Several interactive dashboards were created using Tableau public; 
1) General trends in carbon credit from 2011 to 2020 issued by scope and registry [here](https://public.tableau.com/app/profile/sarah8808/viz/TrendsinCarbonIssuedbyRegistryScope/Dashboard15)

2) Global trends from 2011 to 2020- by country, partitioned by scope, type (subset of project scope) and carbon reduction/removal projects
	a) Reported carbon credits issued (placed on the market)  [here](https://public.tableau.com/app/profile/sarah8808/viz/GlobalDistributionofCarbonCreditIssuance/CarbonCredIssued#2)
	b) Reported carbon credits retired (sold to GHG emitting entity) [here](https://public.tableau.com/app/profile/sarah8808/viz/GlobalDistributionofCarbonCreditsRetired/CarbonCredRetired)

3) U.S. trends in from 2011-2020
	a) Reported carbon credits issued (placed on the market) [here](https://public.tableau.com/app/profile/sarah8808/viz/GlobalDistributionofCarbonCreditIssuance/CarbonCredIssued)
	b) Reported carbon credits retired (sold to GHG emitting entity) [here](https://public.tableau.com/app/profile/sarah8808/viz/U_S_DistributionofCarbonCreditRetired/U_S_CarbonCredRetired)


## Tools

- Python (Pandas)
- Google Spreadsheets
- Tableau
