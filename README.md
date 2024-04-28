# pizza-hut-revival

## Overview

The Pizza Wars in Australia from late 1990s to early 2000s saw 3 major players Pizza Hut, Domino's and Pizza Haven vying for industry dominance. In the early 2000s, the war ended with Domino's completely dominating the market through genius pricing strategies with Pizza Haven stores ultimately acquired by Pizza Hut and Pizza Hut losing its leader position in the industry. Now in 2024, Pizza Hut looks to regain its once lost crown. Currently, Domino's holds 50% market share and Pizza Hut holds 10% market share of the pizza quick service restaurant industry in Australia.

![image](https://github.com/TON369777/pizza-hut-revival/assets/156875448/d781f53b-f832-4f86-b712-18e440080c3d)

This project's main objective is to identify opportunities for Pizza Hut to expand their store locations. It is based upon identifying existing store locations, main competitor Domino's store locations and using geographical population data (from ABS) to identify areas or territories which have high population but no existing pizza store presence from either franchise.

## Regarding Data

Store location details were sourced through web scrapping Pizza Hut and Domino's website. Python was used to automate this stage as there were details of 1000+ stores to obtain.

The addresses were then converted to longitude and latitude coordinates through geopy library in Python through the arcGIS API. This is so that PowerBI could more accurately map store locations through the arcGIS map visual rather than just using addresses.

ABS SA2 Regional Population Data was then used to overlay the map as a reference layer so that opportunities could be identified based on areas that had 19 000+ population.
SA2 (Statistical Area Level 2) is a special classification by ABS. In short, SA2 has been designed to cover all over Australia and differs to PostCodes as PostCode does not have complete coverage of Australia. LGA could have been used as well by covers a much larger area often involving multiple suburbs whereas SA2 is more specific. 
https://www.abs.gov.au/statistics/standards/australian-statistical-geography-standard-asgs-edition-3/jul2021-jun2026/main-structure-and-greater-capital-city-statistical-areas/statistical-area-level-2

## Visualising Data

Store location data set with coordinates were used to visualise store locations through arcGIS map visual in Power BI with ABS SA2 Regional Population Data as reference layer. Opportities for expansion would be identified by identifying areas with no pizza franchise presence and with 19 000+ population (denoted by dark blue colour).

![image](https://github.com/TON369777/pizza-hut-revival/assets/156875448/9869ad73-17a8-450f-9341-895b5f256cbd)

## Other Statistics

Other statistics were also obtained through the scrapped data set. This includes proportion of fast food pizza stores by franchise and how many stores in total and proportion by franchise in each state of Australia. Business stakeholders have option to slice and filter charts by state and franchise.

As of April 2024, Pizza Hut has 269 stores (~24%) out of the 1126 fast food pizza chain stores in Australia.

![image](https://github.com/TON369777/pizza-hut-revival/assets/156875448/3b492d2f-9e6d-4c3e-81a0-ff90dc8ba3cf)

## Insights

An example of store location expansion opportunity identified through this data visualisation is:

-Macquarie Park - Marsfield

-Lindfield - Roseville

-Chatswood(West) - Lane Cove North

![image](https://github.com/TON369777/pizza-hut-revival/assets/156875448/4714c6bc-3ad5-4bfa-8f38-45491ab7196e)

These 3 SA2's do not have presence from either Pizza Hut or Domino's making it a great opportunity for Pizza Hut to expand to these areas.

## Opportunities for Optimisation and Improvement

1) arcGIS maps for PowerBI has more features if a premium arcGIS account was used. More reference layers could be used and other demographic context data could be added to better identify store location expansion opportunities example population density, income of population.
2) Other geospatial data could also be used to identify store location expanion opportunities for example traffic data.
3) Up to date regional population data to be used. Australia's population in 2023 has drastically changed since 2021 since Australia entered lockdown in 2021 and Australia has experienced intense surge in immigration numbers in 2023/2024.
