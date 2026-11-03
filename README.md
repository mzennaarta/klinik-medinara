# 🏥 Klinik Medinara: Operational Performance & Efficiency Analysis

> *"Transforming Operational Healthcare Data into Strategic Business Decisions"*

This data analytics portfolio project presents an in-depth analysis of multi-specialty healthcare operational data to identify financial leakages, optimize physician productivity, and improve pharmacy supply chain efficiency.

---

## 1. Business Understanding

### 1.1 Business Background
Klinik Medinara is a multi-specialty healthcare facility featuring 25 doctors across 8 specialties (General Practice, Pediatrics, Internal Medicine, Dentistry, Dermatology, OB-GYN, ENT, and Ophthalmology). Covering an operational dataset spanning approximately 3.5 years (June 2021 – January 2025), clinic management requires data-driven insights to curb revenue losses and streamline service workflows.

### 1.2 Business Problem
- **Revenue Leakage:** High cancellation and no-show rates severely deplete potential clinic revenue.
- **Administrative & Insurance Inefficiencies:** Discrepancies between patient payment methods and insurance types (e.g., BPJS or private insurance patients paying out-of-pocket with cash/transfer) indicate front-desk verification gaps.
- **Capacity & Stock Optimization:** The need to align physician scheduling and pharmacy procurement strategies with actual patient diagnosis patterns.

### 1.3 Key Business Questions
1. How much revenue is lost to cancellations and no-shows?
2. What is the payment mix composition, and are there insurance mismatches?
3. Which doctors and specialties are the most productive?
4. What is the ratio of returning vs. new patients, and where are they located?
5. What are the most frequent diagnoses and drug prescription patterns?

---

## 2. Data Source & Schema

The clinic's operational dataset consists of 5 core relational tables. Below is the schema structure:

| Table Name | Description | Key Column |
| :--- | :--- | :--- |
| **appointments** | Contains historical records of all patient appointments (dates, attendance status, payment types). | `Appointment_ID`, `Patient_ID`, `Doctor_ID` |
| **patients** | Stores patient demographic profiles, insurance membership statuses, and geographic locations. | `Patient_ID` |
| **doctors** | Contains information regarding the list of doctors, specialties, and clinic assignments. | `Doctor_ID`, `Specialization` |
| **diagnoses** | Records medical diagnosis codes (ICD-10) along with their severity levels. | `Diagnosis_ID`, `Appointment_ID` |
| **prescriptions** | Contains detailed prescription records given by doctors based on patient diagnoses. | `Prescription_ID`, `Diagnosis_ID` |

---

## 3. Tech Stack & Workflow

- **Tools Used:**
  - **Microsoft Excel:** Used for data cleaning, data validation, and initial structural preparation.
  - **Tableau Public:** Used for data modeling, creating calculated fields, and designing interactive visualization dashboards.
- **Analysis Workflow:**
  1. **Dataset & Preparation:** Collecting and validating raw data integrity using Excel.
  2. **Exploratory Data Analysis (EDA):** Exploring historical visit patterns, monthly trends, and data distributions.
  3. **Dashboard Modeling & Calculation:** Connecting table relationships in Tableau and formulating key metrics such as *Revenue Loss*, *Completion Rate*, and *Repeat Patient Rate*.
  4. **Business Insights & Recommendation:** Translating data visualizations into actionable strategies for management.

---

## 4. Data Cleaning
- **Format Standardization:** Harmonized date formats across the appointments table to ensure consistency from 2021 through 2025.
- **Missing Value Handling:** Checked and cleansed missing data within attendance status (*status*) and payment records to prevent distortions in *Revenue Loss* calculations.
- **Relational Integrity Validation:** Ensured primary and foreign key consistency across tables (such as matching `Patient_ID` and `Doctor_ID`) so joining processes in Tableau run smoothly without data duplication.

---

## 5. Key Findings

1. **Revenue Leakage (~14.8%):** The clinic loses approximately **Rp135.87 Million** in potential revenue due to patient cancellations and no-shows. Specialties like Dermatology recorded notable no-show rates (e.g., 10.8% under Dr. Iwan Anggara).
2. **Insurance Mismatch:** An anomaly was discovered where 12% of registered BPJS patients and 84% of private insurance holders settled their bills via out-of-pocket cash/transfer instead of insurance claims.
3. **Productivity & Specialization:** Internal Medicine achieved the highest average revenue yield per physician despite having a smaller doctor count.
4. **Balanced Disease Distribution:** Top 10 diagnoses (such as Bronchial Asthma, Dyslipidemia, Dental Caries, Gingivitis, and Influenza) are evenly distributed with a severity split of 60% mild, 30% moderate, and 10% severe.
5. **High Patient Loyalty:** The *Repeat Patient Rate* reached **78.86%**, reflecting a remarkably strong loyal patient base.

---

## 6. Insights & Strategic Recommendations

- **No-Show Mitigation:** Implement automated H-1 WhatsApp reminders targeting high-no-show specialties. Estimated potential recovery reaches **~Rp31 Million/year** if no-shows are cut in half.
- **Front-Desk Verification Audit:** Conduct audits and streamline front-desk check-in SOPs for BPJS/private insurance eligibility verification to smooth cash inflows.
- **Doctor Capacity Optimization:** Re-evaluate booking slots and schedule allocations for physicians falling below the completion rate average.
- **Pharmacy Supply Chain Management:** Apply buffer stocks and proportional monthly procurement aligned with disease severity trends to prevent stockouts.
- **Expansion & Patient Retention:** Introduce formal retention reward programs while exploring hyper-local marketing expansions into suburban satellite cities.

---

### 👤 Author
**M. Zenna Arta Caessar**
- [LinkedIn Profile](https://linkedin.com/in/M.%20Zenna%20Arta%20Caessar)
