# Master Project Roadmap — RADMAN SILVER 925 & RIDELIN

> **Single Source of Truth Roadmap (PR-01 Alignment)**  
> *Date Convention: All repository dates use Asia/Tehran timezone (UTC+3:30) in ISO format YYYY-MM-DD.*

---

## 1. Official Phase Model & Current Target Status by Brand

```text
RADMAN SILVER 925:  [Phase 0: DONE] ──> [Phase 1: DONE] ──> [Phase 2: CURRENT] ──> [Phase 3: NEXT]
RIDELIN:            [Phase 0: DONE] ──> [Phase 1: CURRENT] ──> [Phase 2+: PENDING]
```

- **RADMAN SILVER 925 (`radmansilver.ir`):**  
  - **Phase 0 (Documentation & Brand Identity):** **DONE ✅**  
  - **Phase 1 (Repository Setup & Architecture):** **DONE ✅**  
  - **Phase 2 (Infrastructure & Hosting Setup):** **CURRENT ⏭**  
  - **Phase 3 (WordPress/WooCommerce Deployment):** **NEXT ⏳**  
  *(Note: RADMAN has launch priority).*

- **RIDELIN (`ridelin.ir`):**  
  - **Phase 0 (Documentation & Brand Identity):** **DONE ✅**  
  - **Phase 1 (Repository Setup & Architecture):** **CURRENT ⏭**  
  - **Phase 2+ (Infrastructure & Staging):** **PENDING ⏳**  
  *(Note: RIDELIN continues in parallel documentation/prep mode).*

---

## 2. Master Execution Phases (Official 7-Phase Model)

### Phase 0: Documentation & Brand Identity (DONE ✅ — 2026-08-06)
- [x] RADMAN SILVER English canonical logo suite (`radman-silver/APPROVED/`)
- [x] RADMAN SILVER Persian typography & lockup suite (`radman-silver/APPROVED-FA/` — Estedad Bold, S2, T2)
- [x] RIDELIN English brand identity & color palette (`ridelin/APPROVED/` — Burgundy `#8A2747`)
- [x] RIDELIN Persian typography & speed line suite (`ridelin/APPROVED-FA/` — Shabnam Bold L3 `360px`)
- [x] Cross-brand typography consistency review & Option A lock (`brand-decisions.md`)

### Phase 1: Repository Setup & Architecture (RADMAN = DONE ✅ | RIDELIN = CURRENT ⏭)
- [x] Create comprehensive GitHub repository documentation (`README.md`, `Roadmap.md`, `Agents.md`) across `brand-assets`, `radman-silver-store`, and `ridelin-store`.
- [x] Define AI automation agent specifications for product migration, order management, and customer support.
- [ ] Complete remaining RIDELIN-specific technical data modeling and inventory state schema.

### Phase 2: Infrastructure & Hosting Setup (RADMAN = CURRENT ⏭ | RIDELIN = PENDING ⏳)
> **Current Architecture Decision Status:** APPROVED FOR INITIAL ONE-MONTH PURCHASE AND STAGING TRIAL — NOT YET PURCHASED (`MizbanFa Mars`, RADMAN only, storefront approved, agent co-location conditional; Review within 30 days after the actual provisioning date and before production launch, whichever occurs first. Provisioning date: TBD). RIDELIN must not be installed or deployed on this host.
- [ ] **Next Step Execution Path:** `purchase Mars plan -> provision staging -> install WordPress/WooCommerce for RADMAN only`.
- [ ] Await hosting server readiness and DNS propagation for `radmansilver.ir`, `radman925.ir`, and `ridelin.ir`.
- [ ] Provision temporary single-host Iranian WooCommerce cloud hosting (`MizbanFa Mars plan`, RADMAN only, required for domestic Shetab gateways and legacy API reachability; Review within 30 days after the actual provisioning date and before production launch, whichever occurs first. Provisioning date: TBD).
- [ ] Configure Let's Encrypt TLS 1.3 HTTPS, Nginx reverse proxy, and MySQL 8.0+ / MariaDB 10.11+ (`utf8mb4_unicode_ci`; MariaDB 10.3 staging-only temporary compatibility waiver; production acceptance pending).

### Phase 3: WordPress/WooCommerce Deployment (RADMAN = NEXT ⏳ | RIDELIN = PENDING ⏳)
- [ ] Install WordPress 6.x core + WooCommerce e-commerce engine.
- [ ] Deploy and customize **Blocksy Child Theme**:
  - Luxury Jewelry Maison theme for RADMAN SILVER (`#0B0B0E` / `#FAF7F2`).
  - Chic Sport Automotive theme for RIDELIN (`#0D0D10` / `#8A2747` / `#D9DCE3`).
- [ ] Install essential free production plugins (WooCommerce, Persian WooCommerce, Zarinpal, RankMath SEO, WP Super Cache, Wordfence, UpdraftPlus).
- [ ] Apply for Enamad trust badge, connect Zarinpal sandbox, connect Kavenegar SMS sandbox, and configure Telegram Bots.

### Phase 4: Agent Integration & Testing (PENDING ⏳)
- [ ] Deploy `Agent-LegacySync` on the Iranian hosting server (`MizbanFa Mars plan`, RADMAN only — CONDITIONAL: pending post-purchase Python/Cron/outbound connectivity acceptance tests) to connect to `noghrehmashhad.ir` Admin Panel API.
- [ ] Enforce 1:1 Stock Reality (`stock = 1` is sellable, zero buffers) and 3-Tier Pricing Model.
- [ ] Deploy `Agent-Pricing` with daily Telegram rate confirmation workflow (`/price 85000`).
- [ ] Deploy `Agent-OrderApproval` Telegram HITL fulfillment bot.
- [ ] Execute end-to-end sandbox checkout test with Shetab debit card and SMS receipt.

### Phase 5: Soft Launch & VIP Cohort (PENDING ⏳)
- [ ] Conduct Soft Launch 1 for RADMAN SILVER 925 (`RADMAN-VIP15` voucher cohort).
- [ ] Conduct Soft Launch 2 for RIDELIN (`RIDELIN-VIP15` voucher cohort).
- [ ] Test order fulfillment, courier tracking, and customer support chatbot response.

### Phase 6: Public Launch & Scale (PENDING 🎯)
- [ ] Official public launch of `radmansilver.ir` and `ridelin.ir`.
- [ ] Roll out SEO indexing, Google Merchant / Torob integration, and Instagram/Telegram content calendars.
