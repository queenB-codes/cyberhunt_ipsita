
# 🚀 CyberHunt: Automated Job Intelligence & Data Pipeline

A production-grade, event-driven background intelligence pipeline that automates the ingestion, filtering, verification, and visual tracking of open roles. Built using low-code backend automation frameworks, raw HTTP endpoint scraping, API databases, and a responsive frontend dashboard.

## 📊 Live Deployments
* **Portfolio & Live Interface:** 
* **Backend Engine:** Powered by Make.com
* **Database Ledger:** Google Sheets API

---

## 🛠️ Architecture & Technical Breakdown

The system is engineered as a defensive data pipeline split into three distinct layers: Ingestion, Verification, and Frontend Presentation.


```

[Live RSS Feed] ──> [Make.com Engine] ──> [Filter: Remote Tag Only]
│
▼
[Gmail Alert] <── [Filter: Rating Pass] <── [HTTP Proxy Scraper]
│                                           │
▼                                           ▼
[Push Notification]                         [Google Sheets API]
│
▼
[Live HTML Dashboard]

```

1. Ingestion & Normalization Layer
* Automated Cron Scheduling:** A scheduled polling mechanism monitors live unstructured RSS feeds to capture newly listed opportunities instantly.
* Text Normalization:** Extracted fields are sanitized and processed to isolate strict geographic parameters (e.g., isolating `Remote` positions).

2. Stealth Investigation & Verification Gateway
* HTTP Web-Scraping Module:** The pipeline dynamically fires background HTTP requests to programmatically audit organizational rating data.
* CORS Proxy Integration:** Bypasses isolated browser sandbox restrictions using a public CORS proxy wrapper (`allorigins`) to fetch raw data objects smoothly.
* Defensive Error Handling:** Employs case-insensitive text operators to intercept and automatically drop low-rated or untrusted organization listings, creating a zero-noise target list.
* Multi-Channel Dispatch:** Verified high-value targets are simultaneously appended to a persistent database via the Google Sheets API and dispatched as instant alerts via Gmail.

3. Frontend Presentation Layer
* Real-Time Data Sync:** The frontend dashboard connects natively to the Google Sheets data stream exported as a public `.csv` asset.
* Asynchronous Fetching:** Built completely in raw HTML5 and Tailwind CSS, executing optimized, asynchronous JavaScript loops to render data cards, search filters, and metrics on demand.
* Iframe-Safe Executions:** Bypasses standard cross-origin communication boundaries by removing volatile `AbortSignal` objects in favor of stable, promise-based performance races.

---

## 📂 Repository Structure

```text
├── index.html          # Self-contained Tailwind CSS frontend dashboard
├── README.md           # Technical documentation and architecture blueprint
└── assets/             # System architecture diagrams and screenshots

```

---

## 💻 Technical Stack & Certifications

* Automation & Core DevSecOps:** Make.com, HTTP Webhook/Request APIs, Regex Filtering
* Frontend Architecture:** HTML5, JavaScript (ES6+), Tailwind CSS (Asynchronous Data Fetching)
* Database Operations:** Google Sheets API, CSV Data Parsing
* Associated Framework Knowledge:** * *Microsoft Cybersecurity Certification* (Network Protocols, Threat Vectoring)




---

## 🔧 Local Configuration & Testing

To test the frontend presentation layout locally without the live automation trigger running:

1. Clone this repository to your local machine:
```bash
git clone [https://github.com/YOURUSERNAME/YOUR-REPO-NAME.github.io.git](https://github.com/YOURUSERNAME/YOUR-REPO-NAME.github.io.git)

```


2. Open `index.html` directly in any standard modern browser.
3. To point the dashboard to your personal database instance, modify the data endpoint initialization variable within the script:
```javascript
const baseCsvUrl = "YOUR_PUBLISHED_GOOGLE_SHEETS_CSV_URL_HERE";

```



---


```



```
