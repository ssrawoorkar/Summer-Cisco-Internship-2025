# Summer-Cisco-Internship-2025
# Developer Dashboard

## 📌 Overview
The **Developer Dashboard** is a platform designed to provide visibility into product quality at multiple levels — from overall product builds down to individual test runs.  
It allows engineers, managers, and stakeholders to:

- Monitor quality trends
- Drill down into failing tests
- Compare product versions
- Track build and pipeline health

---

## 🎯 Objectives
- Provide a high-level view of product and component quality
- Enable drill-down from product level to unit, integration, and sanity tests
- Allow comparison between two product versions to identify regressions or improvements
- Offer real-time visibility into build and pipeline health

---

## ✅ Goals Achieved
- Built a dashboard displaying overall product quality as well as quality for multiple components
- Implemented drill-downs to unit, integration, and sanity test levels
- Added a **Comparator** feature to compare results between two versions
- Integrated pipeline health monitoring with error visibility and future alerting capabilities

---

## 🛠️ Technology Stack
- **Languages:** Python, Groovy, Bash, SPL (query language)  
- **Frameworks:** Jenkins  
- **Database / Storage:** Splunk index  
- **Tools:** Splunk, Git, HTTP Event Collector  

---

## 🏗️ System Architecture

### Components
- **Report Generation** – Collects reports from multiple frameworks (JUnit, Pytest, PyATS, CTest, GoTest, etc.) and converts them into JUnit XML format  
- **Publishing** – Normalizes reports into JSON, then publishes them into a database/index via HTTP POST  
- **Dashboard** – Uses queries and panels to visualize data, calculate quality scores, and display trends  

### Features
- **Homepage:** Product-level quality scores, component breakdowns, and historical performance  
- **Component Pages:** Quality scores, recent runs, test breakdowns, and links to pipeline logs  
- **Comparator:** Side-by-side comparison of two builds (persistent failures, recovered tests, new failures, missing tests)  
- **Pipeline Health:** Overview of latest builds across branches with planned anomaly detection + alerting  

---

## ⚙️ Implementation Details
- Reports from different frameworks are standardized into JUnit XML format  
- A publisher parses test results into JSON schema and sends them to the database via HTTP POST  
- The dashboard queries stored results to construct visual panels and interactive graphs  

**Quality score formula:**
*(Unit tests excluded from final calculation to better reflect real build quality)*

---

## 🚧 Challenges & Solutions
- **Problem:** Mapping unit tests to product versions when version stamping occurred later in the cycle  
  **Solution:** Built pipelines that publish metadata “keys” linking product versions with component and repository versions  

- **Problem:** Some frameworks did not natively output JUnit reports  
  **Solution:** Implemented converters or leveraged libraries to transform results  

---

## 📊 Results
- Ingested and visualized **millions of test case results** across multiple pipelines  
- Enabled drill-down from **product → component → repository → test case**  
- Delivered a **Comparator** feature for version-to-version test comparisons  
- Provided direct links to failing test logs for faster debugging  
- Created the foundation for **AI-driven anomaly detection & predictive alerts**  

---

## 📚 Lessons Learned
- Hands-on full-stack experience: frontend dashboards, backend pipelines, DevOps automation, database querying  
- The importance of **early planning and access requests** to reduce blockers  
- Improved skills in **pipeline development, data ingestion, and visualization**  

---

## 🚀 Future Work
- Expand framework support (Vitest, YATAF, etc.)  
- Integrate AI for **predictive alerts and log summarization**  
- Improve pipeline anomaly detection and real-time alerting  
- Expand component coverage and dashboards  

---

## 📷 Screenshots & Diagrams
<img width="434" height="505" alt="Screenshot 2025-09-16 at 1 15 17 PM" src="https://github.com/user-attachments/assets/9758faa6-adc3-47a0-b609-d0a33cff3fd6" />
<img width="438" height="223" alt="Screenshot 2025-09-16 at 1 16 52 PM" src="https://github.com/user-attachments/assets/97c8cdda-dfb5-4140-972a-dac55b94e4b3" />

