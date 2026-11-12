# RentFlow — Digital Equipment Rental & Leasing Platform

Interactive Single Page Application (SPA) prototype built for the Business Analysis Final Project (Team 01, ITM-2401, Astana IT University).

## Live Demo & Stack
- **Live Prototype:** https://rentflow-kz.netlify.app/
- **Frontend:** HTML5, CSS3, Vanilla JavaScript (SPA)
- **Backend & Realtime:** Supabase (PostgreSQL, Row-Level Security, WebSockets)

## Features Demonstrated
- **KYC Onboarding:** 12-digit IIN/BIN validation and ID scan upload.
- **Dynamic Pricing & Booking:** 3+ day discounts, interactive availability calendar locking, and 4-digit SMS-OTP Digital Offer signing (`1234`).
- **Escrow Deposit Isolation:** 5% security deposit hold with automated 100% refund on clean return.
- **Handover Audit Trail & Chat:** Photo/video condition fixation with client-side SHA-256 checksums and real-time persistent chat.
- **RBAC Separation of Duties:** Isolated views for Renter, Owner, Support (Tier 1 Arbiter), and Admin (Tier 2 Moderator).

## Local Setup
1. Clone the repository or download `index.html`.
2. Open `index.html` in any modern browser (Chrome, Edge, Safari) with an active internet connection to connect to the Supabase backend.
