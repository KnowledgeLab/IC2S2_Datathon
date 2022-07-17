![](./src/ic2s2_logo.png.webp)![](./src/knowledge_lab.png)

![](./src/ic2s2_bg.png)
# IC2S2_Datathon

Hi, Paticipants of #2022-IC2S2-Datathon,

Welcome to the Data Repo of 8th IC2S2,2022!

We provide the following datasets for you to explore. some datasets are privite, you can only download the data on game day.


## 1.Meta Business Data:
### About Data
The goal of the Business Activity Trends project is to provide humanitarian organizations and researchers with dataabout business recovery from disruptive events all over the world.  As noted above, our development of BusinessActivity Trends was inspired by the work of Eyre, De Luca, and Simini(referred to as EDS from here on out). Theseauthors propose and validate a methodology for using business social-media activity to measure business downtime andrecovery following natural disasters. Their approach leverages aggregate posting behavior of Facebook business pages,which are instances of Facebook’s Pages product that are owned and operated by businesses. They hypothesize thatposting to Facebook business pages will be affected by disruptive events (such as natural disasters) and that this changecan be leveraged as a proxy measurement of the state of business sectors.

We encourage you to look at our attached white paper for more information on the data andpotential use cases. We have provided separate files in csv formatfor the years 2020 (beginning2020-03-01), 2021, and 2022 (up to 2022-06-29). Additionally, we have created versions of the data that aggregate all businesses in a county (all_agg) and disaggregate by business verticals (verticals). We highly suggest using the verticals version asaggregating all businesses tends to miss out on a lot of heterogeneity across economicsectors.

the properties are contained in our dataset
- gadm_id: The GADM id of the polygon
- gadm_county_name:The county name (GADM level 2)
- gadm_state_name: The state name (GADM level 1)
- business_vertical: The business vertical of the aggregation.
- activity_percentage: The 7-day rolling sum of totalactivity (i.e., total posts) as a percentof the average weekly baseline average. 
- activity_quantile: The level of activity as a quantilerelative to the baseline period. 
- lat: The latitude of the center of the polygon
- lon:The longitude of the center of the polygon
- ds:The date of the activity provided in YYYY-MM-DDformat defined by Pacific Time


click [here](./dataset/Meta_Business) for more details.

## 2.Proquest News Data:
### About Data
These datasets are made from ProQuest US Newsstream using ProQuest TDM Studio. Below are a few notes which may be helpful when using the datasets.

- US Newsstream Metadata ALL

This csv file contains metadata for all of the newspaper articles. It also includes a selection of metadata fields detailed here. 

[GOID] This can be treated as a unique identifier for the newspaper article.
[Publication Location] This is the location of where the newspapers is published (e.g. Chicago, New York)
[Publication Title] This is the title of the newspaper.
[Author Name(s)] These are the author(s) of the newspaper article. Some of the most prolific authors appear to be: Marni Pyke, Joseph Spector...
[Document Type] This is the type of the newspaper article--These will vary by newspaper article. Some of the most common types in this metadata file are: News, Blogs, Feature, Obituary, Opinions, Editorial...


- US Newsstream Month-Level All

This set of csv files includes all of the available publication titles within US Newsstream and all of the word counts for each article. 
This dataset was created by selecting all newspaper articles (https://about.proquest.com/en/products-services/nationalsnews_shtml/) which have the term 'covid' in the full text. The possible date range is from January 1st, 2019 to July 12th, 2022.

click [here](./dataset/Proquest_News) for more details.

## 3.SafeGraph Mobility:

click [here](./dataset/SafeGraph_Mobility) for more details.

## 4.Covid Cases:


### About Data

The Covide Cases Data is provided by NewYorkerTime.
It contains the daily cumulative number of cases and deaths reported in each county and state across the U.S. since the beginning of the pandemic.
It also includes the additional data sets: 
- Prisons: Cases in prisons
- Colleges: Cases on college and university campuses.
- Excess deaths: The elevated overall number of deaths during the pandemic.
- Mask use: A July 2020 survey of how regularly people in each county wore masks.
- Averages and anomalies: A set of pre-computed rolling averages of cases and deaths for ease of analysis or use in making graphics, along with a set of days with anomalous data that have been excluded from the averages.

you can find the whole intro in their github repo, https://github.com/nytimes/covid-19-data.git

click [here](./dataset/Covid_Cases) for more details.
## 5.Urban Region Information
### About Data
We provide the data with the following properties...
- Gender
- Age
- Household Income
- Occupation & Commuting
- Race/ethnicity
- Education
- Housing and living conditions
- Health 
- 
click [here](./dataset/Urban_Region) for more details.
