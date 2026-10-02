# Zomato Restaurant Data Analysis (Excel)

An end-to-end data analysis of **9,551 Zomato restaurants across 15 countries**, built in **Microsoft Excel**. It covers data cleaning, the analysis itself, a dashboard, and business recommendations.

![Dashboard](images/dashboard.png)

## Project Goal
Find out what drives restaurant ratings on Zomato (price, cuisine, location, online delivery, table booking) and turn the findings into practical recommendations.

## Dataset
- **File:** `Zomato_Restaurant_Dataset.csv` (9,551 rows × 21 columns)
- **Fields:** restaurant name, country code, city, locality, cuisines, average cost for two, currency, table booking, online delivery, price range (1–4), aggregate rating, rating text, votes

## Tools & Excel Skills Used
- **Excel formulas:** `COUNTIFS`, `AVERAGEIFS`, `SUMIFS`, `INDEX/MATCH`, `MAXIFS/MINIFS`, `LARGE`, `CORREL`, `MEDIAN`, wildcard matching for multi-value cuisine fields
- **Data cleaning:** country lookup table, helper columns, fixing mislabelled currencies, handling missing values and "Not rated" restaurants
- **Analysis:** segmentation, distribution analysis, correlation, checking a result while controlling for price level (Simpson's paradox)
- **Visualisation:** KPI cards, bar, doughnut and histogram charts, and a one-page dashboard

Every number in the workbook is a **live formula** on the Data sheet, so filtering or editing the data updates the whole report.

## Workbook Structure
| Sheet | What it shows |
|---|---|
| Dashboard | KPIs, 4 charts, key insights, recommendations |
| Country Analysis | Restaurants, rating, delivery and booking by country |
| India Cities | Delhi NCR vs other Indian cities vs international; all 43 Indian cities |
| Cuisines | Top 25 cuisines by count, rating, cost and delivery share |
| Price & Cost | Price ranges 1–4 and cost-for-two bands (INR) |
| Services Impact | Online delivery and table booking vs rating, overall and within price range |
| Ratings & Votes | Rating distribution, votes vs rating, top chains, most-voted restaurants |
| Data Quality | Checks done, fixes applied, method and caveats |
| Lookups / Data | Country code mapping and the cleaned dataset with helper columns |

## Key Insights
1. **The data is India-heavy.** India makes up 90.6% of restaurants, and Delhi NCR alone makes up 83%. Other cities and countries have small samples.
2. **Price level is the #1 driver of rating.** The average rating rises from 3.24 (budget) to 3.89 (premium). Premium restaurants are about 7× more likely to be rated 4.0+ (47% vs 6%).
3. **The budget segment dominates.** 79% of restaurants are in price range 1–2, and the median cost for two in India is about ₹450.
4. **22.5% of restaurants are "Not rated".** All of them have 3 votes or fewer, which means they are new or low-traffic listings.
5. **Votes and rating move together.** Rating correlates with log(votes) at r = 0.65, and "Excellent" restaurants get about 18× the votes of "Average" ones.
6. **Online delivery doesn't lift ratings.** Restaurants with delivery rate 3.38, against 3.47 for those without.
7. **The table-booking "boost" is a Simpson's paradox.** Restaurants with table booking rate +0.17 higher overall. Within price ranges 3–4, though, they rate *lower*, so the overall gap comes from premium restaurants being the ones that offer booking.
8. **North Indian and Chinese restaurants are the most common (41% and 29%) but rate below average (~3.3).** Continental, Italian, Asian and European restaurants rate 3.7–4.0.

## Recommendations
- For a new restaurant in Delhi NCR, a mid-to-premium Continental, Italian or Asian concept has higher ratings and less competition.
- Budget North Indian, Chinese and fast food is a crowded segment. Restaurants there need to stand out on quality.
- Push customers to leave early reviews, because ratings only appear after a few votes and highly-voted places get more visibility.
- Online delivery is under-used (28% in India), which makes it a growth channel, but it won't improve ratings on its own.

## Data Cleaning Notes
- Country codes were mapped to country names through a lookup table.
- The Philippines currency was mislabelled as "Botswana Pula" and has been corrected to Philippine Peso.
- The garbled UK currency symbol was fixed to £.
- 9 missing cuisines were filled with "Not specified".
- Restaurants with rating = 0 ("Not rated") are excluded from all average ratings.
- Cost is compared only within India (INR), because no currency conversion was applied.

## How to Use
1. Download `Zomato_Restaurant_Analysis_Report.xlsx`.
2. Open it in Microsoft Excel and start on the **Dashboard** tab.
3. Use the Data sheet filters, or edit the Lookups sheet (for example, the Delhi NCR city list), and every sheet updates.

---
**Author:** Sadat Khurram · [LinkedIn](https://www.linkedin.com/in/sadatkhurram/) · [GitHub](https://github.com/sadatkhurram1991)
