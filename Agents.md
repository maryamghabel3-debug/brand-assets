# Master AI Automation Agent Ecosystem — Architecture & Specifications

This document defines the automated AI agent architecture designed to operate across the **RADMAN SILVER 925** and **RIDELIN** e-commerce platforms.

---

## 1. Ecosystem Overview

```text
[ Legacy Silver Website ] ──(Scrape & Clean)──> [ Agent-Migrate ] ──> [ WooCommerce Database ]
                                                                             │
[ Daily Silver Rate API ] ────────────────────> [ Agent-Orders  ] <────────────┘
                                                      │
[ Customer Web/IG Chat  ] <───────────────────> [ Agent-Support ] ──> [ Size / Gear Guidance ]
```

---

## 2. Core Agent Specifications

### A. `Agent-Migrate` — Legacy Product Migration & Enrichment Agent
- **Target Platform:** `radman-silver-store`
- **Objective:** Seamlessly transfer legacy product catalog from the old silver website into WooCommerce.
- **Key Capabilities:**
  - **Automated Scraping & Parsing:** Extracted product titles, descriptions, silver purity (`925 Sterling`), weights, and prices.
  - **Data Scrubbing & Standardization:** Normalizes Persian typography, corrects RTL numbers, and ensures consistent luxury formatting.
  - **Media Processing:** Downloads product photos, assigns alt tags, and maps images to WooCommerce product galleries.

### B. `Agent-Orders` — WooCommerce Order & Dynamic Pricing Manager
- **Target Platform:** `radman-silver-store` & `ridelin-store`
- **Objective:** Automate inventory tracking, daily pricing updates, and order notifications.
- **Key Capabilities:**
  - **Daily Silver Rate Synchronization:** Silver pricing for RADMAN: Owner inputs daily rate via Telegram (/price [amount]). Agent applies formula to all silver_weight_only products. Live market feed integration is NOT in scope for Phase 1-5.
  - **Inventory Alerting:** Detects low-stock items and triggers automated reordering notifications.
  - **Customer Notification Pipeline:** Triggers personalized bilingual SMS and email notifications upon order placement, processing, and dispatch.

### C. `Agent-Support` — Bilingual Customer Concierge & Consultation Agent
- **Target Platform:** `radman-silver-store` (Jewelry Concierge) & `ridelin-store` (Rider Specialist)
- **Objective:** Provide instant, authoritative customer consultation 24/7.
- **Key Capabilities:**
  - **RADMAN Jewelry Concierge:** Assists customers with ring sizing guides, necklace lengths, gifting advice, and silver maintenance care.
  - **RIDELIN Rider Consultant:** Provides sizing guidance for motorcycle gear, helmet fit recommendations, and accessory compatibility.
  - **Bilingual Natural Communication:** Communicates fluently in clear, polite Persian (`فارسی روان و محترمانه`) and English.
