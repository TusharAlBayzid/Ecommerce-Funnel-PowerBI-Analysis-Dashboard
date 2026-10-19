# 📊 E-Commerce Funnel Analysis & Customer Behavior Dashboard

## 🚀 Project Overview
This project is an end-to-end, interactive Data Analytics Dashboard developed in Microsoft Power BI. Using a dataset of 10,000+ user session records, this dashboard transforms raw web traffic and event data into actionable insights. It empowers marketing and UX teams to track the customer journey, identify major drop-off points in the sales funnel, analyze channel performance, and optimize the overall conversion rate.

## 🛠️ Technical Challenges & Solutions
During the data modeling and dashboard development phase, several technical challenges were resolved to ensure data accuracy and a clean user interface:

**1. Data Transformation & Timestamp Parsing:**
*   **Problem:** The primary `Timestamp` column contained combined Date and Time text strings, preventing granular time-series analysis.
*   **Solution:** Utilized **Power Query Editor** (Column From Examples) to extract and convert the raw timestamp into separate, correctly formatted `Date` and `Time` columns.

**2. Dynamic Funnel Metrics Calculation:**
*   **Problem:** Calculating precise drop-off rates between specific stages (e.g., Browse to Cart vs. Checkout to Purchase) required dynamic row filtering.
*   **Solution:** Engineered custom **DAX Measures** using `CALCULATE` and `DISTINCTCOUNT` to isolate specific events. (e.g., `Total Browse = CALCULATE(DISTINCTCOUNT('funnel_analysis_data'[User_ID]), 'funnel_analysis_data'[Event] = "Browse")`).

**3. Handling Advanced Customer Behavior Metrics:**
*   **Problem:** Identifying returning users and bounce rates required complex session-level calculations.
*   **Solution:** Applied advanced DAX logic to calculate `Return User %` and `Bounce Rate` dynamically, handling division errors gracefully using the `DIVIDE` function.

## 📈 Dashboard Pages & Visual Breakdown
This interactive dashboard is divided into three comprehensive pages, equipped with dynamic slicers (Date, Region, Channel, Device):

**1. User Funnel Performance Dashboard (Executive Overview):**
*   **KPI Cards:** Displays top-level metrics—Total User (10K), Conversion Rate (10.80%), Drop-off Rate (89.2%), and Total Revenue (1.18M).
*   **Funnel Chart (Stages):** Visually maps the user journey drop-offs from Browse (10K) ➡️ Add to Cart (7K) ➡️ Checkout (4K) ➡️ Purchase (1K).
*   **100% Stacked Bar Charts:** Shows stage-to-stage micro-conversion rates (Browse-Add to Cart, Add to Cart-Checkout, etc.).
*   **Distribution Charts (Column, Donut, Pie):** Breaks down Total Revenue and Users by Marketing Channel, Device, and Region.

**2. Funnel Drop-off Diagnostics:**
*   **Treemap (Revenue by Channel):** Highlights Google Ads and Social Media as the most significant revenue drivers by volume.
*   **Clustered Bar Chart:** Analyzes the Drop-Off Rate specifically across different Devices (Mobile, Desktop, Tablet) to find UX bottlenecks.
*   **Line Chart (Revenue Trend):** Tracks daily revenue generation across the entire month.

**3. Customer & Behavior Insights:**
*   **Multi-row KPI Card:** Tracks specialized metrics like Return User %, Bounce Rate (89.20%), AVG Views, and Category Success Rate.
*   **Donut Chart (Bounce Rate by Device):** Pinpoints which device type is causing the highest immediate bounce.
*   **Clustered Bar Chart (Revenue by Category):** Highlights top-performing product categories (e.g., Electronics, Fashion).
*   **Line Chart with Markers (Sessions by Day):** Monitors daily traffic and user engagement consistency.

## 📂 Repository Contents
*   `funnel_analysis_data.pbix`: The fully functional Power BI dashboard containing the data model, custom DAX calculations, and interactive visuals.
*   `funnel_analysis_data.csv` / `.xlsx`: The raw dataset used for this analytical project.
*   `funnel_analysis_data_Page-1.png`, `Page-2.png`, `Page-3.png`: High-resolution image previews of the completed dashboard pages.
*   `funnel_analysis_data.pdf`: A static PDF export of the complete dashboard for quick review and presentation.

---

## 👨‍💻 Author

**Bayzid Mostak**<br>
*Data Analyst & Visualization Expert*

*   [LinkedIn] https://www.linkedin.com/in/bayzid-mostak-data-analyst/
*   [GitHub] https://github.com/TusharAlBayzid
*   Note: Download the `.pbix` file and open it in Power BI Desktop to experience the fully interactive cross-filtering capabilities of this dashboard.
