# RADMAN SILVER 925 — Phase-1 Selected Asset Pack Usage Guide

This directory contains the curated, finalized, and production-ready **Phase-1 Logo System** for **RADMAN SILVER**. Every file is standardized and optimized for immediate launch across WooCommerce website headers, packaging, social media avatars, and browser favicons.

---

## 1. Selected Usage Map: Which Logo Goes Where?

| Asset Name | Visual Direction | Best Deployment & Application Targets |
| :--- | :--- | :--- |
| **`logo-primary-header-*.{svg,png}`** | **Direction D** (Horizontal Store Header) | **Primary Website Header:** WooCommerce desktop navigation bar, mobile sticky header, email newsletter header, website order invoices. |
| **`logo-icon-*.{svg,png}`** & **`favicon-*.png`** | **Direction C** (Monogram Emblem) | **Primary Brand Icon:** Instagram profile picture, Telegram/WhatsApp avatar, favicon browser tabs, small wax seals, ring stamping. |
| **`logo-packaging-*.{svg,png}`** | **Direction B** (Wordmark + Minimal Ornament) | **Packaging & Print:** Luxury jewelry gift boxes, velvet pouches, authenticity certificates, gift cards, homepage banner hero. |
| **`logo-wordmark-minimal-*.{svg,png}`** | **Direction A** (Pure Luxury Wordmark) | **Minimal / Legal Use:** Website footer, legal Terms & Conditions pages, copyright notices, subtle internal tags. |

---

## 2. When to Use Black vs. White Backgrounds

### Black Versions (`*-black.svg`, `*-black.png`)
- **Visuals:** Solid black `#000000` text and paths on a transparent background.
- **Where to Use:** 
  - Pure white backgrounds (`#FFFFFF`)
  - Cream / Ivory luxury paper textures (`#FAFAFA`, `#FFFBF5`)
  - Light gray backgrounds or light photography cards.
- **Rule:** Never use on dark or low-contrast backgrounds. Maintain WCAG AAA contrast ratio (> 7:1).

### White Versions (`*-white.svg`, `*-white.png`)
- **Visuals:** Solid white `#FFFFFF` text and paths on a transparent background.
- **Where to Use:**
  - Deep matte black backgrounds (`#0B0B0E`, `#0A0A0E`)
  - Dark charcoal luxury navigation headers (`#141418`)
  - Dark moody product photography overlays.
- **Rule:** Never use on white or light backgrounds.

---

## 3. Favicon Files & Browser Tab Deployment

- **`favicon-32.png` (32×32 px):** Retina browser tab icon, bookmarks bar, and Windows desktop taskbar shortcut.
- **`favicon-16.png` (16×16 px):** Legacy standard browser tab icon.
- **Deployment Implementation:**
  Include both sizes in your HTML `<head>` tag:
  ```html
  <link rel="icon" type="image/png" sizes="32x32" href="/brand-assets/radman-silver/final-selected/favicon-32.png">
  <link rel="icon" type="image/png" sizes="16x16" href="/brand-assets/radman-silver/final-selected/favicon-16.png">
  ```

---

## 4. Recommended Minimum Logo Width for Website Header

- **Desktop Navigation Bar:**
  - **Recommended Display Width:** **180px – 240px** (minimum **160px** width).
  - At this width, the primary wordmark `"RADMAN"` and secondary `"SILVER 925"` remain crisp and legible.
- **Mobile Header / Sticky Navbar (e.g. 375px width screens):**
  - **Recommended Display Width:** **140px – 160px** (minimum **120px** width).
  - Ensures ample breathing room for the mobile burger menu icon and shopping bag cart badge.
- **Format Advice:** Always use `logo-primary-header-white.svg` or `logo-primary-header-black.svg` in WooCommerce for razor-sharp vector rendering on high-DPI/Retina screens.

---

## 5. Recommended Profile Image File (Instagram, Telegram, WhatsApp)

- **Primary File:** **`logo-icon-512.png`** (512×512 px transparent PNG) or `logo-icon-white.svg` on a dark canvas.
- **Why:** Social media platforms automatically crop profile images into a circle. The octagonal Persian Shamsa star frame in `logo-icon-512.png` is perfectly centered and proportioned so that all 8 points sit safely inside circular cropping boundaries without any corner clipping.

---

## 6. Recommended Packaging Logo File (Jewelry Boxes & Authenticity Cards)

- **Primary File:** **`logo-packaging-black.svg`** (for cream/ivory boxes and cotton certificates) or **`logo-packaging-white.svg`** (for deep matte black boxes).
- **Why:** Includes the prominent `"RADMAN"` wordmark, the minimalist Persian Shamsa star ornament (`◈`), and `"SILVER 925"`. This balanced 3-tier structure is engineered specifically for hot foil stamping, blind embossing, and letterpress engraving on jewelry boxes, tags, and cards.
