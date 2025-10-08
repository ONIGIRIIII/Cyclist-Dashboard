# Cyclist-Dashboard
# Cyclistic Bike-Share Case Study: Converting Casual Riders to Annual Members

## 📊 Project Overview

This repository contains a comprehensive data analysis case study for Cyclistic, a bike-share company in Chicago. As a junior data analyst on the marketing team, I analyzed user behavior patterns to develop strategic recommendations for converting casual riders into annual members, ultimately driving revenue growth.

**Analysis Period:** January 2025 - August 2025  
**Primary Goal:** Increase annual membership conversions to maximize revenue  
**Interactive Dashboard:** [View Power BI Dashboard](https://app.powerbi.com/view?r=eyJrIjoiZjRkNDZhOWQtYzUwNy00MmRlLWIyMzgtMWIyYjFhMDI5NmViIiwidCI6Ijk4OTk3ZjE3LWI5Y2MtNDVhNy05ZTkxLThhOWFhMTlkMTg5NiJ9)

---

## 📑 Table of Contents

1. [Ask](#1-ask)
2. [Prepare](#2-prepare)
3. [Process](#3-process)
4. [Analyze](#4-analyze)
5. [Share](#5-share)
6. [Act](#6-act)
7. [Key Findings](#key-findings)
8. [Strategic Recommendations](#strategic-recommendations)

---

## 1. Ask

### Business Task

**How do annual members and casual riders use Cyclistic bikes differently, and what strategies can convert casual riders into annual members?**

### Key Questions

- What are the usage patterns between casual riders and annual members?
- When and where do casual riders use the service most frequently?
- What behavioral differences can inform targeted marketing strategies?
- How can we optimize conversion strategies for the next 4 months (September-December 2025)?

### Stakeholders

- **Lily Moreno:** Director of Marketing
- **Cyclistic Marketing Analytics Team:** Data-driven strategy team
- **Cyclistic Executive Team:** Final decision makers

### Success Metrics

- Increase annual membership conversion rate
- Maximize revenue from existing casual rider base
- Develop data-backed marketing strategies for Q4 2025

---

## 2. Prepare

### Data Sources

**Dataset:** Cyclistic historical trip data (January 2025 - August 2025)  
**Source:** Motivate International Inc. (publicly available under license)  
**Organization:** Monthly CSV files containing ride details

### Data Structure

Key variables analyzed:
- `ride_id`: Unique identifier for each trip
- `rideable_type`: Type of bike used
- `started_at`: Trip start timestamp
- `ended_at`: Trip end timestamp
- `start_station_name`: Starting station location
- `end_station_name`: Ending station location
- `member_casual`: User type (member vs casual)

### Data Credibility (ROCCC)

- **Reliable:** First-party data directly from Cyclistic systems
- **Original:** Source data from actual bike-share transactions
- **Comprehensive:** 8 months of complete trip records
- **Current:** Recent data from 2025
- **Cited:** Properly licensed public dataset

### Limitations

- Privacy restrictions prevent linking individual users across multiple trips
- Unable to determine geographic residence of users
- Cannot connect pass purchases to payment methods

---

## 3. Process

### Tools Used

- **Microsoft Excel / Google Sheets:** Initial data cleaning and exploration
- **SQL:** Data aggregation and transformation
- **Power BI:** Interactive dashboard creation and visualization
- **GitHub:** Version control and documentation

### Data Cleaning Steps

1. **Removed duplicates** based on ride_id
2. **Handled missing values** in station names and coordinates
3. **Created calculated fields:**
   - `ride_length`: Duration of each trip (ended_at - started_at)
   - `day_of_week`: Day name for each ride (1=Sunday, 7=Saturday)
   - `hour_of_day`: Hour when ride started (0-23)
4. **Filtered invalid data:**
   - Removed trips with negative duration
   - Excluded trips longer than 24 hours (likely data errors)
   - Removed maintenance and testing rides
5. **Standardized formats:**
   - Consistent date/time formatting
   - Unified station name conventions
   - Standardized member type categories

### Data Integrity Checks

- Verified all ride_ids are unique
- Confirmed date ranges fall within analysis period
- Validated that member_casual field only contains "member" or "casual"
- Cross-checked station names against official station list

---

## 4. Analyze

### Analysis Methodology

Conducted comprehensive analysis across three key dimensions:

1. **Geographic Analysis:** Location-based usage patterns
2. **Temporal Analysis:** Time-based behavior patterns
3. **Duration Analysis:** Trip length comparisons

### Key Calculations

- **Average ride length** by user type
- **Total rides per day/hour/location** by user type
- **Peak usage times** and seasonal trends
- **Station popularity rankings** by user type
- **Weekly usage patterns** by day of week

### Analytical Insights

#### Finding 1: Location-Based Opportunity
The top 10 stations show significantly higher casual ridership compared to annual members, particularly at:
- Streeter Dr & Grand Ave
- DuSable Lake Shore Dr & Monroe St
- Kingsbury St & Kinzie St

**Insight:** These high-traffic casual locations represent prime conversion opportunities.

#### Finding 2: Peak Hour Patterns
Two distinct usage spikes occur at:
- **8:00 AM** - Morning commute
- **5:00 PM (17:00)** - Evening commute

**Insight:** Members dominate commute hours, while casual riders are more evenly distributed throughout the day.

#### Finding 3: Weekend vs Weekday Behavior
- **Weekdays:** Higher member volume, shorter average trip duration (~16-18 minutes)
- **Weekends:** Increased casual usage, longer average trip duration (~23-25 minutes)

**Insight:** Casual riders use bikes primarily for leisure on weekends, while members use them for daily commuting.

---

## 5. Share

### Visualizations

The interactive Power BI dashboard includes:

1. **Top 10 User Locations** (Bar Chart)
   - Compares casual vs member usage by station
   - Identifies conversion opportunity zones

2. **Number of Rides per Hour** (Area Chart)
   - Shows daily usage patterns
   - Highlights peak commute times

3. **Weekly Ride Patterns** (Combination Chart)
   - Displays ride volume by day of week
   - Overlays average duration trends
   - Reveals behavioral differences between user types

### Key Data Stories

**Story 1: The Leisure-to-Commute Opportunity**  
Casual riders primarily use bikes for longer leisure trips on weekends, while members use them for shorter, frequent commute trips. This suggests casual riders haven't yet discovered the commuting value proposition.

**Story 2: Geographic Concentration**  
Tourist and recreational areas show disproportionately high casual usage, indicating these locations are ideal for targeted conversion campaigns.

**Story 3: The Untapped Weekday Potential**  
Significant casual usage exists during weekdays, but with longer durations than member trips. This suggests an opportunity to educate casual riders about membership benefits for regular use.

---

## 6. Act

### Top 3 Strategic Recommendations

#### Recommendation 1: Location-Based Conversion Campaign (Q4 2025)

**Target Locations:** Top 10 casual-heavy stations (Streeter Dr & Grand Ave, DuSable Lake Shore Dr & Monroe St, etc.)

**Tactics:**
- Install digital signage at high-traffic stations showing membership savings calculator
- Deploy street teams on weekends to offer limited-time membership discounts (20% off for sign-ups at these locations)
- Create station-specific QR codes linking to instant membership signup with location-based promotions
- Partner with nearby businesses to offer "member-exclusive" discounts

**Expected Impact:** 15-20% increase in conversions at targeted locations

**Budget:** $50,000 for Q4 2025

---

#### Recommendation 2: Peak-Hour Incentive Program

**Target Times:** 7:00-9:00 AM and 4:00-6:00 PM weekdays

**Tactics:**
- **"Commuter Challenge"**: Casual riders who take 3+ rides during peak hours in a month receive 30% off annual membership
- Push notifications to casual users during peak hours highlighting time and money saved with membership
- Implement "Fast Pass" lanes for members at busy stations during rush hour
- Email campaign showing casual users their potential annual savings based on their peak-hour usage history

**Expected Impact:** 25% increase in weekday casual-to-member conversions

**Budget:** $35,000 for Q4 2025

---

#### Recommendation 3: Weekend-to-Weekday Bridge Program

**Target Audience:** Weekend casual riders with 4+ rides per month

**Tactics:**
- **"Weekend Warrior to Weekday Hero"** campaign: Free 30-day trial membership for frequent weekend casual riders
- Personalized email series highlighting:
  - Cost comparison: casual weekend rides vs. unlimited membership
  - Environmental impact of bike commuting
  - Health benefits of daily cycling
  - Member testimonials from leisure-riders-turned-commuters
- Partner with employers near popular stations for corporate membership discounts
- Create "Commute Starter Kit" for trial members (route planning, safety tips, weather gear recommendations)

**Expected Impact:** 30% trial-to-paid conversion rate, 10% overall membership growth

**Budget:** $45,000 for Q4 2025

---

### Additional Quick-Win Tactics

**For September-October 2025:**
- Launch retargeting ads to casual users who haven't ridden in 30 days: "We miss you! Come back with 40% off membership"
- Create urgency: "Fall Flash Sale - Lock in summer pricing before winter" (limited time discount)
- Implement referral program: Members get 1 month free for each casual rider they convert

**For November-December 2025:**
- Holiday gift memberships at discounted rates
- "New Year, New Ride" campaign positioning membership as fitness/sustainability resolution
- Year-end email to all casual riders showing their 2025 ride stats + potential savings with membership

---

## Key Findings

### Behavioral Differences Summary

| Metric | Casual Riders | Annual Members |
|--------|---------------|----------------|
| **Primary Usage** | Leisure/Recreation | Commuting |
| **Peak Days** | Weekends | Weekdays |
| **Average Trip Duration** | 23-25 minutes | 16-18 minutes |
| **Top Locations** | Tourist/Waterfront areas | Residential/Business districts |
| **Peak Hours** | Evenly distributed | 8 AM & 5 PM sharp |

### Revenue Opportunity

Based on 8 months of data analysis:
- **Current casual rider base:** ~45% of total rides
- **Estimated conversion potential:** 15-25% of casual riders
- **Projected revenue increase:** $850,000 - $1.2M annually (assuming avg membership price $99/year)

---

## Strategic Roadmap (September - December 2025)

### September
- Launch location-based conversion campaign at top 10 stations
- Implement peak-hour incentive tracking system
- Begin email segmentation for weekend warriors

### October
- Activate "Commuter Challenge" program
- Deploy street teams at target locations
- Launch retargeting ad campaigns

### November
- Introduce 30-day trial program for weekend riders
- Launch holiday gift membership promotions
- Implement corporate partnership program

### December
- "New Year, New Ride" campaign kickoff
- Year-end recap emails with savings calculations
- Measure and report Q4 conversion metrics

---

## Project Files

```
├── data/
│   ├── raw/                    # Original CSV files (Jan-Aug 2025)
│   ├── cleaned/                # Processed data files
│   └── aggregated/             # Summary tables and calculations
├── sql/
│   ├── data_cleaning.sql       # Data cleaning queries
│   └── analysis_queries.sql    # Analytical SQL queries
├── visualizations/
│   ├── dashboard.pbix          # Power BI dashboard file
│   └── screenshots/            # Dashboard screenshots
├── documentation/
│   ├── data_dictionary.md      # Variable definitions
│   └── analysis_notes.md       # Detailed analysis notes
└── README.md                   # This file
```

---

## Technologies & Skills Demonstrated

- **Data Analysis:** Excel, SQL, statistical analysis
- **Data Visualization:** Power BI, interactive dashboards
- **Business Intelligence:** KPI development, strategic recommendations
- **Communication:** Executive-level reporting, storytelling with data
- **Project Management:** 6-step data analysis framework

---

## Contact & Portfolio

**Analyst:** Harshpreet Singh  
**LinkedIn:** [Your LinkedIn URL]  
**Portfolio:** [Your Portfolio URL]  
**Email:** [Your Email]

---

## License & Acknowledgments

Data provided by Motivate International Inc. under license.  
This case study was completed as part of the Google Data Analytics Professional Certificate.

---

## Next Steps

To build upon this analysis:
1. Conduct A/B testing of conversion campaigns at selected stations
2. Implement customer satisfaction surveys for new members
3. Analyze retention rates of converted casual riders
4. Develop predictive model for conversion likelihood scoring
5. Expand analysis to include seasonal weather impact on ridership

---

*Last Updated: October 2025*
