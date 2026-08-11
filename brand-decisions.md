# Master Log of Approved Brand Decisions

Date Convention: All repository dates use Asia/Tehran timezone (UTC+3:30) in ISO format YYYY-MM-DD.

This master record tracks all officially approved brand identity decisions for **RADMAN SILVER 925** (`radmansilver.ir`, `radman925.ir`) and **RIDELIN** (`ridelin.ir`).

---

## 1. RADMAN SILVER 925 (`رادمان سیلور ۹۲۵`)

### A. English Brand Identity — **FINAL APPROVED & LOCKED**
- **Wordmark Typography:** Customized French Didot serif (`RADMAN`) with modern geometric sans-serif subtext (`SILVER 925`) and spaced heritage micro-text (`STERLING • MAISON • EST. 2026`).
- **Canonical Shamsa Crest:** 8-pointed Royal Shamsa star ornament with internal dotted ring, circular borders, and chic capital `'R'` monogram.
- **Locked Colorway Palette:**
  - Primary Dark: Matte Black background (`#0B0B0E`) with Ivory artwork (`#FAF7F2`).
  - Primary Light: Ivory background (`#FAF7F2`) with Matte Black artwork (`#0B0B0E`), featuring a 100% clean Ivory interior inside the Shamsa and zero background rectangles behind text.
- **Canonical Folder Location:** `brand-assets/radman-silver/APPROVED/`

### B. Persian Brand Identity (`رادمان سیلور`) — **FINAL APPROVED & LOCKED**
- **Approval Date:** `2026-08-06` ( Asia/Singapore timezone)
- **Approved Persian Wordmark Font:** **Estedad Bold (`استعداد Bold`)** (Version 8.5, SIL OFL 1.1 by Amin Abedi), offering chic modern geometric luxury proportions.
- **Secondary Line Sizing (`سیلور ۹۲۵`):** **S2 Recommended Size** (approximately 50% visual width of `رادمان`), providing exceptional legibility in digital headers.
- **Tagline Decision:**
  - **Primary Website Logo (`T0` Minimal Version):** **NO TAGLINE** — clean lockup (`Shamsa + رادمان + سیلور ۹۲۵`) reserved for website headers, mobile viewports, and watermarks.
  - **Secondary Brand Logo (`T2` Tagline Version):** **`اصالت در جزئیات`** (Authenticity in Details) — reserved for jewelry boxes, shopping bags, Instagram profile/posts, and "About Us" pages.
- **RTL & BiDi Technical Standard:** Pillow native `libraqm` shaping (`RAQM = True`), logical Unicode strings, `direction="rtl"`, `language="fa"`. Zero manual string reversal.
- **Canonical Folder Location:** `brand-assets/radman-silver/APPROVED-FA/`
  - Complete usage index and background rules documented in `INDEX.md`.

---

## 2. RIDELIN (`رایدلین`)

### A. English & Persian Phase 1 Brand Identity — **FINAL APPROVED & LOCKED**
- **Wordmark & Horizon Line:** Pure minimalist geometric wordmark (`RIDELIN`) paired with the canonical speed blade horizon line below. Zero overlapping circle in header logos.
- **Locked Colorway Palette:** Primary Burgundy (`#8A2747`), Deep Bordeaux (`#681B34`), Primary Black (`#0D0D10`), Ivory (`#FAF7F2`), Platinum (`#D9DCE3`), Charcoal Text (`#17171A`).
- **Persian Wordmark Font:** **Shabnam Bold (`شبنم Bold`)** with short horizon speed line **L3 (`360px`)**.
- **Canonical Folder Location:** `brand-assets/ridelin/APPROVED/` & `brand-assets/ridelin/APPROVED-FA/`

---

## 3. Infrastructure & Hosting Architecture Decision Status — **APPROVED FOR INITIAL TRIAL (NOT YET PURCHASED)**
- **Decision Date:** `2026-08-10` (`Asia/Tehran` timezone)
- **Official Status:** **`APPROVED FOR INITIAL ONE-MONTH PURCHASE AND STAGING TRIAL — NOT YET PURCHASED`** (Approved to purchase, but not yet purchased).
- **Vendor and Plan:** **MizbanFa** (`میزبان‌فا`) Iran managed WooCommerce hosting, **Mars plan** (`مارس` — 60 GB NVMe, advertised 12 Cores / 12 GHz Equivalent CPU, advertised 12 GB RAM, cPanel).
- **Scope Limitation:** **RADMAN SILVER only**. RIDELIN must not be installed or deployed on this host. Staging must be provisioned before any production deployment. Production deployment requires a separate reviewed approval after staging QA.
- **Architecture & Agent Co-Location:** Storefront hosting on MizbanFa Mars is approved for the initial trial. Co-locating Python agents on the same host is **`CONDITIONAL — pending post-purchase Python/Cron/outbound connectivity acceptance tests.`** Python agents may be deployed on the same host only after real verification of Python, pip, venv, Cron runtime, outbound HTTPS, filesystem permissions, process limits, and Legacy API connectivity. If those checks fail during the refund/test window, agents must be moved to a separate runner without blocking the WooCommerce storefront.
- **Review Deadline:** **Review within 30 days after the actual provisioning date and before production launch, whichever occurs first. Provisioning date: TBD.** This is a temporary operational decision for launch speed, not a permanent multi-year architecture lock. All architecture evaluations and host separations obey this absolute decision/review rule.
- **Owner Notification Model:** `SMS mandatory, Telegram optional, WooCommerce Admin fallback allowed` (SMS via Kavenegar is mandatory; Telegram is optional; WooCommerce Admin is the fallback HITL approval path; Telegram availability must not be a single point of failure).
- **Database Yellow Flag:** Vendor support reported MariaDB 10.3.39. Actual database version must be detected after provisioning. Status: **`STAGING-ONLY TEMPORARY COMPATIBILITY WAIVER; production acceptance pending.`** MariaDB 10.3.x is accepted only for staging compatibility testing with an explicit waiver (`ALLOW_LEGACY_DB_FOR_STAGING=1`). It is not automatically approved as the permanent production database. Production Go/No-Go must remain blocked until database compatibility, security risk, and upgrade options are reviewed.
- **Cache Policy:** **`LiteSpeed Cache active, WP Rocket inactive, Redis conditional.`** (LiteSpeed Cache is the selected project page-cache plugin; LiteSpeed Cache and WP Rocket must not be activated simultaneously. Redis persistent object cache may only be activated after real connectivity verification. Distinguish vendor-provided features from project-approved active configuration).
- **Refund/Test Window:** Vendor support stated a 14-day test/refund window. Mark it: **`TO BE RECONFIRMED AGAINST THE PURCHASE TERMS AT CHECKOUT.`**
- **Launch Priority Strategy:**
  - **RADMAN SILVER 925:** RADMAN has launch priority and is approved for initial one-month purchase and staging trial on MizbanFa Mars.
  - **RIDELIN:** RIDELIN must not be installed or deployed on this host. RIDELIN hosting procurement is deferred until RADMAN reaches stable staging/production operation. RIDELIN no-hosting work continues in parallel (including documentation, data model, static content, brand implementation planning, agent contracts, and QA preparation).
- **Preservation of Business Rules:** All previously approved business rules remain strictly locked and unchanged:
  - Exact 1:1 inventory mapping (`legacy_stock = radman_stock`, zero buffer logic, `stock = 1` sellable).
  - Four official RADMAN pricing modes (`silver_weight_only`, `silver_weight_plus_stone`, `legacy_mirror`, `manual_locked`).
  - Manual daily silver rate input via Telegram Bot (`/price <toman_per_gram>`) with interactive summary and button confirmation.
  - Human-in-the-Loop (`HITL`) Telegram order confirmation (`[تأیید موجودی و ارسال]` / `[عدم موجودی و لغو]`) for every paid order.

