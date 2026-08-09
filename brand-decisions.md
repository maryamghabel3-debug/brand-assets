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

## 3. Infrastructure & Hosting Architecture Decision Status — **PENDING TECHNICAL DUE DILIGENCE**
- **Decision Date:** `2026-08-09` (`Asia/Tehran` timezone)
- **Vendor-Neutral Requirement:** Production infrastructure must be hosted inside Iran and must pass the approved technical acceptance criteria. Final vendor, plan, and deployment architecture remain **PENDING** until technical due diligence is completed.
- **Candidate Vendors Under Due Diligence:** **MizbanFa** (`میزبان‌فا`) and **ParsPack** (`پارس‌پک`) are candidate hosting providers under technical due diligence. Neither vendor is selected, approved, or preferred; no purchase authorization is granted.
- **Architecture Status:** **`PENDING TECHNICAL DUE DILIGENCE — NO PURCHASE APPROVED YET`**.
- **Launch Priority Strategy:**
  - **RADMAN SILVER 925:** RADMAN launches before RIDELIN. RADMAN hosting vendor and architecture are NOT yet selected; candidates are under evaluation.
  - **RIDELIN:** RIDELIN hosting procurement is deferred until RADMAN reaches stable staging/production operation. RIDELIN no-hosting work continues in parallel (including documentation, data model, static content, brand implementation planning, agent contracts, and QA preparation).
- **Preservation of Business Rules:** All previously approved business rules remain strictly locked and unchanged:
  - Exact 1:1 inventory mapping (`legacy_stock = radman_stock`, zero buffer logic, `stock = 1` sellable).
  - Four official RADMAN pricing modes (`silver_weight_only`, `silver_weight_plus_stone`, `legacy_mirror`, `manual_locked`).
  - Manual daily silver rate input via Telegram Bot (`/price <toman_per_gram>`) with interactive summary and button confirmation.
  - Human-in-the-Loop (`HITL`) Telegram order confirmation (`[تأیید موجودی و ارسال]` / `[عدم موجودی و لغو]`) for every paid order.

