# Tip Split (tip2split.com)

A mobile-first progressive web application (PWA) for calculating fair tip allocations across store staff using a 50/50 weighted split algorithm. Linked to its sister app, Daydot Calc (`day2dot.com`).

---

## Features

* **50/50 Pool Partition Algorithm**:
  * **Half X**: Divided uniformly across all working staff members.
  * **Half Y**: Weighted by role and contract type (BM = 3 pts, Full Time = 2 pts, Part Time = 1 pt).
* **Step Adjustments**: Fine-tune individual role payouts using `+£1` / `-£1` steppers with auto-balancing across other staff.
* **Transparent Breakdown**: Modal detailing the step-by-step pool division, point values, and the mathematical formula.
* **Sister-App Navigation Dock**: Centered, flush bottom dock to jump directly to **Day Dot** (`day2dot.com`).
* **Offline PWA Support**: Precached assets and local Jost fonts ensure full functionality offline.

---

## File Structure

```text
├── fonts/
│   ├── jost-v18-latin-regular.woff2
│   ├── jost-v18-latin-700.woff2
│   └── jost-v18-latin-800.woff2
├── icon.png
├── index.html
├── manifest.json
└── sw.js
