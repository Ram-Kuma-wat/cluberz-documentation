# Cluberz Customer Panel Documentation

This document consolidates all customer panel modules into one reference.

# Module 1: Global Layout & Navigation

## Purpose
Provide consistent navigation and location-based discovery across the platform.

## Components
- Top Header
- Location Selector
- Search (future scope)
- Login / Profile CTA

## Features
- Sticky header
- Location-based content rendering
- Auth-aware navigation (Login vs Profile)

## Outcome
Users can navigate the platform quickly with clear access to location, search, and account actions.

# Module 2: Location Selection

## Purpose
Allow users to browse content based on city/location.

## Features
- Auto-detect location (optional)
- Manual location selection
- Location persistence (cookie/local storage)

## Affects
- Listings
- Search results
- Availability & pricing

## Outcome
Users see relevant venues, events, and pricing based on their selected location.

# Module 3: Home Page

## Purpose
Serve as the primary discovery and marketing page.

## Sections
- Hero section
- Featured Night Clubs
- Featured Restaurants
- Upcoming Events
- Popular Venues
- Promotions / banners

## Behavior
- Location-based data
- Click-through to listing & detail pages

## Outcome
Users can discover venues and events quickly through curated, location-aware sections.

# Module 4: Night Clubs Listing Page

## Purpose
List all night clubs available in the selected location.

## Features
- Paginated / infinite scroll list
- Filters (price, rating, amenities – future)
- Sorting (popularity, rating)

## Data Shown
- Club name
- Images
- Location
- Starting price
- Rating

## Outcome
Users can browse and filter night clubs with key details for quick comparison.

# Module 5: Restaurants Listing Page

## Purpose
List restaurants available for table reservations.

## Features
- Restaurant cards
- Cuisine & cost indicators
- Availability highlights
- Paginated / infinite scroll list
- Filters (price, rating, amenities, and more)
- Sorting (popularity, rating, etc.)

## Outcome
Users can browse restaurants with availability and key details for table reservations.

# Module 7: Night Club Detail Page

## Purpose
Show complete details of a club.

## Sections
- Image gallery
- About club
- Amenities
- Zones & pricing overview
- Policies
- Location map
- Reviews
- Events hosted by the club

## Outcome
Users can evaluate a club and decide on bookings with full context.

# Module 8: Restaurant Detail Page

## Purpose
Show restaurant details and table reservation options.

## Sections
- Hero summary card (rating, cuisines, cost for two, address, open status)
- Gallery
- About restaurant
- Location and direction
- Cuisine & cost
- Amenities
- Operational hours
- Available reservation slots
- Book table panel
- Policies
- Reviews

## Hero Summary Card

**Data Shown**
- Rating and review count
- Cost for two
- Cuisine tags
- Address
- Open status and closing time

**Actions**
- Book Table CTA
- Call
- Direction
- Show all images

---

## Book Table Panel

**Fields**
- Date selector
- Time slot
- Guest count
- Booking CTA (confirm/reserve)

**Behavior**
- Uses available reservation slots based on selected date/time.
- Confirmation opens checkout or booking summary.

## Outcome
Users can review restaurant details and reserve a table from the detail page.

# Module 9: Event Detail Page

## Purpose
Provide detailed event information and booking entry point.

## Sections
- Event images
- Event description
- Venue details
- Event date & time
- Available zones
- Pricing per zone (Couple / Stag / Table)
- Cancellation policies

## CTA
- Book Now (land on booking page)

## Book Now Flow
- If already logged in, collect guest details for each selected zone.
- Proceed to checkout with appropriate payment options.

## Outcome
Users can review event details and start a booking with zone-specific pricing.

# Module 10: Event Booking Information & Checkout

## Purpose
Enable structured zone-wise booking and payment.

## Booking Flow
1. Select Zone(s)
2. Select ticket type (Couple / Male Stag / Female Stag / Table)
3. Select quantity (as per zone limits)
4. Enter guest names (dynamic based on seats)
5. Review booking summary
6. Checkout & payment

## Checkout Details
- Ticket price
- Cover amount
- Taxes
- Discounts / coupons
- Final payable amount

## Payment
- Online payment gateway
- Booking confirmation after success

## Outcome
Users can complete a zone-wise booking with a clear cost breakdown and payment confirmation.

# Module 11: Static Pages

## Purpose

Provide informational and compliance content that supports trust, SEO, and legal requirements.

## Pages Included

- About Us
- Contact Us
- Privacy Policy
- Terms & Conditions
- FAQs (if needed)
- Refund & Cancellation Policy (if required)

## Core Features

- SEO-ready metadata (title, description, canonical)
- Consistent layout with header/footer
- Mobile-first readability and accessibility
- Internal linking to support navigation and discovery

## Content Guidelines

- Keep copy concise and user-friendly
- Highlight contact options and support hours on Contact Us
- Ensure legal pages are versioned and include last updated dates

## Navigation & Discovery

- Footer links to all static pages
- Optional header link for About Us and Contact Us
- Search engines can crawl without authentication

# Module 12: Authentication (Customer)

## Purpose

Allow users to register and log in securely.

## Login Options

- Email login
- OTP-based login
- Google login

**OTP Flow Behavior**
- After OTP verification, if the user is already registered, complete login.
- If the user is not registered, automatically redirect to the signup form.

## Signup

**Fields**
- Name
- Email
- Phone Number
- Gender

**Notes**
- Validate email and phone number formats before account creation.
- Display terms/privacy links on the signup screen for consent.

# Module 13: User Profile

## Purpose

Allow users to manage personal information and preferences.

## Sections

- Profile details
- Contact information
- Gender
- Email & phone verification status

## Behaviors

- Show verification badges for confirmed email/phone.
- Prompt verification flow when contact details are edited.

# Module 14: My Bookings

## Purpose
Allow users to track all event and table reservations, view booking details, and download invoices.

## Booking Types
- **Event Bookings**
  - Upcoming
  - Past
  - Cancelled
- **Table Bookings**
  - Upcoming reservations
  - Past reservations
  - Cancelled reservations

---

## Event Bookings List

**Fields**
- Booking ID
- Event Name
- Venue (Club/Bar/Lounge)
- Event Date
- Booking Status (Upcoming/Past/Cancelled)
- Payment Status (Paid/Pending/Cancelled)
- Ticket Summary (count + total)

**Instructions**
- Allow filters by status and date.
- Provide quick access to booking details and invoice download.

---

## Event Booking Details

**Fields**
1. Booking ID
2. Booking Date
3. Venue Name
4. Event Name
5. Location
6. Event Date & Time
7. Primary Guest Name
8. Primary Guest Email
9. Primary Guest Phone
10. Payment Status (Paid/Cancelled/Pending)
11. Ticket Table
    - Zone
    - Type (Couple/Male Stag/Female Stag/Table)
    - Guest Details (names)
    - Ticket Count
    - Price per Ticket
    - Cover Amount
    - Total Ticket Price
12. Sub Total
13. Discount
14. Tax
15. Platform Fee
16. Final Payable Amount

**Invoice**
- Downloadable invoice/receipt for completed bookings.

---

## Table Bookings List

**Fields**
- Reservation ID
- Restaurant Name
- Reservation Date
- Reservation Slot
- Guest Count
- Payment Status
- Booking Status (Upcoming/Past/Cancelled)

**Instructions**
- Allow filtering by status and date.
- Provide access to reservation details and invoice.

---

## Table Booking Details

**Fields**
1. Reservation Detail Title
2. Reservation ID
3. Booking Date & Time
4. Restaurant Name
5. Reservation Date
6. Reservation Slot
7. Location
8. Primary Guest Name
9. Primary Guest Email
10. Primary Guest Phone Number
11. Payment Status
12. Table For (guest count)
13. Reservation Cost
14. Promo Discount
15. Sub Total
16. Internet Handling Charges
17. Cluberz Commission
18. Platform Fee
19. Total Amount

**Invoice**
- Downloadable invoice/receipt for completed reservations.

# Module 15: My Favourites

## Purpose

Allow users to save preferred night clubs, bars, and restaurants for quick access.

## Features

- Add/remove favourites from listings and detail pages
- Quick access to saved night clubs, bars, and restaurants from the My Favourites tab
- Saved items retain their latest availability, pricing, and status
- Saved list cards show club/bar/restaurant name, thumbnail, location, and key pricing/rating
- Card click opens the relevant club, bar, or restaurant detail page
- A checked favourite icon remains visible on each card to remove from favourites

# Module 16: Change Password

## Purpose

Allow users to update their account password securely.

## Fields

- Old Password
- New Password
- Confirm New Password

## Behavior

- New password and confirmation must match before submission
- Password update requires valid old password verification

# Module 17: Logout

## Purpose

Securely log the user out of the customer panel.

## Features

- Logout confirmation modal
- Session/token invalidation
- Redirect to home page
