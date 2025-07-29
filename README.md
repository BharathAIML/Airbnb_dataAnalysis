
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

## 📚 Category 1: Host Activity & Performance

![App Screenshot](https://drive.google.com/file/d/1hFKDOQb6eb-8R_xnENbZNfIRKe05urui/view?usp=sharing)

Insight 1: Verified hosts received 22% more reviews on average and had 16% more annual availability than unverified hosts.

Insight 2: Hosts with more than 3 listings tend to price their properties higher but receive fewer reviews per listing.

Insight 3: Hosts located in Manhattan and Brooklyn dominate the listing count, but the review-per-month rate has stagnated in recent months.

Insight 4: Listings without a verified identity had a higher incidence of missing license and house rule data.


##  📘 Category 2: Listing Availability & Reviews

![App Screenshot](https://drive.google.com/file/d/1hFKDOQb6eb-8R_xnENbZNfIRKe05urui/view?usp=sharing)

Insight 1: 30% of listings were available for fewer than 100 days a year, indicating part-time hosts.

Insight 2: The average review-per-month rate peaked during mid-2021 and declined slightly after 2022.

Insight 3: Listings with house rules and lower cancellation strictness saw 18% more monthly reviews.

Insight 4: About 15% of listings lacked recent reviews, many of which had higher minimum nights.


##  📙 Category 3: Pricing & Service Fees
![App Screenshot](https://drive.google.com/file/d/1_NPhSpIC3_BGbIw5x-7bL22fo-goyqN0/view?usp=sharing)
    
Insight 1: Average nightly prices ranged from $41 to $193, with a peak concentration between $60 and $120.

Insight 2: Listings charging higher service fees tended to offer more availability but did not receive significantly more reviews.

Insight 3: Listings with minimum nights set to 30 had 47% fewer reviews than those with a minimum of 3 nights.

Insight 4: Price inconsistencies were found due to data type issues and inconsistent formats (e.g., dollar symbols in strings).




##  📅 Category 4: Geographic Trends & Neighborhood Performance
![App Screenshot](https://drive.google.com/file/d/1kmeHRe4o3BlTBZe8c_DO4AsVRMKLW-WS/view?usp=sharing)

Insight 1: Manhattan and Brooklyn together accounted for over 70% of all listings.

Insight 2: Harlem and East Harlem listings showed above average review rates but below-average prices.

Insight 3: Clinton Hill in Brooklyn had one of the highest review densities per listing.

Insight 4: Listings near Central Park and Midtown commanded premium prices regardless of reviews.
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

