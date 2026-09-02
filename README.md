# Marketing Campaign Performance Dashboard

**Tools:** Power BI · DAX
**Type:** Marketing analytics dashboard / data analytics portfolio project

A Power BI dashboard built to analyze how a business's marketing campaigns are performing across platforms (Google, Instagram, TikTok, WhatsApp, Facebook, Email, LinkedIn) — covering spend, ROI, engagement, conversion, and revenue by service, content type, and target audience.

---

## 📌 Business Problem

The business promotes a mix of services — hotel rooms, weekend getaways, buffets, corporate events, and conferences — through paid and organic campaigns spread across seven digital platforms. With spend and results scattered across channels, there was no single view showing which platforms, content types, or audience segments were actually converting into bookings and revenue, making it hard to justify or reallocate marketing budget with confidence.

## 🎯 Objective

Build a dashboard that lets a marketing/business stakeholder answer, at a glance:
1. Is our ad spend generating a positive return, and on which platforms?
2. Which campaigns and platforms convert engagement into actual bookings?
3. Which content types, services, and audience segments perform best — and worst?

## 🗂️ Dataset

A simulated marketing campaign dataset created for this portfolio project, modeled on a hospitality & events business running paid and organic campaigns across multiple digital platforms.

Fields used: `CampaignName`, `Platform`, `CampaignType`, `OrganicPaid`, `ContentType`, `ServicePromoted`, `TargetAudience`, `Date`, `Engagements`, `Clicks`, `Bookings`, `AdSpend`, `RevenueGenerated`.

## 🛠️ Approach

1. **Data preparation** — cleaned and shaped the raw campaign data in Power Query, standardizing platform/campaign naming and date fields.
2. **Data modeling** — built relationships between campaign, platform, and date dimensions to support cross-filtering.
3. **DAX measures** — created custom measures, including:
   - `ROI Multiple` = Total Revenue Generated ÷ Total Ad Spend
   - `Average Cost per Booking` = Total Ad Spend ÷ Total Bookings
   - `Average Conversion Rate` = Sum of Bookings ÷ Sum of Clicks (or Engagements)
4. **Dashboard design** — split the analysis into three focused report pages (below) rather than one crowded page, each with its own slicers so a user can drill in without losing context.

## 📊 Dashboard Walkthrough

### Page 1 — ROI & Spend Overview
![ROI & Spend Overview](screenshots/roi-spend-overview.png)

Answers: *"Are we spending efficiently, and where?"*
- Total Ad Spend: **61M** | Total Revenue: **232M** | ROI Multiple: **3.79**
- Total Bookings: **1K** | Average Cost per Booking: **71.94K**
- **Google has the highest ROI multiple** by a wide margin, followed distantly by WhatsApp — platforms like LinkedIn and Facebook lag behind despite spend
- Monthly Ad Spend vs. Revenue trend shows a **seasonal spike around July–August**

### Page 2 — Engagement & Conversion
![Engagement & Conversion](screenshots/engagement-conversion.png)

Answers: *"Is engagement actually turning into bookings?"*
- Scatter plot of Engagements vs. Bookings by platform highlights that high engagement doesn't always mean high bookings — some platforms drive attention without driving action
- Campaign-level breakdown table (engagements, clicks, bookings, revenue) supports drilling into individual campaigns like "All You Can Eat Promo"

### Page 3 — Platform, Content, Service & Audience Performance
![Platform, Content, Service & Audience Performance](screenshots/platform-content-audience.png)

Answers: *"Where should budget and creative focus go next?"*
- **Google generates by far the most total revenue** of any platform
- **Story and Video content** have the highest average conversion rates — Carousel and Photo lag behind
- **Event Planners and Couples** have the highest average cost per booking, i.e. the most expensive audiences to convert
- **86.7% of bookings come from Paid campaigns**, only 13.3% Organic

## 💡 Key Insights & Recommendations

- **Shift budget toward Google and WhatsApp**, the two highest-ROI platforms, and reassess spend on lower-performing channels like LinkedIn and Facebook.
- **Prioritize Story and Video content** in future campaigns given their higher conversion rates versus static formats like Photo and Carousel.
- **Re-evaluate targeting for high-cost audiences** (Event Planners, Couples) — either adjust the offer/creative for them or accept the higher acquisition cost if their lifetime value justifies it.
- **Plan for the July–August seasonal peak** by front-loading budget and content ahead of that window.

## 🔍 What I'd Improve Next

- Add a customer lifetime value metric to weigh against cost-per-booking, so "expensive" audiences can be judged on long-term value, not just acquisition cost.
- Bring in a second year of data to confirm whether the July–August spike is a true seasonal pattern or a one-off.
- Add a simple forecast for next quarter's ad spend and expected revenue based on current trends.


3. Use the slicers on each page (Platform, Campaign Type, Organic/Paid, Content Type, Date, etc.) to explore the data interactively
