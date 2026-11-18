# 🏥 Clinic Appointments & Healthcare Operations Dashboard

## 📌 Project Overview
This project delivers an end-to-end healthcare analytics and operational dashboard built in **Microsoft Excel**. It takes raw, uncleaned appointment records and transforms them into a fully automated, interactive executive reporting tool. The dashboard is designed to provide clinic stakeholders with real-time visibility into patient volume, revenue generation, departmental performance, wait times, and cancellation rates.

---

## 🗂️ Workbook Architecture
The Excel workbook (`003_Clinic_Appointments_Project.xlsx`) is structured into four sequential, professional tabs:

1. **`Data`**: Contains the raw, uncleaned dataset (5,120 rows) capturing patient appointments, timestamps, locations, departments, doctors, visit types, billing components, and satisfaction scores.
2. **`Clean_Data`**: The standardized, deduplicated core dataset (5,000 rows across 23 engineered columns) ready for analysis and reporting.
3. **`Analysis`**: The backend calculation engine featuring aggregated Pivot Tables, summary metrics, and KPI formulas powering the front-end visuals.
4. **`Dashboard`**: The front-end executive view featuring a structured visual grid, dynamic KPI cards, connected slicers, an interactive timeline, and full sheet protection for end-user safety.

---

## 🔄 Data Cleaning & Transformation Pipeline
Before building any visuals or metrics, the raw data underwent a rigorous cleaning and feature-engineering workflow:
* **Deduplication:** Identified and removed duplicate `Appointment_ID` records to ensure data integrity.
* **Text Standardization:** Cleaned extra whitespace, fixed inconsistent casing, and normalized text entries across columns using `TRIM`, `CLEAN`, `PROPER`, and `SUBSTITUTE`.
* **String Splitting:** Extracted clean `City` and `Country` attributes from raw `Location` strings using formula logic (`LEFT`, `RIGHT`, and `SEARCH`).
* **Date & Time Extraction:** Parsed appointment timestamps to isolate `Year`, `Month`, and `Hour` for temporal trend analysis.
* **Missing Value Handling:** Cleaned invalid or zero-value patient ages into true blanks to preserve accurate statistical averages without dropping valid appointment rows.
* **Financial Calculations:** Computed net patient billing using structured formula logic: 
  $$\text{Total\_Bill} = (\text{Consultation\_Fee} + \text{Lab\_Charges}) \times (1 - \text{Insurance\_Coverage})$$

---

## 📊 Key Metrics & Executive Insights (KPIs)
The dashboard tracks 5 core performance indicators across a filtered portfolio of **5,000 appointments**:
* **Total Appointments:** 5,000 visits recorded across 2024–2025.
* **Total Revenue:** **$249,733** generated through consultation fees, labs, and insurance settlements.
* **Average Wait Time:** **20.89 minutes** tracked from check-in to provider consultation.
* **Cancellation & No-Show Rate:** **13.98%** combined operational loss rate (`401` cancellations, `298` no-shows against `4,301` completed visits).
* **Patient Satisfaction:** **2.89 / 5** average rating across clinical encounters.

### Department & Regional Performance Highlights:
* **Top Revenue Departments:** **General Medicine** leads with **$72,464**, followed by **Pediatrics** ($38,435) and **Dentistry** ($35,275).
* **Regional Hubs:** **Cairo** accounts for the highest patient volume (**2,064 appointments**), followed by Riyadh, Giza, Alexandria, Dubai, and Jeddah.
* **Visit Types & Payment Methods:** **Consultations** drive nearly 60% of revenue ($148,698), while **Insurance** leads payment methods (1,803 visits) ahead of Cash (1,648) and Card (1,549).

---

## 🖥️ Dashboard Features & User Experience
* **Command Control Panel:** A unified sidebar container housing 4 interactive slicers (`City`, `Department`, `Visit_Type`, `Payment_Method`) and an interactive date `Timeline` (`Appointment_DateTime`).
* **Global Interactivity:** Fully wired **Report Connections** ensure that clicking any filter dynamically updates all summary tables, KPIs, and charts simultaneously.
* **Custom Visual Hierarchy:** Styled using a professional clinical palette (Burgundy accents paired with soft light-blue container cards and custom medical icon headers).
* **Security & Access Control:** The dashboard sheet is protected with unlocked controls, allowing end-users to filter data seamlessly while preventing accidental formula or layout modifications.

> **Dashboard Preview:**
> <img width="1564" height="747" alt="image" src="https://github.com/user-attachments/assets/1a933626-df44-44c1-baf7-f518f368a919" />
> *(Description: Screenshot of the full interactive Excel dashboard showing the top KPI cards, the left-side control panel with slicers/timeline, and the 6 core analytics charts).*

---

## 🛠️ Tools & Techniques Used
* **Microsoft Excel:** Advanced Formulas (`XLOOKUP`, `SUMIFS`, `SUBSTITUTE`, `LEFT`/`RIGHT`), Data Validation, and Conditional Formatting.
* **Data Modeling:** Multi-table Pivot Table aggregation and Pivot Chart generation.
* **Business Intelligence Design:** Interactive Slicers, Timelines, Dynamic KPI Card linking via formula bars, and Sheet Protection protocols.

---
