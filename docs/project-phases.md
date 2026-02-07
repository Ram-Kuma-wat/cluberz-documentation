# Cluberz Project Phases (214 Business Days)

This plan divides the documented scope into four delivery phases totaling **214 business days**, covering:
- **Vendor Panel** modules (onboarding, zones, events, bookings, finance/legal, and operations)
- **Customer Panel** modules (discovery, listings, detail pages, booking/checkout, profile, favourites, bookings, and security)
- **Admin Panel** modules (login, dashboard, customer/club oversight, approvals, masters, and settings)
- **Figma UI** for the vendor panel
- **Flutter App** implementing the customer panel experience

The total timeline remains **214 business days**; phases are rebalanced to run panel work in parallel.

## Phase Breakdown

| Phase | Business Days | Day Range | Parallel Scope Focus |
| --- | ---: | --- | --- |
| Phase 1 | 60 | Day 1–60 | Vendor Figma approval + customer/admin foundations + Flutter scaffold |
| Phase 2 | 60 | Day 61–120 | Vendor build kickoff (post-Figma) + booking & checkout flows across panels |
| Phase 3 | 50 | Day 121–170 | Admin masters/settings + vendor ops + customer engagement + integrations |
| Phase 4 | 44 | Day 171–214 | Cross-panel QA, UAT, hardening, and rollout readiness |

## Phase 1: Design Approval & Foundations (60 Business Days)
- **Vendor panel (design + requirements)**:
  - Onboarding flow mapping, business profile field definitions, media/gallery requirements.
  - Zone & event data model definitions (zone types, pricing slots, occupancy rules).
  - Reservation combo rule structure and booking close/cancellation policy templates.
  - Figma review and approval gate (development starts only after sign-off).
- **Customer panel (core discovery)**:
  - Location selection, global navigation, and home/discovery layouts.
  - Listing pages (clubs, restaurants, events) with card data requirements.
  - Detail page structures (club/restaurant/event) and static page layouts.
- **Admin panel (baseline operations + masters)**:
  - Admin authentication, dashboard KPI tiles, and base customer/club lists.
  - User management: roles, admin users, customers, and access controls.
  - Full masters setup (zone types, amenities/categories, artists, banks, locations).
- **Figma UI (vendor panel)**:
  - Wireframes, design system, and approval-ready prototypes.
- **Flutter app (customer)**:
  - Project setup, navigation shell, location selection, and discovery/listing screens.

## Phase 2: Vendor Build Kickoff & Commerce (60 Business Days)
- **Vendor panel (post-Figma approval)**:
  - Onboarding + business profile setup, gallery/cover/profile media management.
  - Zone add/edit with pricing matrix (couple/male/female/table) and amenities.
  - Event creation with available zones, booking close time, and cancellation combos.
  - Reservation combo offers (bundle rules) and finance/legal submissions.
- **Customer panel (transactional flows)**:
  - Authentication, profile basics, booking selection, checkout, and payment flow.
  - Booking confirmation, invoice view, and cancellation visibility rules.
- **Admin panel (workflow enforcement)**:
  - Club approvals, booking oversight, and compliance checks.
  - Customer verification, reviews oversight, and dispute flags.
- **Figma UI (vendor panel)**:
  - High-fidelity screens for zones, events, booking controls, and offers.
- **Flutter app (customer)**:
  - Booking, checkout, payment confirmation, and account/profile screens.

## Phase 3: Operations & Integrations (50 Business Days)
- **Vendor panel (operations)**:
  - Booking management (upcoming/past/cancelled), payouts tracking, reporting.
  - Reviews management, support/contact tools, and notification preferences.
- **Customer panel (engagement)**:
  - Favourites, booking history, security/password controls, and notifications.
  - Profile enrichment and saved preferences.
- **Admin panel (settings + compliance)**:
  - Settings: tax, commission, cancellation rules, information pages, compliance.
  - Audit logs, operational monitoring, and escalation workflows.
- **Integrations**:
  - Payment reconciliation, analytics dashboards, and policy alignment.

## Phase 4: QA, UAT & Release (44 Business Days)
- End-to-end QA across vendor, customer (Flutter), and admin panels.
- Performance tuning, security reviews, and data validation.
- Stakeholder UAT, regression fixes, and launch readiness.
