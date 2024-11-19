![Screenshot 2024-11-16 at 5 (8)](https://github.com/user-attachments/assets/02400ec2-4d21-45e8-9b18-9ca777a62ddb)

## Overview¶

[MiBici](https://www.mibici.net/) (translated as MyBike in english) is a public bike service used in my home city of [Guadalajara](https://en.wikipedia.org/wiki/Guadalajara), Jalisco, Mexico. This service is used in Guadalajara's Metropolitan Area, which has a population of 5,268,642 (as of 2020) distributed in eight main municipalities and a total area of 2,543.13 squared km (981.91 squared mi).

This service has established stations where users can take and return a public bike, all they need is to sign up through MiBici's platform and pay a charge for 1, 3, 7 days, or annual use. After signing up, users get a transport card that can be used at any station in Guadalajara's Metropolitan Area.

MiBici makes their data public and has published it every month since December 2014.

This notebook includes sections for data cleaning and transformation, exploratory data analysis (EDA), data visualization, and statistical analysis.

## Objective

The aim of this notebook is to analyse public bike use data in Guadalajara's Metropolitan Area and answer the following questions:

- How many bike trips have been registered?
- How many users have used the service?
- What is the mean amount of trips per user?
- What are the demographic charactristics of users (age, sex) and how does bike use vary between groups?
- What are the minimum, mean, and maximum times of bike trips?
- What are the most and least used stations?
- What are the most and least occuring trips between destinations?

## Data

Data was obtained directly from [MiBici's public data website](https://www.mibici.net/es/datos-abiertos/). In this site, data is published in CSV files corresponding to individuals month from December 2014 to March 2024 (datasets range from 1.5 to 33.2 MB). A dataset is also available with the information of the bike stations themselves.

Note: Due to this assignment's 10 MB limit on dataset size, this analysis will focus on only one month of pubic bike use, in this case the most recent month within this size constraint, which is April 2020 (8.9 MB).

#### Dataset 1 - 'datos_abiertos_2020_04.csv' (translates to open_data_2020_04.csv in english)

Contains data of public bike use in Guadalajara's Metropolitan Area during December 2020.

#### Dataset 2 - 'nomenclatura_2024_03.csv' (translates to nomenclature_2024_03.csv in english)

Data of bike stations in Guadalajar's Metropolitan Area.

One final note before getting started, I have cleaned, transformed, and combined all datasets from Dec 2014 to Mar 2024 and published the final dataset (2.51 GB) in [Kaggle](https://www.kaggle.com/datasets/sebastianquirarte/over-9-years-of-real-public-bike-use-data-mibici), this is not part of this analysis but is available if anyone is interested.

## Results

In Guadalajara's Metropolitan Area during April, 2020:

- 129,185 total trips, 8,169 unique users and an average of 15.81 trips per user.
- Mean age was 33.92 years, median age was 31 years, and minimum and maximum ages were 17 and 103 years respectively, with a standard deviation of 10.59 years.
- Average bike ride duration was 11 min and 15 seconds, mean was 9 min 38 seconds, and minimum and maximum were 2 seconds and 23 hours 11 min 46 seconds respectively, with a standard deviation of 13 min 50 seconds.
- Out of 129,185 total trips, 99267 (76.84%) were registered by male users and 29,917 (23.16%) by female users.
- Overall, male users had more registered bike trips and longer trip durations.
- Most bike trips took place on Wednesdays, and there were overall more trips during weekdays than weekends.
- Peaks of bike use were registered at 8am, 2pm, and 6pm, which aligns with typical working schedules from 9am to 5pm with lunch taken usually between 1 - 3pm.
- Most used stations are found around Guadalajara's Downtown which is more densly-populated and has more buisnesses, offices, and cultural settings (restaurants, bars, venues, etc.).
- Least used stations are found at the outskirts of Guadalajara's metropolitan area, which is less densly populated and has less bike stations.
