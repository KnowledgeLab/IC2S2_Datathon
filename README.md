# IC2S2_Datathon

Hi, Paticipants of #2022IC2S2Datathon,

Welcome to our Data repo!
We provide the following datasets for you to explore.For each dataset
some datasets are privite, you can only download the data on game day.


## Meta Business Data:
The goal of the Business Activity Trends project is to provide humanitarian organizations and researchers with dataabout business recovery from disruptive events all over the world.  As noted above, our development of BusinessActivity Trends was inspired by the work of Eyre, De Luca, and Simini [4] (referred to as EDS from here on out). Theseauthors propose and validate a methodology for using business social-media activity to measure business downtime andrecovery following natural disasters. Their approach leverages aggregate posting behavior of Facebook business pages,which are instances of Facebook’s Pages product that are owned and operated by businesses. They hypothesize thatposting to Facebook business pages will be affected by disruptive events (such as natural disasters) and that this changecan be leveraged as a proxy measurement of the state of business sectors.

## Proquest News Data:
### About Data
These datasets are made from ProQuest US Newsstream using ProQuest TDM Studio. Below are a few notes which may be helpful when using the datasets.

US Newsstream Metadata ALL

This csv file contains metadata for all of the newspaper articles. It also includes a selection of metadata fields detailed here. 

[GOID] This can be treated as a unique identifier for the newspaper article.
[Publication Location] This is the location of where the newspapers is published (e.g. Chicago, New York)
[Publication Title] This is the title of the newspaper.
[Author Name(s)] These are the author(s) of the newspaper article. Some of the most prolific authors appear to be: Marni Pyke, Joseph Spector...
[Document Type] This is the type of the newspaper article--These will vary by newspaper article. Some of the most common types in this metadata file are: News, Blogs, Feature, Obituary, Opinions, Editorial...


US Newsstream Month-Level All

This set of csv files includes all of the available publication titles within US Newsstream and all of the word counts for each article. 

This dataset was created by selecting all newspaper articles (https://about.proquest.com/en/products-services/nationalsnews_shtml/) which have the term 'covid' in the full text. The possible date range is from January 1st, 2019 to July 12th, 2022.


How to cite this dataset:

ProQuest, TDM Studio US Newsstream Dataset, [Unpublished Raw Data]. ProQuest Part of Clarivate
## SafeGraph Mobility Data:

## Covid Cases:

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


## Location Information
### About Data
- Gender
【female_population】B01001e26: Female
- Age
【0_to_9_years_old】B01001e3,B01001e4,B01001e27,B01001e28: 0-9 years old
【10_to_19_years_old】B01001e5,B01001e6,B01001e7,B01001e29,B01001e30,B01001e31: 10-19 years old
【20_to_29_years_old】B01001e8,B01001e9,B01001e10,B01001e11,B01001e32,B01001e33,B01001e34,B01001e35: 20-29 years old
【30_to_39_years_old】B01001e12,B01001e13,B01001e36,B01001e37: 30-39 years old
【40_to_49_years_old】B01001e14,B01001e15,B01001e38,B01001e39: 40-49 years old
【50_to_59_years_old】B01001e16,B01001e17,B01001e40,B01001e41: 50-59 years old
【60_to_69_years_old】B01001e18,B01001e19,B01001e20,B01001e21,B01001e42,B01001e43,B01001e44,B01001e45: 60-69 years old
【70_to_79_years_old】B01001e22,B01001e23,B01001e46,B01001e47: 70-79 years old
【80_years_old_and_older】B01001e24,B01001e25,B01001e48,B01001e49: 80+ years old
- Household Income
【total_households】B19001e1: Total Households
【households_whose_annual_income_less_than_10000_dollars】B19001e2: Households whose annual income less than 10000 dollars
【households_whose_annual_income_between_10000_and_50000_dollars】B19001e3, B19001e4, B19001e5, B19001e6, B19001e7, B19001e8, B19001e9, B19001e10: Households whose annual income between 10000 and 50000 dollars
【households_whose_annual_income_between_50000_and_200000_dollars】B19001e11, B19001e12, B19001e13, B19001e14, B19001e15, B19001e16: Households whose annual income between 50000 and 200000 dollars
【households_whose_annual_income_greater_than_200000_dollars】B19001e17: Households whose annual income greater than 200000 dollars

- Occupation & Commuting
【total_workforce】B23025e1: Workforce (Population 16 Years And Over)(at an age that is suitable to work)
【workforce_in_labor】B23025e2: In Labor Force (actually has a job)
【healthcare_worker】C24030e23, C24030e50: Health Care Worker
【commuting_by_car_or_truck_or_van】B08134e11: Going to work by Car, Truck, Or Van
【commuting_by_public_transportation_except_taxicabs】B08134e61: Going to work by public transportation (except taxicabs)
【commuting_by_walk】B08134e101: Going to work by walk
【commuting_by_taxicab_or_motorcycle_or_bicycle_or_other_means】B08134e111: Going to work by Taxicab, Motorcycle, Bicycle, Or Other Means
【commuting_time_less_than_20_minutes】B08303e2, B08303e3, B08303e4, B08303e5: Travel time to work less than 20 minutes
【commuting_time_between_20_and_60_minutes】B08303e6, B08303e7, B08303e8, B08303e9, B08303e10, B08303e11: Travel time to work between 20 and 60 minutes
【commuting_time_over_60_minutes】B08303e12, B08303e13: Travel time to work over 60 minutes
- Race/ethnicity
【white】B02001e2: White
【black_or_african_american】B02001e3: Black or African American
【american_indian_and_alaska_native】B02001e4: American Indian and Alaska Native
【asian】B02001e5: Asian
【non_hispanic_white】B03002e3: Non-Hipanic White
【hispanic_or_latino】B03002e12: Hispanic or Latino
- Education
【no_schooling_completed】B15002e3, B15002e20: No-schooling completed
【high_schooling_graduate】B15002e11, B15002e28: High School Graduate (Includes Equivalency)
【bachelor's_degree】B15002e15, B15002e32: Bachelor's Degree
- Housing and living conditions
【occupied_housing_units】B25037e1: Occupied Housing Units
【owner_occupied_housing_units】B25037e2: Owner Occupied Housing Units (the rest are renter occupied)

- Health 
【no_health_insurance_covered】B27010e17, B27010e33, B27010e50, B27010e66: No Health Insurance Covered

