
# 📊 Airbnb Listing & Host Behavior Analysis
Type: Exploratory Data Analysis (EDA)
Domain: Travel & Hospitality
Tools Used: Python, Pandas, Seaborn, Matplotlib





## 🏢 Project Background
As a data analyst working at a leading online hospitality marketplace, the company has operated in the short-term rental industry for over a decade. Founded in 2008, the company connects property hosts with travelers looking for unique accommodations across the globe. The business operates under a commission-based model, earning revenue from both hosts and guests on each booking. Key metrics include booking volume, average nightly rate, occupancy rate, review counts, and listing availability. Our analytical focus is to drive market competitiveness, optimize pricing, and improve host and guest experiences.

Insights and recommendations are provided on the following key areas:

Category 1: Host Activity & Performance

Category 2: Listing Availability & Reviews

Category 3: Pricing & Service Fees

Category 4: Geographic Trends & Neighborhood Performance


## 🧱 Data Structure & Initial Checks

![App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/4c729e2b531c56a729bc6e9a1543b6dc08e7a422/ERD_1.png)

The company’s main database structure as seen below consists of four tables with a total of 102,599 records:

Table 1: Listings - Main listing information, prices, location, host verification, and policies

Table 2: Hosts - Host identities, listings count, and review statistics

Table 3: Reviews - Number, frequency, and content of guest reviews

Table 4: Availability - Calendar and availability data for each listing




## 📌 Executive Summary

From the dataset, three key trends emerged:

![App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/471cc55ce2433eea600df376fc94e0bb39aaa994/neighb%20.png)


Neighborhood Dominance with Signs of Saturation: Manhattan and Brooklyn account for the majority of listings, indicating a high market share but also showing early signs of oversupply in some areas.

![App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/d483067423bffba0e3a542f7419821f232e0dcf2/AVG.png)

Shifting Price and Engagement Trends Over Time: While average prices have shown fluctuations across years, engagement (measured by review rates) peaked during the pandemic recovery and then gradually declined.

![App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/5b9fb51ae6e93da819ac5ff61cd975c983cfef86/PVR.png)


Availability-Price Sweet Spots: Listings priced in the mid-range with moderate availability and lower minimum stay requirements tend to receive the most consistent review volume.

These findings offer actionable direction for marketing, pricing, and host onboarding strategies.

## 📁 Dataset
The analysis is based on the "Airbnb_data.csv.zip" dataset, which contains detailed listing, host, review, and availability data for Airbnb properties in New York City.

## 🏙️ Category 1: Neighbourhood Group Insights

![App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/3864c37ebcf69f577641a243d7cf7faa43c6faf1/listings.png)

Insight 1:
The majority of listings are concentrated in Manhattan and Brooklyn, together contributing to the largest share of Airbnb properties in NYC.
This was shown through both value_counts() and a barplot. Manhattan leads, suggesting high tourist and business activity.

Insight 2:
Despite having fewer listings, Queens and Bronx offer more budget-friendly options compared to Manhattan.
This suggests price-sensitive customers or long-term renters might prefer these boroughs.

Insight 3:
Staten Island has the fewest listings, indicating low Airbnb activity. Could be due to limited tourist infrastructure or lower demand.

Insight 4:
The groupby aggregation showed average prices are highest in Manhattan, reinforcing its premium market positioning.

##  🛏️ Category 2: Room Type & Price Insights

![App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/a55d9fdaae82da780ac4fe1b78ece3c0fac6e21f/boxplot.png)

Insight 1:
Entire home/apartment is the most common room type, followed by private rooms. Entire homes are the preferred option for tourists and families.

Insight 2:
Shared rooms and hotel rooms form a small portion of listings, showing limited demand or supply.

Insight 3:
Price distribution is right-skewed, with many listings priced under $500 but a few outliers pushing prices much higher. You used a boxplot to detect outliers and cleaned price > $500.

Insight 4:
Room type directly correlates with price, where entire homes are more expensive than private/shared rooms.

## 📍 Category 3: Location-Based Price & Availability

[!App Screenshot](https://github.com/BharathAIML/Airbnb_dataAnalysis/blob/f905b3b94bb953f176993393ffffbb9178f6a094/top.png)

Insight 1:
Some neighborhoods like Williamsburg (Brooklyn) and Harlem (Manhattan) show high listing density. This was shown through neighbourhood.value_counts().head(10)

Insight 2:
The scatterplot of longitude vs latitude colored by price reveals hotspots of expensive listings concentrated in central Manhattan.

Insight 3:
Correlation heatmap shows number_of_reviews, reviews_per_month, and availability_365 are weakly correlated with price.

Insight 4:
Listings with extremely high availability_365 might be owned by professional hosts or businesses.

##  💬 Category 4: Review Activity & Engagement

Insight 1:
Most listings have a low number of reviews, as shown in the review distribution plot.

Insight 2:
There are many listings with 0 reviews, possibly new or inactive. This affects visibility and trust.

Insight 3:
reviews_per_month is higher for private rooms, suggesting higher guest turnover.

Insight 4:
Review count does not strongly correlate with price but may influence booking frequency.

## ✅ Recommendations:

For the Host Onboarding Team: Encourage new hosts to verify their identities and set flexible minimum nights (3-7) to improve review rates.

For the Pricing Strategy Team: Reassess listings with 30-night minimums and high service fees as they are underperforming in terms of review volume.

For the Marketing Team: Focus promotions on Harlem and East Harlem to capitalize on high engagement areas with room for price optimization.

For the Data Quality Team: Normalize price and service fee fields to consistent numerical formats. Flag listings with missing values for follow-up.

For the Product Team: Introduce dashboards or alerts for hosts whose listings are trending down in availability or reviews.

## ⚠️ Assumptions: 
Missing country records were assumed to be in the United States based on neighborhood fields and were re-coded accordingly.

Missing December data for 2021 was imputed using December 2020 averages and November 2021 trends.

Listings with nonsensical review dates (e.g., future dates or 0000/00/00) were excluded.

Service fee and price columns were cleaned by removing currency symbols and converting to float.

License information was missing for 99% of listings; thus, it was excluded from most regulatory analysis.

