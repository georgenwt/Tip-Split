# Tip Split

Tip Split is a mobile-first Progressive Web App (PWA) designed for store teams to calculate and distribute tip pools fairly, transparently, and instantly.

Built with frosted liquid glassmorphism, spring physics, and Costa Burgundy (#730723) theming, the application automates a dual-tier tip distribution model: a 50% baseline equal share combined with a 50% role-weighted dividend.

---

## Features

- Mobile-First Liquid Glass Interface: High-end frosted glass styling (backdrop-filter: blur), floating ambient background orbs, and spring bounce animations.
- Progressive Web App (PWA): Fully installable on iOS and Android with offline caching via sw.js and standalone full-screen support.
- Dual-Tier Mathematical Distribution:
  - Half X (50%): Divided equally across all eligible team members.
  - Half Y (50%): Weighted based on role and contract type:
    - BMs (Assistant Managers): 3 points (Highest share)
    - Full-Time Staff: 2 points
    - Part-Time Staff: 1 point
- Live Interactive Roster Controls: Easily tweak staffing levels with tactile step counters in an accordion drawer.
- Detailed Math Modal: Complete visibility into the live calculations and an academic textbook-level reference formula for pen-and-paper verification.

---

## Mathematical Formulation

Let the team be a finite set of eligible workers S = {1, 2, ..., N} partitioned into three disjoint subsets:
- S_BM: Assistant Managers (Weight w_i = 3)
- S_FT: Full-Time Staff (Weight w_i = 2)
- S_PT: Part-Time Staff (Weight w_i = 1)

### 1. Total Tip Pool Partitioning
The gross tip capital T is partitioned into two equal pools:
X = Y = T / 2

### 2. Total Weighted Role Points (W)
W = sum_{i in S} w_i = 3|S_BM| + 2|S_FT| + 1|S_PT|

### 3. Master Closed-Form Dividend Formula
The individualized tip payout P_i for any worker i is defined as:

P_i = (T / (2N)) + w_i * (T / (2W))

Factored form:
P_i = (T / 2) * [ (1 / N) + (w_i / (3n_BM + 2n_FT + n_PT)) ]

---

## Project Structure

```text
tip-split/
├── index.html       # Single-page web application UI and calculation engine
├── manifest.json    # Web App Manifest for mobile installation
├── sw.js            # Service Worker for offline asset caching
├── icon.png         # App icon (192x192 and 512x512 recommended)
└── README.md        # Project documentation
