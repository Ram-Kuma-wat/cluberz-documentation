# Customer Panel Documentation

This document provides module-wise documentation for the Customer Panel (frontend) of the Cluberz booking platform.

## Customer Panel Overview

The Customer Panel is the public-facing and authenticated user interface that allows users to:
- Discover venues and events
- Make event and table bookings
- Manage their profile and bookings
- Save favourites
- Perform secure checkout

The panel is designed to be SEO-friendly, fast, and mobile-first.

## Customer Panel High-Level Modules

1. Global Layout & Navigation
2. Discovery & Listings
3. Detail Pages
4. Booking & Checkout
5. Static Pages
6. Authentication
7. User Profile & Account
8. User Engagement (Favourites, Bookings)
9. Security & Logout

---

## Module 1: Global Layout & Navigation

**Purpose:** Provide consistent navigation and location-based discovery across the platform.

**Components**
- Top Header
- Location Selector
- Search (future scope)
- Login / Profile CTA

**Features**
- Sticky header
- Location-based content rendering
- Auth-aware navigation (Login vs Profile)

**Outcome:** Users can navigate the platform quickly with clear access to location, search, and account actions.
