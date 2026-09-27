# 🏙️ NYC Airbnb Market Dashboard

An interactive 3-page Excel dashboard analyzing the NYC Airbnb 2019 dataset — exploring pricing, availability, host concentration, and neighbourhood dynamics across all five boroughs of New York City.

📊 **[Open the Full Dashboard (Google Drive)](https://docs.google.com/spreadsheets/d/1PDgg46HsRfXufBfyfUeTRF6TqDTN-jUJ/edit?usp=sharing&ouid=102257784823381701268&rtpof=true&sd=true<img width="880" height="396" alt="Screenshot 2026-09-26 235534" src="https://github.com/user-attachments/assets/0b3bb89b-4bf5-457c-afab-5b3df9cf8749" />
<img width="605" height="387" alt="Screenshot 2026-09-26 235512" src="https://github.com/user-attachments/assets/74c4cd91-0a7b-4571-9a3d-ab6d54cb662e" />
<img width="901" height="359" alt="Screenshot 2026-09-26 235443" src="https://github.com/user-attachments/assets/8a167afa-f6c4-49e1-b336-c6f6952f847d" />
)**

---

## 📌 Project Goal

Build an interactive Excel dashboard that helps a stakeholder — a new host, an investor, or a market analyst — understand NYC's short-term rental market well enough to make informed pricing and investment decisions.

---

## 📂 About the Dataset

- **Source:** NYC Airbnb Open Data (2019)
- **Size:** ~48,895 listings, 16 columns
- **Coverage:** All 5 NYC boroughs — Manhattan, Brooklyn, Queens, Bronx, Staten Island
- **Room Types:** Entire home/apt, Private room, Shared room
- **Key Columns:** `price`, `neighbourhood_group`, `neighbourhood`, `room_type`, `host_id`, `host_name`, `number_of_reviews`, `last_review`, `reviews_per_month`, `availability_365`

---

## 🧹 Data Cleaning (Power Query)

| Issue Found | Action Taken |
|---|---|
| 11 listings priced at $0 | Removed — invalid data |
| 10,052 blank `reviews_per_month` values | Replaced with 0 (blank = zero reviews, not missing data) |
| Blank `last_review` dates | Left as null (not faked) — added a `Review Status` flag instead |
| 21 blank `host_name`, 16 blank `name` | Labeled "Unknown" |
| Inconsistent data types | Fixed dates, whole numbers, and decimals |
| No price grouping | Created a `Price Bucket` column — Budget / Mid-Range / Premium / Luxury |

---

## ❓ Business Questions Answered

1. How does price vary by borough and room type?
2. Which neighbourhoods have the highest price / listing density?
3. Does price affect availability?
4. Which room type dominates each borough?
5. Who are the top hosts by number of listings?
6. How does review activity relate to price?
7. What's the typical minimum-nights requirement?
8. Which areas are under-saturated opportunities for new hosts?

---

## 📊 Dashboard Pages

### 1️⃣ Overview
KPI summary (Total Listings, Average Price, Total Hosts, Average Availability), average price by borough, listings by borough, and room type breakdown — with interactive slicers for borough and room type.

### 2️⃣ Pricing & Availability
Deeper pricing analysis — price by borough & room type, reviews by price tier, availability by price tier, and listings by price tier — with a Price Bucket slicer and a review-date Timeline control. Includes both **average** and **median** price to account for luxury outliers skewing the data.

### 3️⃣ Hosts & Neighbourhoods
Top 10 hosts (grouped by unique `host_id` to avoid merging different people with the same name), top 10 neighbourhoods by listing count, and a summary of key insights and recommendations.

---

## 🔑 Key Findings

- **Manhattan** has the highest average price (**$196.88**) — more than double the Bronx (**$87.58**)
- **65.3%** of listings are priced under $150/night — the market skews budget-to-mid-range, not luxury
- **Median price ($106)** is notably lower than **average price ($153)** — luxury outliers pull the average up
- The top hosts are **professional property managers** (Sonder, Blueground) — not individuals — running 550+ listings combined
- **Williamsburg** and **Bedford-Stuyvesant** are the most saturated neighbourhoods, each with 3,700+ listings
- Higher-priced (Luxury tier) listings show **higher average availability**, suggesting lower booking demand at that price point

---

## 🎯 Recommendations

- New hosts may find less competition in **Staten Island** or the **Bronx**
- Benchmark pricing **by borough**, not a single citywide number
- Pricing above **$300/night** is rare — reserve it for genuinely premium/unique listings

---

## 🛠️ Tools Used

`Excel` · `Power Query` · `PivotTables & PivotCharts` · `Data Model` · `Slicers & Timeline`

---

## 🖼️ Screenshots

### Overview
![Overview](page1-overview.png)

### Pricing & Availability
![Pricing](page2-pricing.png)

### Hosts & Neighbourhoods
![Hosts](page3-hosts.png)

---

## 📁 File Access

The dashboard file is hosted on Google Drive (not in this repo directly) due to file size — click the link at the top of this page to view or download it.
