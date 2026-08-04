# RADMAN SILVER — Controlled Persian Font Metadata Report (v6)

This document records the official typography metadata, license, official source, and shaping verification for the four controlled Persian font options tested in **Phase 6 (`APPROVED-FA-review-v6/`)**.

---

## 1. Option A — Gandom (`گندم`)

- **Font Family Name:** `Gandom`
- **Subfamily Name:** `Regular`
- **Exact Installed File Path:** `/home/user/.fonts/Gandom.ttf`
- **Font Version:** `Version 0.8`
- **OS/2 `usWeightClass`:** `400` (Normal / Regular weight)
- **Weight Classification Note:** Despite visually displaying heavy, serif-like contrast strokes, its internal TrueType metadata confirms `usWeightClass = 400` (`Regular`), not true Bold. It is a single-weight release by Saber Rastikerdar. No synthetic or fake bolding was applied.
- **License:** **SIL Open Font License (OFL) 1.1** (Open-source, free for commercial use)
- **Official Source:** Saber Rastikerdar Official GitHub Repository (`https://github.com/rastikerdar/gandom-font`)
- **Persian Shaping & BiDi Result:** **PASS (`100%`)** — Native `libraqm` rendering in Pillow (`RAQM = True`) correctly shapes and joins characters (`ما` in `رادمان`) in logical right-to-left order without manual reversal.

---

## 2. Option B — Estedad (`استعداد`)

- **Font Family Name:** `Estedad`
- **Subfamily Name:** `Bold`
- **Exact Installed File Path:** `/home/user/.fonts/Estedad/Estedad-v8.5/Statics/ttf/Estedad-Bold.ttf`
- **Font Version:** `Version 8.5`
- **OS/2 `usWeightClass`:** `700` (True Bold weight)
- **Weight Classification Note:** True Bold weight (`700`), offering a modern geometric luxury proportion without excessive stroke thickness.
- **License:** **SIL Open Font License (OFL) 1.1** (Open-source, free for commercial use)
- **Official Source:** Amin Abedi Official GitHub Repository (`https://github.com/aminabedi68/Estedad`)
- **Persian Shaping & BiDi Result:** **PASS (`100%`)** — Flawless RTL shaping and character joining via native HarfBuzz/FriBidi in `libraqm`.

---

## 3. Option C — Noto Kufi Arabic (`نوتو کوفی`)

- **Font Family Name:** `Noto Kufi Arabic`
- **Subfamily Name:** `Bold`
- **Exact Installed File Path:** `/home/user/.fonts/NotoKufiArabic-Bold.ttf`
- **Font Version:** `Version 2.100`
- **OS/2 `usWeightClass`:** `700` (True Bold weight)
- **Weight Classification Note:** True Bold weight (`700`), Kufic architectural geometry.
- **License:** **SIL Open Font License (OFL) 1.1**
- **Official Source:** Google Fonts Official Repository (`https://github.com/googlefonts/noto-fonts`)
- **Persian Shaping & BiDi Result:** **PASS (`100%`)** — Clean Kufic RTL rendering.

---

## 4. Option D — Noto Naskh Arabic (`نوتو نسخ`)

- **Font Family Name:** `Noto Naskh Arabic`
- **Subfamily Name:** `Bold`
- **Exact Installed File Path:** `/home/user/.fonts/NotoNaskhArabic-Bold.ttf`
- **Font Version:** `Version 2.100`
- **OS/2 `usWeightClass`:** `700` (True Bold weight)
- **Weight Classification Note:** True Bold weight (`700`), classic Naskh calligraphic book style.
- **License:** **SIL Open Font License (OFL) 1.1**
- **Official Source:** Google Fonts Official Repository (`https://github.com/googlefonts/noto-fonts`)
- **Persian Shaping & BiDi Result:** **PASS (`100%`)** — Clean calligraphic RTL rendering.
