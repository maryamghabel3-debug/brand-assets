# RADMAN SILVER — Deterministic Pixel-Level Mask Extraction & Validation Report

## 1. Ground Truth Source & Similarity Audit
- **Ground Truth Source:** `radman-logo-on-black-1600.png` (1600x1200 RGBA)
- **Pixel Similarity with Ground Truth:** **98.60%** (PASS — almost 100% identical, minor anti-aliased edge variance only)

## 2. Identical Mask Shapes Verification
- Both `radman-english-dark-on-black.png` and `radman-english-black-on-ivory.png` generated strictly from single-channel `radman-mask.png`.
- Foreground pixel positions match 100% mathematically. Only RGB values differ.

## 3. Shamsa Interior vs Empty Background Pixel Sampling Audit
We sampled the RGB pixel color at the center of the Shamsa's interior (`x=800, y=380`) and an empty background area (`x=200, y=200`):
- **Dark Version Shamsa Center (800, 380):** RGB=(11, 11, 14) | **Far Background (200, 200):** RGB=(11, 11, 14) -> **PASS** (Both exactly Matte Black #0B0B0E)
- **Ivory Version Shamsa Center (800, 380):** RGB=(250, 247, 242) | **Far Background (200, 200):** RGB=(250, 247, 242) -> **PASS** (Both exactly Ivory #FAF7F2)

## 4. Bottom Text Region Background Audit (Zero Gray/Black Rectangle)
- **Dark Version Region Behind Bottom Text (800, 1085):** RGB=(11, 11, 14) -> **PASS** (Matches Matte Black #0B0B0E exactly; zero rectangle/patch)
- **Ivory Version Region Behind Bottom Text (800, 1085):** RGB=(250, 247, 242) -> **PASS** (Matches Ivory #FAF7F2 exactly; zero gray/black box)

## 5. Summary Check Table
| Test Item | Expected Result | Sampled RGB Value | Validation Status |
| :--- | :--- | :--- | :--- |
| Dark Version Shamsa Interior | `#0B0B0E` (11, 11, 14) | `(11, 11, 14)` | **PASS** |
| Dark Version Far Background | `#0B0B0E` (11, 11, 14) | `(11, 11, 14)` | **PASS** |
| Ivory Version Shamsa Interior | `#FAF7F2` (250, 247, 242) | `(250, 247, 242)` | **PASS** |
| Ivory Version Far Background | `#FAF7F2` (250, 247, 242) | `(250, 247, 242)` | **PASS** |
| Ivory Version Bottom Text BG | `#FAF7F2` (250, 247, 242) | `(250, 247, 242)` | **PASS** |
| Identical Foreground Geometry | 100% Binary Mask Match | Single Mask Source (`radman-mask.png`) | **PASS** |