Markdown
# 🛡️ JalShield — Urban Risk & Flood Intelligence Portal
> **AWS Bharat Builds Hackathon 2026 Submission** | Enterprise Municipal Hydrology & Excavation Hazard Intelligence System

[![AWS Amplify CI/CD](https://img.shields.io/badge/AWS_Amplify-Live_Deployment-232F3E?style=flat-square&logo=amazon-aws)](https://main.d1v80rgy7thi9n.amplifyapp.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](LICENSE)
[![Build Status](https://img.shields.io/badge/Build-Passing-brightgreen?style=flat-square)](https://github.com/saloni-Dev63/jalshield)
[![DPDP Act Compliant](https://img.shields.io/badge/DPDP_Act-Compliant_Privacy_Guard-emerald?style=flat-square)](https://github.com/saloni-Dev63/jalshield)

---

## 📌 Executive Summary

Urban waterlogging during monsoon seasons in major Indian metropolitan regions (such as Delhi-NCR and Faridabad) presents a twin crisis: **surface runoff inundation** and **shallow soil sewage contamination**. Conventional flood monitoring tools only track surface water levels, leaving municipal officers, utility workers, and civil contractors blind to underground hazards.

**JalShield** is an enterprise-grade, DPDP Act-compliant municipal web portal that bridges this gap. By integrating real-time meteorological API data with localized soil saturation logic, JalShield automatically calculates ward-level flood vulnerability and predicts **Shallow Excavation Hazard Depths** to prevent toxic blackwater breaches during local digging operations.

---

## ✨ Key Features & Capability Matrix

| Feature Module | Technical Execution | Municipal & Public Value |
| :--- | :--- | :--- |
| **Automated Weather API Sync** | Integrates with Open-Meteo Geocoding & Meteorological API via client-side asynchronous fetch pipelines[cite: 1]. | Eliminates manual input errors by auto-capturing precipitation rates ($mm/hr$) based on ward addresses or GPS[cite: 1]. |
| **Shallow Dig Hazard Engine** | Evaluates soil saturation curves against septic infrastructure age multipliers[cite: 1]. | Prevents hazardous blackwater exposure by outputting safe vs. toxic excavation depth thresholds in feet[cite: 1]. |
| **Grievance Token Tracker** | Client-side state engine with unique token generation (`#MCD-DELHI-2026-XXXX`) & 3-step field resolution tracking[cite: 1]. | Provides citizens with transparent, real-time tracking for municipal waterlogging and sewer complaints[cite: 1]. |
| **Bilingual JalBot AI Desk** | Real-time conversational agent supporting English and Hinglish query processing[cite: 1]. | Ensures high civic accessibility for non-technical residents and local field workers[cite: 1]. |
| **DPDP Privacy Guard** | Client-side AES-256 local encrypted storage simulation for citizen sessions[cite: 1]. | Full compliance with India's Digital Personal Data Protection (DPDP) Act[cite: 1]. |
| **Official Government UI** | Built with NIC/MCD design standards, National Tricolor header, font scaler (`A- \| A \| A+`), and toll-free helpline links (`1800-11-0011` / `1916` / `155304`)[cite: 1]. | Delivers domain authority and immediate trust for government stakeholders[cite: 1]. |

---

## 🧮 Hydrological Scoring Logic & Mathematical Formula

JalShield computes the **Combined Vulnerability Index ($V_I$)** on a scale of $0$ to $100$ using a modified Rational Method equation for urban runoff coupled with an infrastructure degradation coefficient:

$$V_I = \min\left(98, \max\left(12, \left[ (R \times 0.6) + ((100 - D) \times 0.4) \right] \times (S_{age} \times 0.7) \right)\right)$$

Where:
* $R$ = Captured Real-Time Rainfall Intensity ($mm/hr$) via Meteorological API[cite: 1].
* $D$ = Secondary Drainage Desiltation & Clearance Level ($10\% - 100\%$).
* $S_{age}$ = Septic Structure Degradation Coefficient:
  * **$1.0$**: Modern / Sealed Concrete Tank ($< 5$ Years)[cite: 1].
  * **$1.5$**: Aging / Unmaintained Structure ($5 - 15$ Years)[cite: 1].
  * **$2.2$**: Critical Degradation & High Leakage Risk ($15+$ Years)[cite: 1].

### Excavation Hazard Depth Thresholds
* **Low Risk ($V_I < 40$):** Soil saturated depth isolated beyond **$12+$ feet**[cite: 1].
* **Moderate Risk ($40 \le V_I < 70$):** Hazardous effluent table rises to **$4 - 6$ feet**[cite: 1].
* **Critical Risk ($V_I \ge 70$):** Critical saturation! Excavation deeper than **$2 - 3$ feet** risks immediate blackwater exposure[cite: 1].

---

## 🏗️ System Architecture & AWS Infrastructure

┌─────────────────────────────────────────────────────────────────────────┐
│                           JalShield Client                             │
│       Single-File HTML5 / Tailwind CSS / Vanilla JS Application         │
└──────┬────────────────────────────┬─────────────────────────────┬───────┘
│                            │                             │
▼                            ▼                             ▼
┌───────────────┐           ┌───────────────┐             ┌───────────────┐
│ Open-Meteo    │           │ LocalStorage  │             │ AWS Amplify   │
│ Geocoding &   │           │ AES-256 State │             │ Automated     │
│ Weather API   │           │ Encryption    │             │ CI/CD Hosting │
└───────────────┘           └───────────────┘             └───────────────┘


### Serverless Expansion Roadmap (Phase 2 Architecture)
To scale JalShield across all 250+ municipal wards of Delhi-NCR, the application is architected for seamless integration with AWS native serverless services:

[ Citizen Portal ] ──> [ AWS API Gateway ] ──> [ AWS Lambda (Risk Engine) ]
│
┌───────────────────┴───────────────────┐
▼                                       ▼
[ Amazon DynamoDB ]                   [ Amazon Bedrock / SageMaker ]
(Persistent Complaints)                  (ML Hydrological Forecasting)


---

## 🚀 Deployment & Local Installation

### Live Demo Link
The application is live and hosted on AWS Amplify:
🔗 **[https://main.d1v80rgy7thi9n.amplifyapp.com](https://main.d1v80rgy7thi9n.amplifyapp.com)**

### Running Locally
Because JalShield is implemented as a high-performance single-file portal, no heavy Node.js node_modules or build toolchains are required.

1. Clone the repository:
   ```bash
   git clone [https://github.com/saloni-Dev63/jalshield.git](https://github.com/saloni-Dev63/jalshield.git)
   cd jalshield
