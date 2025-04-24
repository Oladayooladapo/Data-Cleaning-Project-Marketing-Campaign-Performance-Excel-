# Data-Cleaning-Project-Marketing-Campaign-Performance-Excel-
Leveraging Excel's Advanced Data Cleaning Functions for Marketing Campaign Analysis at Pulse360 Advertising

## Project Summary
This project demonstrates a complete data cleaning workflow using Microsoft Excel on a real-world marketing dataset from Pulse-360 Advertising. The dataset, containing over 99,000 records, was riddled with inconsistencies, missing values, formatting errors, and duplicates—challenges commonly faced in business analytics.

As part of the analysis readiness process, I applied systematic data preprocessing techniques to transform this raw data into a clean, structured dataset ready for performance analysis and reporting.

## Business Context
Pulse-360 Advertising is a full-service marketing firm managing campaigns across multiple digital channels. Each year, they generate an end-of-year report to assess campaign effectiveness. Reliable data is essential to:

Identify successful initiatives

Pinpoint areas needing improvement

Support data-driven strategy for upcoming campaigns

## Project Objectives
✅ Detect and fix missing values, duplicates, and anomalies

✅ Standardize formats across dates, currencies, percentages

✅ Correct inconsistent category names and typos

✅ Separate and recode complex columns for better analysis

✅ Prepare the dataset for accurate and insightful analytics

## Dataset Description

| Column Name         | Description |
|---------------------|-------------|
| `Campaign_ID`       | Unique identifier for each campaign |
| `Company`           | Client name |
| `Campaign_Type`     | Type of marketing campaign (Email, Social Media, etc.) |
| `Target_Audience`   | Demographic targets (e.g., Men Ages 25-34) |
| `Duration`          | Length of campaign (in days) |
| `Channels_Used`     | Marketing channels used |
| `Conversion_Rate`   | Conversion % from views to actions |
| `Acquisition_Cost`  | Cost per acquired customer |
| `ROI`               | Return on Investment (%) |
| `Location`          | City or region of campaign |
| `Language`          | Campaign language |
| `Clicks`, `Impressions` | User interaction metrics |
| `Engagement_Score`  | Score (1–10) indicating audience interaction |
| `Customer_Segment`  | Target audience category |
| `Date`              | Campaign start date |

---

## Cleaning Techniques Applied
### General Cleaning
Removed extra white spaces and trimmed text values

Replaced inconsistent values using Substitute() (e.g., “SM (socail media)” → “Social Media”)

### Format Standardization
Converted percentage strings (e.g., "23%") to numeric values

Removed dollar signs from monetary fields (e.g., "£250" → 250)

Standardized date formats using TEXT() formulas

#### Categorical Fixes
Cleaned and unified naming for campaign types, languages, and customer segments

Replaced ambiguous entries like "All" with more specific terms (e.g., "Men & Women", "All Ages")

### Missing Values Handling
Replaced blanks in numerical columns with zeros using =IF(ISBLANK(), 0, value)

Flagged missing or unusual categorical entries for manual review

### Data Parsing
Split Target_Audience into gender and age group for easier segmentation using:

=LEFT(F1, FIND(" ", F1)-1)
=RIGHT(F1, LEN(F1)-FIND(" ", F1))

### Outlier Detection
Corrected datatypes using =Proper()
corrected date types using =TEXT(W2,"mm/dd/yyy")
Applied Z-score analysis to detect numerical outliers in:

Conversion_Rate

Acquisition_Cost

Clicks and Impressions

Flagged entries with Z-score > 3 as outliers:

Z = (Value - Mean) / StdDev

# What else is in This Repository

Raw_campaign_data.xlsx           Raw dataset
cleaned_campaign_data.xlsx	     Final cleaned dataset


# Outcome
The cleaned dataset is now:

Consistent and formatted for analysis

Free from duplicates and critical missing data

Ready for performance tracking, segmentation, and ROI optimization

This project reflects my attention to detail, understanding of business context, and Excel proficiency in preparing data for impactful decision-making.
