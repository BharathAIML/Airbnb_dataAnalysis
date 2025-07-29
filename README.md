
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

## 🏙️ Category 1: Location Performance

![App Screenshot](https://drive.google.com/file/d/1hFKDOQb6eb-8R_xnENbZNfIRKe05urui/view?usp=sharing)

Insight 1:
Manhattan dominates Airbnb listings with over 20,000 listings, followed by Brooklyn (~18,000). Together, they account for >80% of all NYC listings from 2008 to 2019, indicating high tourist activity in these boroughs.

Insight 2:
The top neighborhoods with the most listings include Williamsburg (~3,900), Harlem (~3,200), and Bedford-Stuyvesant (~2,900), showing strong hosting activity in both upscale and gentrifying areas.

Insight 3:
Despite high listing density, the average price in Manhattan is significantly higher (~$180–$220) compared to Queens or the Bronx (~$90–$120), suggesting a premium placed on central location.

Insight 4:
Brooklyn and Queens listings show higher availability across the year, potentially due to more long-term hosts or less seasonal demand compared to Manhattan.

##  💰 Category 2: Price Trends & Distribution

![App Screenshot](https://drive.google.com/file/d/1hFKDOQb6eb-8R_xnENbZNfIRKe05urui/view?usp=sharing)

Insight 1:
The average listing price across NYC is ~$152, but varies drastically: Entire homes average ~$212, private rooms ~$95, and shared rooms ~$65.

Insight 2:
Outliers above $1,000 per night skew the price distribution. When capped at $500, the average price stabilizes and offers a clearer view of the central trend.

Insight 3:
Queens and the Bronx are budget-friendly zones, with 80% of listings priced under $100, making them attractive for longer stays or low-budget travelers.

Insight 4:
Listings with high service fees (>$100) typically belong to luxury properties or professional hosts, especially in Manhattan and high-rise buildings.

##  📅 Category 3: Availability & Booking Behavior

![App Screenshot](https://drive.google.com/file/d/1hFKDOQb6eb-8R_xnENbZNfIRKe05urui/view?usp=sharing)

Insight 1:
35% of listings are available year-round (365 days), suggesting commercial use. The remaining listings vary widely — with spikes at 0 (inactive) and 180 (seasonal).

Insight 2:
Listings with availability less than 30 days/year often correlate with high prices and low review counts, hinting at either seasonal use or listings inactive during much of the year.

Insight 3:
The minimum nights requirement shows a median of 3 nights, but some listings require >30 nights, which may align with NYC’s short-term rental regulations.

Insight 4:
Entire apartments/homes show higher minimum stays (~5+ nights) compared to shared/private rooms (~2–3 nights), reflecting booking policies or target guest behavior.

##  🧑‍💼 Category 4: Host & Listing Characteristics

![App Screenshot](https://drive.google.com/file/d/1hFKDOQb6eb-8R_xnENbZNfIRKe05urui/view?usp=sharing)

Insight 1:
Over 40% of hosts have more than one listing, indicating many are professional or commercial hosts rather than individual owners.

Insight 2:
Hosts with 10+ listings are mainly concentrated in Brooklyn and Manhattan, where Airbnb has evolved into a business model.

Insight 3:
Listings with the highest number of reviews (~500+) tend to be private rooms priced below $100 — indicating popularity among solo or budget travelers.

Insight 4:
Review scores (not shown in dataset) could be further integrated to analyze sentiment or satisfaction trends if merged with other Airbnb review data.

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

