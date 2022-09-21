# Trends in the Voluntary Carbon Offset Market 
## Abstract
There is a new awakening of climate action in the corporate world. Investors, customers, and regulators have built momentum in pressuring companies to make pledges to target “net zero” emission in the coming decades. Achieving net zero requires negating anthropogenic greenhouse gas (GHG) emissions through avoidance (i.e., modifying company operations) or through “offsetting” the emissions by funding the reduction and removal of GHG from the atmosphere. The accounting process for offsetting GHG is usually in carbon-based units, as carbon dioxide is the GHG with the highest atmospheric concentrations and is directly associated with warming of the planet. Therefore, for every metric ton of carbon released by a company, an equivalent metric ton of carbon can be offset through carbon reduction/removal projects to ultimately attain a net zero target. Total metric tons of reduced/removed carbon are estimated for each carbon offset project and exchanged 1:1 as carbon credits within the so-called “voluntary market.” Within this voluntary market, credit allocations from each verified project is placed on sale (i.e., “issued”)  and can be purchased (i.e., “retired”) by GHG emitting entities. It is important to note that any carbon credit project placed on the market must satisfy the terms of **additionality** - that the project would not be funded through alternative means outside of the carbon credit offset market. 

## Objectives
1) Determine locations with greatest potential for an influx of carbon credits supply to meet the growing demand based on national and global trends in issuances and retired credits
2) Identify project scopes with growing popularity based on national and global trends in issuances and retired credits
3) Find most probable characteristics of high quality projects

## Main Findings at a Glance
Worldwide, carbon offset projects are mainly located in the countries contributing the majority of carbon dioxide emissions- U.S., China, India, Indonesia, and Brazil. The types/scopes of projects are location specific, as Land Use and Reforestation projects are more common in the U.S., Brazil, Africa, and Southeast Asia, while Renewable Energy projects (generally wind and hydropower) are commonly found in India and Turkey. Brazil, China, and the U.S. to some extent, have more diverisifed carbon offset project portfolios. Overall very few projects qualify as the higher quality "carbon removal," which are specifically for either afforestation or reforestation projects.

In U.S., carbon offset projects are predominantly issued along the West and East Coasts (including Alaska) and the South, with the most common project scope being Land Use and Reforestation in recent years. The vast majority of these project credits were transferrable to the ARB (indicating higher quality). Previously there was a substantial number of projects in Chemical Processes and Waste Management, particularly in the South and Eastern states. 


<details>
  <summary><h2>Background/Design</h2></summary>

### Main Dataset
UC Berkeley’s Carbon Trading Project has consolidated all project activity from  four registries into [a database](https://gspp.berkeley.edu/faculty-and-impact/centers/cepp/projects/berkeley-carbon-trading-project/offsets-database), which includes specific dates (i.e., the year the project began, the year the carbon credits were issued and retired)  as well as specific aspects of the project (i.e., number of carbon credits allocated to the project, the project scope, the country/state). The voluntary carbon market has four major carbon registries that all have three main objectives: 
- Develop eligibility criteria for accepting new projects
- Assign third-party validators to verify the project’s methods
- Issue the carbon credits for accepted projects and track them throughout their lifetime on the market

Even though each carbon credit is considered to have equivalent values, unfortunately the caliber of each carbon offset project varies, and therefore more desirable credits tend to be those associated with "higher quality" projects. The Carbon Trading Project research team included two categorical features to help infer a project’s relative quality.  
**Project Activity** -  This is defined as either “temporary removal,” “reduction”, or “mixed.” Removal efforts are superior to reduction efforts because carbon is taken from the atmosphere (i.e., reforestation) as opposed to simply reducing the amount of emissions (i.e., preventing deforestation). 
**California Air and Resource Board (ARB) Credits**  -  For the U.S. specifically, there’s been heightened interest from theto migrate high-quality carbon credits into this highly-regulated “compliance market.” Projects (specifically those in the American Climate Registry and Climate Action Reserve Registry) that have passed a certain quality threshold and moved to the ARB thus far have been tagged by the researcher team as well. 

### Additional Datasets
While there is no necessity for carbon offset projects to be within proximity to the source of the greenhouse gas emissions, certain countries/states that have greater emissions may have more motivation to produce meaningful offset projects.  Two additional datasets were acquired to examine the distribution of carbon credits in relation to carbon dioxide emissions per location. [Annual fossil CO2 emissions per country](https://zenodo.org/record/5569235#.YxaGAuzMJ9v) was obtained from the Global Carbon Project for 2019 and [state-level, energy-related carbon dioxide emissions](https://www.eia.gov/environment/emissions/state/) was also obtained for 2019 from the US Energy and Information Administration.(Energy-related CO2 emissions account for 84% of total carbon emissions in the US.) 
</details>

<details>
  <summary><h2>Data</h2></summary>

The original Voluntary Carbon Offset dataset from UC Berkeley’s Carbon Trading Project was in wide format and contained 6081 projects with 148 features. The dataset includes variables on the voluntary registry for the project, project location (world region, country, and, if relevant, state and exact locale), project developer, project scope, detail on project type and methodology used, as well as carbon credits issued/registered/retired each year (since 1996). Data on the global and U.S. CO2 emissions were filtered for only year 2019.

### Data Cleaning and Aggregation
Data cleaning was limited to data transformation (from wide to long) for the voluntary carbon market registry data and some manually resolving of country names to merge country/state level carbon emission data with the voluntary carbon market registry data. After transforming the data to long format there were 17 categorical variables and 6 continuous variables of potential interest. As 2457 projects listed had no carbon credits issued yet, a remaining 3624 entries for projects were used for years 2011 to 2020. 
For overall annual trends of carbon credits issued, annual credits were aggregated by scope and voluntary registry. For annual global or national dashboards, carbon credits issued were aggregated across particular locations, given the project scope, type, contributions to carbon reductions or removal, and ARB status. 
</details>

## Visualization
Several interactive dashboards were created using Tableau public; 
1) General trends in carbon credit from 2011 to 2020 issued by scope and registry [here](https://public.tableau.com/app/profile/sarah8808/viz/TrendsinCarbonIssuedbyRegistryScope/Dashboard15)

2) Global trends from 2011 to 2020- by country, partitioned by scope, type (subset of project scope) and carbon reduction/removal projects
(a) Reported carbon credits issued (placed on the market)  [here](https://public.tableau.com/app/profile/sarah8808/viz/GlobalDistributionofCarbonCreditIssuance/CarbonCredIssued)
(b) Reported carbon credits retired (sold to GHG emitting entity) [here](https://public.tableau.com/app/profile/sarah8808/viz/GlobalDistributionofCarbonCreditsRetired/CarbonCredRetired)

3) U.S. trends in from 2011-2020
(a) Reported carbon credits issued (placed on the market) [here](https://public.tableau.com/app/profile/sarah8808/viz/U_S_DistributionofCarbonCreditIssuance/U_S_CarbonCredIssuance)
(b) Reported carbon credits retired (sold to GHG emitting entity) [here](https://public.tableau.com/app/profile/sarah8808/viz/U_S_DistributionofCarbonCreditRetired_v2/U_S_CarbonCredRetired)


## Tools
- Python (Pandas)
- Google Spreadsheets
- Tableau
