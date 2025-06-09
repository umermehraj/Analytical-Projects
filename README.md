# Analytical-Projects

Analysis Overview
This project is to conduct analysis on COVID19-related data to extract factors that may have influence on the spread of COVID-19 virus.

Our team has first built an automated pipeline to aggregate and clean the latest COVID-19 data at state level. Then we have aggregated other data, such as medical resources index, social distancing index, etc, into our dataset for futher analysis.

After preparing the data, we conducted some basic visualizations on the data and have found that social distancing may have a huge impact on spread of COVID-19 by comparing the virus trends of California and New York.

To further verify our findings from a more comprehensive perspective, we bulit linear regression model to quantitatively measure these factors' impact on infection and death rates.

In the end, we reach the conclusion that gathering ban, education level, aging level in one area may have great impact on the spread of COVID-19 virus and made corresponding recommendations based on the results.

Out team has posted a blog about our analytics and findings on Towards Data Science.

Data Preparation
Data Source
The data we used for analysis are gathering from the following sources:

COVID-19 data: Built a pipeline to get and clean the latest data at state level from CSSE daily report.

Medical resource data: 1) Download state-level medicare disparity from Data.Medicare-link2 and surgical quality from Data.Medicare-link1. 2) Extract country-level health index data from WHO through its API.3)Mannually scrap other information from GHDx

Aging data: Mannually scrap data from census.gov

Popularity density data: Mannually scrap information from wikipedia

Basic geographic data: Mannually scrap information from wikipedia

Airpots index data: Mannually scrap data from globalair

Education index data: Mannually scrap information from USA.com

Social distancing index: Get data file from KhakiEconomics

Final dataset overview
Our team has generater two final datasets.

The first one contains all the indices and demographic information about states in US.

The second one contains the latest COVID19 data,including confirmed, death, recovered cases, for each state in US.

Data Visualizations
COVID-19 Overview in US
The COVID-19 situations is most serious in California in west coase and in New York in east coast. So we have picked these two states for deeper visualizations and analysis.

COVID-19 trends in California and New York
COVID-19 trends in CA and NY As we can see from the above graph, CA starts social distancing before things get worse and the new confirmed cases stay at a stable level while NY didn't start social distancing until there are quite a lot confirmed cases, which results in a different situations compared to CA.

Modeling
After gaining some insights from our visualizations and analysis, we applied machine learning techniques to further quantitatively analyze the impact of those factors, such as social distancing, medical resource, etc.

Modeling process
Our team has built two linear regression models to predict infection rate and death rate separately.

The independent variables for both models are standarized index about education, medical resource, public transportation, social distancing, aging and population density.

Modeling results
Model Features Coefficients and P-value From the model results, we have identified three factors, aging index, gathering ban(one index for social distancing) and education level, that have relatively high coefficient and are statically significant.

Recommendations and Insights
Our team found that stricter gathering ban policy would effectively lower the infection rate especially in the early stage when the virus is not eidely spread. Meanwhile, the more population is occupied by elder people, the higher the infection rate will be. This is reasonable because it is proved that old people are more likely to be infected.

Surprisingly, we also found that there's a strong correlation education level and infection rate. Regions with high education level tend to have lower infection rate.

Thus, we recommend that countries or regions where the pandemic is not particularly serious should also release stricter policy about social gathering. Besides, they should also pay more attention to regions with lower education level and give more resources to regions with more elders.
