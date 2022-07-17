
# Meta Business Data
Business Activity Trends measures how local businesses are affected by and recover fromcrisis events using data about posting activity on Facebook. Given the broad presence of smallbusinesses on the Facebook platform, this dataset aims to provide timely estimates of globalbusiness activity without the common limitations of traditional data collection methods, such asscale, speed and nonstandardization. This method for understanding local economic activity,first described by the University of Bristol team and published inNature Communications, isintended to provide humanitarian organizations, researchers and policymakers with a broadview of subnational economic activity after disasters.

#How we measure business activity
Business activity is measured by the volume of posts made by business Pages on Facebook ona daily basis, where a post is defined broadly to include posts, stories and reels created by thebusiness Page anywhere on Facebook. In practice, almost all posts are either made on thebusiness Page itself or in Facebook Groups. The sample of business Pages is fixed at thebeginning and is derived through a set of internal filters to represent quality local businessesPages.

A baseline posting pattern is established using the 365 days prior to the event start date (in thiscase, 2020-03-01 for COVID). We then measure the daily posting activity relative to the expectedposting activity based on the baseline period. Individual business Page activity is thenaggregated by business vertical (proxy for economic sector) and byGADMversion 3.6administrative polygons (geographic units). Data is provided for the US at the county level(GADM level 2).Polygons and business verticals withfewer than 10 active business Pages areexcluded from the dataset for privacy protection.

# How to use the data
We encourage you to look at our attached white paper for more information on the data andpotential use cases.
- Files: We have provided separate files in csv formatfor the years 2020 (beginning2020-03-01), 2021, and 2022 (up to 2022-06-29). Additionally, we have created versionsof the data that aggregate all businesses in a county (all_agg) and disaggregate by
business verticals (verticals). We highly suggest using the verticals version asaggregating all businesses tends to miss out on a lot of heterogeneity across economicsectors.
- Metrics: We have included two main metrics,activity_percentageandactivity_quantile.We suggest usingactivity_quantilesince it is morerobust to outliers, but we includeactivity_percentagefor better interpretability.
- Business churn: Since our sample of businesses isfixed at the beginning, we tend tosee the business activity metrics decrease as time passes simply due to normalbusiness churn. We do not differentiate between normal business churn and churn dueto crisis. We also do not replace businesses in the sample with new businesses thatform after the crisis date. Therefore, we suggest focusing on the 2020 data first to trulyunderstand the extent of COVID-related activity.
- Merging with other geographies:We use GADM v3.6 asour main source ofgeographic aggregation due to its global coverage and standardization. For the US, thegeographic unit used here is the US county. However, you may be interested in usingother geographical units such as zip 
or Metropolitan Statistical Area (MSA). Wehave not found very many reliable crosswalks between GADM and other geographicalunits, but we have had some success matching crosswalks based on county name. Forexample, you may consider usingdelineation filesfrom the US Census Bureau to matchto MSA based on county name. Note that MSAs can contain multiple counties and acounty can also contain multiple MSAs.

# Code book
- gadm_id: The GADM id of the polygon
- gadm_county_name:The county name (GADM level 2)
- gadm_state_name: The state name (GADM level 1)
- business_vertical: The business vertical of the aggregation.Business verticals are defined internally within Facebook from categories selected by the Page admins. We usebusiness verticals as a proxy for local economic sectors. In the all_agg files, businessvertical is the “All” category, which includes but is not limited to all the other businessverticals.
- activity_percentage: The 7-day rolling sum of totalactivity (i.e., total posts) as a percentof the average weekly baseline average. The weekly baseline average is calculated asthe average of the 7-day sum of total activity every Monday within the baseline period.For each day during the crisis, we divide the 7-day rolling sum of total posts by thisweekly baseline average and multiply by 100. A value around 100 is considered to benormal activity. This metric is the most easily interpretable but tends to be heavilyinfluenced by businesses that post a lot, which may give misleading results. This metricis also numerically less stable when the number of posts is relatively low.We adviseusing this metric if interpretability is the most important criteria.
- activity_quantile: The level of activity as a quantilerelative to the baseline period. 
This is equivalent to the 7-day average of what the University of Bristol researchers call the aggregated probability integral transform metric (see thisarticle in NatureCommunications). It’s calculated by first computingthe approximate quantiles (themidquantiles in the article) of each Page’s daily activity relative to their baseline activity.The quantiles are summed and the sum is then shifted, rescaled and variance-adjustedto follow a standard normal distribution. The adjusted sum is then probability transformedthrough a standard normal cumulative distribution function to get a value between 0 and1. We then average this value over the last 7 days to smooth out daily fluctuations. Wegive this metric a quantile interpretation since it compares the daily activity to the distribution of daily activity within the baseline period, where a value around 0.5 isconsidered normal activity. This is a one-vote-per-Page metric that gives equal weight toall businesses and is not heavily influenced by businesses that post a lot.We advisepreferencing this metric, especially if robustness to outliers and numerical stability areimportant concerns.
- lat: The latitude of the center of the polygon
- lon:The longitude of the center of the polygon
- ds:The date of the activity provided in YYYY-MM-DDformat defined by Pacific Time

# Business verticals

We derived the business verticals by aggregating categories as defined by the admins on thebusiness Pages.
- All:Refers to all businesses in the polygon. Thisincludes but is not limited to all thefollowing categories. (only available in the all_agg datasets)
- Grocery and convenience stores: Retailers that selleveryday consumable goodsincluding food (typically unprepared foods and ingredients) and a limited range ofhousehold goods (like toilet paper). These can include grocery stores, conveniencestores, pharmacies and general stores.
- Retail:Retail other than grocery and conveniencestores such as auto dealers, homegoods stores, personal goods stores and general merchandise/big-box stores likeWalmart
- Restaurants: Businesses that sell prepared food andbeverages for on-premise oroff-premise dining
- Localevents: Events, activities and businesses thatsell real-life experiences, such asamusement parks, bowling alleys, concert venues and social clubs
- Professional services: Services driven by demand froman individual event such as alegal need or health issue that require high customization. Providers usually have anadvanced degree or certification and are considered experts and “knowledge workers.”Examples include CPAs, lawyers, medical professionals, architects.
- Business and utility services: Business services offeringbusiness-to-businessservices like construction, office cleaning, advertising and marketing companies andbusiness software solutions. Utility services offer commodity services like electric,phone, internet, water and energy.
- Home services: Services driven by demand from an individual event at home such asplumbing or electrical work. Examples include home repairs, photographers, cleaning,mechanics, plumbers, electricians, landscapers, interior decorators.
- Lifestyle services: Specific to beauty, care and fitnessservices. These businesses offerstandardized services that are part of a customer's regular routines. Examples includegyms, salons, barbers, and nonmedical and noneducational supervision, like childcarenurseries and pet care.
- Travel: Businesses that provide or sell transportationor accommodation services, suchas airlines, hotels, car rentals and tour operators
- Manufacturing: Businesses that manufacture durablegoods (like furniture and cars) orconsumable goods (like food and personal goods) and have no or limitedbusiness-to-customer sales
- Public good: Includes government agencies, nonprofitsand religious organization
