# RentFlow — Digital Equipment Rental & Leasing Platform

> **Educational Project Notice:** This prototype was developed exclusively for educational purposes as part of the *Business Analysis* course (Team Project 2, Team 01, Group ITM-2401) at **Astana IT University** (November 2026). All payment workflows, Escrow holds, SMS-OTP signatures, and user records are simulated for academic demonstration and do not process real financial transactions or real personal data.

## Overview & Live Demo
**RentFlow** is a two-sided digital marketplace for renting and leasing high-value equipment (cameras, laptops, audio gear, and presentation displays) in Astana, Kazakhstan. It replaces physical collateral (such as holding passports) with automated 5% Escrow security deposits, 12-digit IIN/BIN KYC verification, SMS-OTP Digital Offers, and an immutable SHA-256 Media Audit Trail.

- **Live Web Prototype:** https://rentflow-kz.netlify.app/
- **Demo Video (OneDrive — enable English CC for `TC-01`–`TC-10`):** `[ВСТАВЬ_СЮДА_ССЫЛКУ_НА_ONEDRIVE]`

---

## Implemented Requirements (by ID)
The prototype fully implements **22 of 24** functional requirements (all *Must-Have* requirements) and partially implements **2** *Should-Have* features (`FR-08`, `FR-16`):

- **KYC & Onboarding (`FR-01`–`FR-04`):** Role-based registration (`Renter` / `Owner`), strict 12-digit IIN/BIN validation, ID document upload, and Admin `Verified` badge assignment.
- **Equipment Listings & Dynamic Pricing (`FR-05`–`FR-08`):** Listing creation with Astana district tags, base daily rates, automated `3+ days` discounts, and *Rent-to-Own* monthly leasing preview (`FR-08` partial).
- **Catalog Search & Digital Booking (`FR-09`–`FR-12`):** Real-time filtering by category/price/district, itemized quote calculator (rent + 10% platform fee + 5% Escrow deposit), atomic availability calendar locking, and 4-digit SMS-OTP (`1234`) Digital Offer signing.
- **Escrow Payments & Penalties (`FR-13`–`FR-16`):** Isolated 5% Escrow hold, 100% automated refund on clean return, Escrow freeze on damage dispute, and `1.5x` daily overdue penalty calculation (`FR-16` partial).
- **Handover Audit Trail & Live Chat (`FR-17`–`FR-20`):** Mandatory before/after condition media upload tagged with client-side **SHA-256** cryptographic hashes, persistent WebSocket chat, and role-filtered notifications.
- **RBAC Governance & Arbitration Hub (`FR-21`–`FR-24`):** Strict separation of duties via Supabase Row-Level Security (RLS) — Tier 1 Support executes deposit splits, while Tier 2 Admins moderate KYC/listings and hold strict **Read-Only** access (`403`) to financial disputes.

---

## Technology Stack
- **Frontend:** HTML5, CSS3, Vanilla JavaScript (Single Page Application)
- **Backend & Database:** Supabase (PostgreSQL relational schema: `profiles`, `products`, `bookings`, `messages`)
- **Security & Realtime:** Supabase Row-Level Security (RLS), WebSockets Realtime, Web Crypto API (SHA-256)

---

## Local Installation & Setup
1. Clone the repository or download `index.html`:
   ```bash
   git clone [https://github.com/erzhsnsaniya-ui/rentflow-final.git](https://github.com/erzhsnsaniya-ui/rentflow-final.git)
   cd rentflow-final
