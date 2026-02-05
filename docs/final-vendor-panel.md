# Cluberz Vendor Panel Documentation

This document consolidates all vendor panel modules into one reference.

# Module 1: Authentication & Onboarding (Profile Management)

## Purpose
Enable vendor signup, verification, secure login, and complete business profile onboarding for clubs, bars, lounges, and restaurants.

## Scope
This module covers the entire authentication and onboarding journey, including registration, OTP/email verification, multi-step profile completion, admin approval, secure login, and password recovery.

## Roles Involved
- **Vendor Owner**: Primary account holder completing onboarding.
- **Admin Reviewer**: Approves or rejects vendor onboarding submissions.

## Key Features
- Signup with OTP and email verification.
- Multi-step business profile completion (9-step onboarding).
- Admin approval workflow.
- Secure login with password/OTP options.
- Password recovery and reset.
- Profile completion status tracking.

---

## Onboarding Flow (9-Step Signup)

### Step 1: Account Setup
**Purpose:** Create initial vendor account credentials.

**Fields**
- Full Name (required)
- Email Address (required, unique)
- Mobile Number (required, unique)
- Password (required, min 8 chars, 1 uppercase, 1 number)
- Accept Terms & Conditions (required checkbox)

**Instructions**
- Email and mobile must not already exist in the system.
- Password is stored hashed; never display it back to user.

### Step 2: OTP & Email Verification
**Purpose:** Verify ownership of contact details.

**Fields**
- OTP Code (SMS, 6-digit)
- Email Verification Link (auto-generated)

**Instructions**
- OTP expires in 5 minutes, max 3 resend attempts.
- Email verification link expires in 24 hours.
- Both SMS OTP and email verification are required before proceeding.

### Step 3: Business Info
**Purpose:** Capture core business details.

**Fields**
- Business Name (required)
- Business Type (club/bar/lounge/restaurant)
- Business Registration Number (optional)
- GST/VAT Number (optional)
- Primary Contact Name (required)
- Primary Contact Phone (required)

**Instructions**
- Business name should be displayed publicly.
- Validate phone number format per country.

### Step 4: Location Info
**Purpose:** Register venue location for discovery and compliance.

**Fields**
- Address Line 1 (required)
- Address Line 2 (optional)
- City (required)
- State/Province (required)
- Country (required)
- Postal Code (required)
- Map Pin / Geo Coordinates (required)

**Instructions**
- Use map pinning for accurate geo coordinates.
- Postal code must match the selected country format.

### Step 5: Amenities
**Purpose:** Capture core amenities offered by the venue.

**Fields**
- Amenity Checklist (Parking, Wi-Fi, Smoking, Live Music, Dance Floor, Outdoor Seating)

**Instructions**
- Use the same amenity list across modules for consistency.
- Amenities are visible on customer listings.

### Step 6: Photos
**Purpose:** Upload venue photos for listings and verification.

**Fields**
- Profile Image (required)
- Cover Photo (required)
- Gallery Images (multiple uploads)

**Instructions**
- Accept JPG/PNG uploads.
- No fixed limit on gallery images; support multiple uploads.
- Maximum file size: 5 MB per image.

### Step 7: Policies and Operation Hours
**Purpose:** Set venue policies and opening hours.

**Fields**
- Cancellation Policy (required)
- Entry Policy (optional)
- Opening Hours (per day)
- Holiday Closures (optional)

**Instructions**
- Validate opening hours format using a hyphen-minus (e.g., 10:00-23:00).
- Apply closures to booking availability.

### Step 8: Finance & Legal
**Purpose:** Configure payout and legal compliance details.

**Fields**
- Business License (required, PDF/JPG)
- Owner ID Proof (required, PDF/JPG)
- Venue Permit (optional)
- Bank Name (dropdown, required)
- Bank Country (dropdown, required)
- Account Holder Name (required)
- Account Number (required)
- IFSC Code (required for domestic accounts in India)
- SWIFT Code (required for international accounts)
- Upload Passbook / Cancelled Cheque (required)
- Image Preview (auto-generated after upload)
- PAN Holder Name (required)
- PAN Number (required)
- Do you have TAN? (Yes/No)
    - select No if the business does not deduct tax at source or does not require a TAN
    - TAN Number (required when Yes)
- GST Number (required for GST-registered businesses in India, optional otherwise)
- Property Type (Owned/Leased)
- Upload Supporting Document (PDF, required)

**Instructions**
- File size limit: 5 MB per file.
- Accepted formats: PDF, JPG, PNG.
- Account number should be masked on display.
- Bank details listed above include the required Bank Name, Country, and IFSC/SWIFT fields.
- Bank list is maintained by the admin team; vendors select from supported banks.
- Bank Country determines whether IFSC (domestic) or SWIFT (international) is required.

### Step 9: Review & Submit
**Purpose:** Confirm the details and submit for approval.

**Fields**
- Confirmation checkbox: “I confirm all details are accurate.”
- Submit button

**Instructions**
- Display a summary of all entered information.
- Once submitted, profile status changes to **Pending Review**.

---

## Login

### Password Login
**Fields**
- Email or Mobile Number
- Password

**Instructions**
- Lock account for 15 minutes after 5 failed attempts.
- Offer “Login with OTP” as an alternative.
- Restrict dashboard access until profile status is **Approved**; unapproved vendors are redirected to onboarding.

### OTP Login
**Fields**
- Mobile Number
- OTP Code (6-digit)

**Instructions**
- OTP expires in 5 minutes.
- Maximum 3 OTP requests per 15 minutes.
- Restrict dashboard access until profile status is **Approved**; unapproved vendors are redirected to onboarding.

---

## Forgot Password

**Flow**
1. User submits email or mobile number.
2. System sends OTP or reset link.
3. User sets a new password.

**Password Rules**
- Minimum 8 characters.
- Must include 1 uppercase letter and 1 number.
- Must be different from last 3 passwords.

---

## Profile Completion Status Tracking

**Status States**
- Draft
- Pending Review
- Approved
- Rejected

**Status Triggers**
- **Draft:** User has not completed all steps.
- **Pending Review:** User submits completed onboarding.
- **Approved:** Admin approves documents and profile.
- **Rejected:** Admin rejects with required correction notes.

**Instructions**
- Show progress indicator (e.g., “Step 4 of 9”).
- Persist the last completed step so returning vendors resume at the next pending step.
- Until approval, vendor logins always land on the onboarding flow with current status.
- Provide admin rejection reason and enable resubmission.

---

## Admin Approval Workflow

**Actions**
- Review business profile and documents.
- Approve or reject with reason.
- Unlock sections for re-edit if needed.

**Notifications**
- Email/SMS notification on approval or rejection.
- In-app notification in vendor panel.

---

## Security & Compliance Requirements

- Use HTTPS for all authentication endpoints.
- Store passwords with strong hashing (bcrypt/argon2).
- Apply rate limiting on OTP and login endpoints.
- Log authentication events for audit.

---

## Outputs

**Successful Completion**
- Vendor account created.
- Profile status set to Pending Review.
- Vendor notified of review status.

**Failure Scenarios**
- Duplicate email/mobile.
- OTP expired or invalid.
- Missing required documents or fields.
- Admin rejection due to invalid compliance documents.

# Module 2: Dashboard

## Purpose
Provide a quick overview of business performance and activity for vendor owners immediately after login.

## Scope
This module focuses on the main dashboard landing experience, presenting key performance indicators, operational highlights, and actionable alerts related to events and table reservations.

## Roles Involved
- **Vendor Owner**: Views overall business performance.
- **Vendor Manager**: Monitors daily activity and upcoming reservations.

## Key Metrics Displayed
- Total Earnings
- Total Events
- Event Booking Cancellation Ratio
- Total Reviews
- Total Table Reservations
- Upcoming Table Reservations
- Table Booking Cancellation Ratio
- Reservation Combos

---

## Dashboard Layout & Sections

### 1. Performance Summary (Top Cards)
**Purpose:** Provide at-a-glance KPIs for business health.

**Fields**
- Total Earnings (currency formatted)
- Total Events (count)
- Total Table Reservations (count)
- Total Reviews (average rating + count)

**Instructions**
- Show data for the selected time range (default: last 30 days).
- Use trend indicators (up/down) for comparison vs previous period.

### 2. Events Overview
**Purpose:** Highlight event performance and cancellations.

**Fields**
- Total Events (count)
- Event Booking Cancellation Ratio (percentage)
- Upcoming Events (count)

**Instructions**
- Cancellation ratio = cancelled event bookings / total event bookings.
- Link to event management for details.

### 3. Table Reservations Overview
**Purpose:** Track table bookings and upcoming reservations.

**Fields**
- Total Table Reservations (count)
- Upcoming Table Reservations (count)
- Table Booking Cancellation Ratio (percentage)

**Instructions**
- Cancellation ratio = cancelled table bookings / total table bookings.
- Upcoming reservations should show next 7 days by default.

### 4. Reservation Combos
**Purpose:** Surface popular reservation package combinations.

**Fields**
- Combo Name
- Total Bookings
- Revenue Contribution

**Instructions**
- Sort by highest bookings first.
- Show at least top 5 combos.

### 5. Reviews Snapshot
**Purpose:** Provide quick view of customer feedback.

**Fields**
- Total Reviews (count)
- Average Rating (1–5)
- Latest Review Snippet

**Instructions**
- Show most recent review with customer name masked.
- Link to full reviews module.

---

## Filters & Controls

**Filters**
- Date Range (Today, Last 7 Days, Last 30 Days, Custom)
- Venue Selector (for multi-venue vendors)

**Instructions**
- Cache dashboard results for faster load.
- Preserve last-used filters when user returns.

---

## Empty & Error States

**Empty State Examples**
- “No reservations yet. Promote your venue to attract bookings.”
- “No events created. Start by adding an event.”

**Error State**
- “Unable to load dashboard metrics. Please try again.”

---

## Notifications & Alerts

**Types**
- High cancellation rate alerts.
- Low ratings alert (average rating < 3).
- Upcoming reservation reminders.

---

## Outputs

**Successful Load**
- All metrics display with updated values.
- Vendor can navigate to deeper modules.

**Failure Scenarios**
- Metrics API timeout.
- Missing data for selected date range.

# Module 3: Zones Management

## Purpose
Allow businesses to define seating/entry zones used for bookings and pricing control.

## Scope
This module manages all zone configuration for eligible venues, including zone types, capacity rules, pricing rules, and amenities (such as smoking). It drives how bookings are categorized and priced.

**Availability Rule:** Zones management is available only for businesses registered as clubs, bars, or lounges. Businesses registered solely as restaurants do not see or use this module.

## Roles Involved
- **Vendor Owner**: Configures business zones and pricing.
- **Vendor Manager**: Maintains zone availability and amenities.

## Key Features
- Multiple zones per business.
- Zone types (Regular, VIP, VVIP, Couple, etc.).
- Pricing and occupancy configuration.
- Zone-level amenities.

## Includes
- Zones listing.
- Add/Edit/Delete zone.
- Zone pricing rules (Couple, Male Stag, Female Stag, Table).
- Smoking and amenities configuration.

---

## Zones Listing

**Purpose:** Provide a searchable list of zones for a venue.

**Fields**
- Zone Name
- Zone Type
- Capacity (min/max)
- Pricing Rule Summary
- Amenities (icons/labels)
- Status (Active/Inactive)

**Instructions**
- Allow filtering by zone type and status.
- Highlight zones with missing pricing rules.

---

## Add Zone

**Purpose:** Create a new zone for bookings.

**Required Fields**
- Zone Name (unique per venue)
- Zone Type (Regular, VIP, VVIP, Couple, Family, etc.)
- Minimum Occupancy
- Maximum Occupancy
- Default Pricing Rule (required)

**Optional Fields**
- Description
- Zone Image
- Amenities (Parking, Smoking, Live Music, DJ, Dance Floor)
- Priority Order (display order in booking flow)

**Instructions**
- Validate max occupancy > min occupancy.
- Zone type must match configured pricing rules.
- Save zone as Active by default.

---

## Edit Zone

**Purpose:** Update existing zone details.

**Instructions**
- Allow editing of type, capacity, pricing, and amenities.
- If zone type changes, revalidate pricing rules.
- Maintain existing bookings; prevent edits that reduce capacity below already confirmed bookings.

---

## Delete Zone

**Purpose:** Remove zones that are no longer used.

**Instructions**
- Soft-delete zones with existing booking history.
- Block deletion if there are upcoming confirmed bookings.
- Provide warning before removal.

---

## Zone Pricing Rules

**Purpose:** Define pricing based on booking category.

**Pricing Types**
- Couple
- Male Stag
- Female Stag
- Table

**Fields**
- Base Price
- Minimum Spend
- Included Guests
- Extra Guest Price
- Service Charge (%)

**Male Stag Limits**
- Limit: No. of male stags allowed.
- Ratio: No. of couples vs no. of male stags.

**Instructions**
- Validate all required pricing types are configured.
- Support day/time-specific overrides if enabled.
- Enforce male stag limits and ratios before confirming bookings.

---

## Smoking & Amenities Configuration

**Purpose:** Capture zone-specific amenities for discovery and filtering.

**Amenities Examples**
- Smoking Allowed (Yes/No)
- Live Music
- DJ
- Dance Floor
- Private Entry
- Outdoor Seating

**Instructions**
- Show amenities badges in customer booking UI.
- Smoking flag must be explicit (Allowed/Not Allowed).

---

## Outputs

**Successful Completion**
- Zone available in booking inventory.
- Pricing applied correctly for booking categories.

**Failure Scenarios**
- Duplicate zone name.
- Missing required pricing rules.
- Invalid capacity ranges.

# Module 4: Restaurant Setup

## Purpose
Configure restaurant-specific menus, amenities, and dining slots for businesses registered as restaurants.

## Scope
This module is available only for businesses registered as restaurants or with restaurant as a business type. It manages menus, best-selling items content, restaurant amenities, and meal slot schedules.

## Availability Rule
- Visible only when the business type includes **Restaurant**.
- Hidden for businesses registered exclusively as clubs, bars, or lounges without restaurant selection.

## Roles Involved
- **Vendor Owner**: Sets up menus, amenities, and slots.
- **Vendor Manager**: Maintains menu updates and slot changes.

## Key Features
- Food menu (multiple images upload).
- Bar menu (multiple images upload).
- Cuisine menu (multiple images upload).
- Best-selling items (rich text editor).
- Restaurant amenities (same amenities list from onboarding).
- Slot management (breakfast, lunch, dinner).

---

## Menu Management

### Food Menu
**Purpose:** Upload and maintain the primary restaurant menu.

**Fields**
- Menu Title
- Menu Images (multiple uploads)
- Effective Date

**Instructions**
- Accept JPG/PNG/PDF uploads.
- Limit 10 images per menu set.
- Display the most recent menu first.

### Bar Menu
**Purpose:** Upload bar-specific menus when applicable.

**Fields**
- Menu Title
- Menu Images (multiple uploads)
- Effective Date

**Instructions**
- Optional for restaurants without alcohol service.
- Use the same upload limits as Food Menu.

### Cuisine Menu
**Purpose:** Highlight cuisine-focused menus (e.g., Italian, Indian).

**Fields**
- Cuisine Name
- Menu Images (multiple uploads)
- Effective Date

**Instructions**
- Support multiple cuisine entries.
- Use the same upload limits as Food Menu.

---

## Best-Selling Items

**Purpose:** Showcase popular dishes and recommendations.

**Fields**
- Rich Text Content (editor)

**Instructions**
- Allow formatting (bold, bullets, links).
- Keep content concise for dashboard display.

---

## Restaurant Amenities

**Purpose:** Display dining amenities consistent with onboarding.

**Fields**
- Amenity Checklist (e.g., Parking, Wi-Fi, Outdoor Seating, Family Friendly, Live Music)

**Instructions**
- Use the same amenity list as onboarding for consistency.
- Visible to customers in restaurant listing details.

---

## Slot Management

**Purpose:** Configure dining slots for reservations.

**Slot Types**
- Breakfast
- Lunch
- Dinner

**Fields**
- Slot Name
- Start Time
- End Time
- Max Reservations per Slot

**Instructions**
- Prevent overlapping slots within the same day.
- Apply slot configuration across selected weekdays.
- Default slot durations can be prefilled by admin settings.

---

## Outputs

**Successful Completion**
- Menus displayed on restaurant listing.
- Best-selling items visible on restaurant profile.
- Slots available for customer booking.

**Failure Scenarios**
- Missing required menu images.
- Invalid slot time ranges.
- Overlapping slot configurations.

# Module 5: Events Management (My Events)

## Purpose
Allow vendors to create and manage events hosted at their venue.

## Scope
This module handles event creation, categorization, pricing per zone, booking controls, cancellation policies, and event media content.

## Roles Involved
- **Vendor Owner**: Creates and publishes events.
- **Vendor Manager**: Manages bookings, pricing, and event updates.

## Event Categories
- All Events
- Ongoing Events
- Upcoming Events
- Past Events

---

## Events Listing

**Purpose:** Provide a categorized view of all events.

**Fields**
- Event Name
- Event Date/Time
- Status (Ongoing/Upcoming/Past)
- Total Bookings
- Primary Zone Pricing

**Instructions**
- Default view is All Events with filters for status.
- Show quick actions for Edit/Delete.

---

## Add/Edit Event

**Purpose:** Create a new event listing.

**Required Fields**
- Event Name
- Event Type (Outdoor/Indoor)
- Event Location
- Event Start Date + Time
- Event End Date + Time
- Event Check-in Date + Time
- Event Profile Image
- Event Cover Image
- Event Description
- Available Zone(s) (multi-select)
- Booking Close Date + Time
- Policies/Rules (select existing or add new)

**Optional Fields**
- Hard Liquor (True/False)
- Kids Allowed (True/False)
- Comedy Show (True/False)
- Live Performance (True/False)
- DJ (select from already added; add more supported)
- Celebrity (select from already added; add more supported)
- Event Hours (auto-calculated from start/end)

**Instructions**
- Prevent overlapping event schedules for the same venue.
- Event hours are derived from the selected start/end date-time range.
- Validate image uploads (JPG/PNG, max 10 images + 1 profile image + 1 cover).
- Allow multiple DJs or celebrities via add-more controls.

---

## Available Zones & Zone-wise Pricing

**Purpose:** Configure pricing per zone for the event.

**Fields**
- Zone Selection (checkbox multi-select)
- Price per Category (Couple, Male Stag, Female Stag, Table)
- Minimum Spend (optional)
- Max Bookings per Zone

**Instructions**
- On zone selection, show editable price fields per category.
- Use existing zone definitions from Zones Management.
- Enforce male stag limits and ratios if configured in zone rules.

---

## Booking Control Per Zone

**Purpose:** Limit availability per zone.

**Fields**
- Total Slots per Zone
- Reserved Slots
- Remaining Slots (auto-calculated)
- Can Booking Be Cancelled (checkbox)
- Cancellation Combos (shown only if cancellation is enabled)

**Instructions**
- Block bookings when zone capacity is reached.
- Allow vendors to close bookings manually.
- If cancellation is enabled, show available cancellation combos for selection.

---

## Cancellation Policies

**Purpose:** Define refund and cancellation rules.

**Fields**
- % Deduct
- Hours Before
- No Refund (toggle)

**Instructions**
- Visible only if cancellations are allowed.
- Display policy at checkout.
- Apply default policy if no custom rule is set.

---

## Event Gallery & Description

**Purpose:** Showcase event details visually.

**Fields**
- Event Description (rich text)
- Gallery Images (multiple uploads)

**Instructions**
- Support basic formatting in description.
- Gallery should include at least 3 images for featured events.

---

## Outputs

**Successful Completion**
- Event visible in upcoming/ongoing lists.
- Zone pricing and booking controls enforced.

**Failure Scenarios**
- Missing required fields.
- Overlapping event schedules.
- Invalid pricing setup.

# Module 6: Business Profile Management

## Purpose
Allow vendors to view and update their approved business profile.

## Scope
This module handles profile updates for approved vendors, including business details, contact data, location, amenities, zones overview, policies, finance, and social links. Some changes trigger re-approval.

## Notes
- Critical edits may require re-approval.
- Phone number change requires OTP verification.
- Field definitions and validation rules align with the onboarding steps in Module 1.

## Sections
1. Business Info
2. Contact Info
3. Location Info
4. Amenities
5. Zones Overview
6. Policies & Opening Hours
7. Finance Details
8. Social Media Links

---

## Business Info

**Fields**
- Business Name
- Business Type
- Registration Number
- GST/VAT Number
- Business Profile Image
- Business Cover Image

**Instructions**
- Changing business type may require re-approval.

---

## Contact Info

**Fields**
- Primary Contact Name
- Primary Contact Phone
- Primary Contact Email

**Instructions**
- Phone number updates require OTP verification.
- Email changes require verification.

---

## Location Info

**Fields**
- Address Line 1
- Address Line 2
- City
- State/Province
- Country
- Postal Code
- Map Pin / Geo Coordinates

**Instructions**
- Location changes may require admin review.

---

## Amenities

**Fields**
- Amenity Checklist (Parking, Wi-Fi, Smoking, Live Music, Dance Floor, Outdoor Seating)

**Instructions**
- Use the same amenity set as onboarding.

---

## Zones Overview

**Fields**
- Zone Name
- Zone Type
- Capacity Range
- Pricing Summary

**Instructions**
- Read-only overview; edits redirect to Zones Management.

---

## Policies & Opening Hours

**Fields**
- Cancellation Policy
- Entry Policy
- Opening Hours (per day)
- Holiday Closures

**Instructions**
- Opening hours use a hyphen-minus format (e.g., 10:00-23:00).

---

## Finance Details

**Fields**
- Account Holder Name
- Bank Name
- Account Number
- IFSC/SWIFT Code

**Instructions**
- Updates may require admin approval.

---

## Social Media Links

**Fields**
- Instagram URL
- Facebook URL
- Website URL
- Google Maps Link

**Instructions**
- Validate URL format.

---

## Outputs

**Successful Completion**
- Profile updates saved.
- Admin review triggered for critical changes.

**Failure Scenarios**
- Invalid contact verification.
- Missing required fields.

# Module 7: Photos & Gallery

## Purpose
Manage visual content for business, zones, and events.

## Scope
This module provides gallery management for different content types, enabling uploads, previews, and album grouping where applicable.

## Galleries
1. Business Gallery
2. Zones Gallery
3. Event Gallery

---

## Business Gallery

**Purpose:** Maintain venue-wide images used across listings and profiles.

**Fields**
- Profile Image
- Cover Image
- Images (multiple uploads)

**Instructions**
- Profile and cover images appear on the public profile and listings.
- Business gallery uses direct image uploads without a title.
- Accept JPG/PNG uploads.
- Provide preview before publishing.

---

## Zones Gallery

**Purpose:** Showcase images specific to each zone.

**Fields**
- Zone Name
- Album Title
- Images (multiple uploads)

**Instructions**
- Images map to the selected zone.
- Album title is required to group images under the zone.

---

## Event Gallery

**Purpose:** Store event-specific media.

**Fields**
- Event Name
- Album Title
- Images (multiple uploads)

**Instructions**
- Allow uploads during event creation and editing.
- Album title is required to group images under the event.
- Mark featured image for event listing.

---

## Features

- Image upload
- Preview before save
- Gallery type selection (business, zone, event)
- Album title for zone and event galleries

---

## Outputs

**Successful Completion**
- Images visible in corresponding listings.
- Galleries updated with album grouping where applicable.

**Failure Scenarios**
- Unsupported file format.

# Module 8: Event Coupons

## Purpose
Create and manage discount coupons for events.

## Scope
This module supports coupon creation, usage limits, validity windows, enable/disable controls, and usage tracking for event and restaurant bookings.

## Features
- Coupon creation
- Usage limits
- Validity dates
- Enable/Disable coupons
- Usage tracking
- Coupon type selection (events, restaurants, or both)
- Coupon scope selection (all or specific events/restaurants)

---

## Event Coupons List

**Purpose:** Provide a list view of all coupons.

**Fields**
- Title
- Coupon Type (Events, Restaurants, or Both)
- Coupon For (All Events, Specific Events, All Restaurants, Specific Restaurants)
- Uses per person (limit)
- Total uses (limit)
- Start Date
- End Date
- Status
- Created Date
- Actions (Edit/Delete/View uses)

**Instructions**
- Allow filtering by status (Active/Expired/Disabled).
- Show usage count vs total limit in list view.

---

## Create/Edit Coupon

**Required Fields**
- Title
- Coupon Type (Events, Restaurants, or Both)
- Coupon For (All Events, Specific Events, All Restaurants, Specific Restaurants)
- Uses per person (limit)
- Total uses (limit)
- Start Date
- End Date
- Status (Enabled/Disabled)

**Instructions**
- If specific events are selected, limit choices to upcoming events.
- If specific restaurants are selected, limit choices to active restaurant listings.
- Start date must be before end date.
- Disable coupons automatically after end date.
- Prevent total uses from being less than current usage.

---

## Usage Tracking

**Purpose:** Track coupon usage over time.

**Fields**
- Total Uses
- Remaining Uses
- Recent Redemptions (date, booking reference)

**Instructions**
- Update usage counts in real time.

---

## Outputs

**Successful Completion**
- Coupons available for event checkout.
- Usage limits enforced.

**Failure Scenarios**
- Invalid date ranges.
- Usage limits exceeded.

# Module 9: Flairs & Videos

## Purpose
Allow vendors to request promotional materials from admin.

## Scope
Vendors submit requests for flairs and videos with summarized details. Admin reviews, approves/rejects, produces media, and assigns a price. Vendors can preview watermarked media and download the final version after payment.

## Features
- New request submission
- Status tracking
- Preview with watermark
- Paid download after admin approval

---

## Request Submission

**Purpose:** Submit a new request for promotional media.

**Fields**
- Request Title
- Request Type (Flairs, Videos, or Both)
- Summary/Brief
- Target Event or Venue (optional)
- Preferred Deadline (optional)

**Instructions**
- Vendors must provide a clear summary of required media.
- Requests start in **Pending Review** status.

---

## Status Tracking

**Statuses**
- Pending Review
- In Discussion
- Approved
- Rejected
- In Production
- Ready for Preview
- Ready for Payment
- Completed

**Instructions**
- Show latest admin notes and decision history.

---

## Admin Review (Vendor View)

**Purpose:** Track admin decisions and next steps.

**Details Shown**
- Approval/Rejection decision
- Admin remarks
- Assigned price (once approved)

**Instructions**
- Approved requests proceed to production.
- Rejected requests can be resubmitted with updates.

---

## Preview with Watermark

**Purpose:** Allow vendors to preview produced media before payment.

**Details**
- Watermarked images/videos
- Preview expiration (if any)

**Instructions**
- Watermark should remain until payment is completed.

---

## Paid Download

**Purpose:** Enable final media download after payment.

**Fields**
- Amount Due
- Payment Status
- Download Links

**Instructions**
- Payment must be confirmed before unlocking non-watermarked files.

---

## Outputs

**Successful Completion**
- Vendor downloads final media without watermark.
- Request status updates to Completed.

**Failure Scenarios**
- Payment failed or pending.
- Request rejected by admin.

# Module 10: Event Bookings

## Purpose
Allow vendors to manage customer bookings for events.

## Scope
This module provides booking visibility across event timelines, with booking detail views, guest lists, payment status, and check-in tracking.

## Booking Categories
1. Upcoming Bookings
2. Ongoing Bookings
3. Past Bookings
4. Cancelled Bookings

---

## Booking List View

**Purpose:** Show bookings grouped by category.

**Fields**
- Booking ID
- Event Name
- Event Date
- Primary Guest Name
- Payment Status
- Booking Status (Upcoming/Ongoing/Past/Cancelled)

**Instructions**
- Allow filtering by category and payment status.

---

## Booking Details

**Fields**
1. Booking ID
2. Booking Date
3. Business (Club/Bar/Restaurant Name)
4. Event Name
5. Location
6. Event Date
7. Primary Guest Name
8. Primary Guest Email
9. Primary Guest Phone
10. Payment Status (Paid/Cancelled/Pending)
11. Table of guests/candidates
    - Zone
    - Type (Couple/Male Stag/Female Stag/Table)
    - Guest Details (names)
    - Ticket
    - Price per Ticket
    - Cover Amount
    - Total Ticket Price
12. Sub Total
13. Discount
14. Tax
15. Club Net Pay

---

## Guest List

**Purpose:** Track attendees per booking.

**Fields**
- Guest Name
- Ticket Type
- Check-in Status

**Instructions**
- Update check-in status at entry.

---

## Payment Status

**Purpose:** Show payment outcomes.

**Statuses**
- Paid
- Pending
- Cancelled

---

## Check-in Tracking

**Purpose:** Track entry for guests.

**Fields**
- Check-in Date/Time
- Checked In By

**Instructions**
- Allow manual overrides with audit trail.

---

## Outputs

**Successful Completion**
- Vendor can track bookings and check-ins by event.

**Failure Scenarios**
- Payment status mismatch.
- Missing guest list data.

# Module 11: Table Reservation Bookings (Conditional)

## Purpose
Manage restaurant table reservations.

## Scope
This module is available for restaurant businesses to track reservation requests, guest counts, payment details, and check-in status.

## Reservation Categories
1. New Reservations
2. Past Reservations
3. Cancelled Reservations

---

## Reservation List View

**Fields**
- Reservation ID
- Restaurant Name
- Reservation Date
- Reservation Slot
- Primary Guest Name
- Payment Status

**Instructions**
- Allow filtering by category and date.

---

## Reservation Booking Details

**Fields**
1. Reservation Detail: Title
2. Reservation ID
3. Booking Date and Time
4. Restaurant Name
5. Reservation Date
6. Reservation Slot
7. Business Location
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
18. Total Amount

---

## Features

- Reservation detail view
- Slot & guest count
- Payment & discount breakdown
- Check-in status

---

## Check-in Status

**Fields**
- Check-in Date/Time
- Checked In By

**Instructions**
- Track check-ins at arrival.

---

## Outputs

**Successful Completion**
- Reservation details visible with payment breakdown.

**Failure Scenarios**
- Missing reservation data.
- Payment status mismatch.

# Module 12: Earnings & Transactions

## Purpose
Track business earnings and withdrawals.

## Scope
This module provides earnings breakdowns for events and restaurant reservations, plus transaction history. Withdrawals are automatic based on booking completion timelines.

## Earnings Types
1. Event Earnings
2. Table Reservation Earnings (restaurant-only)

---

## Event Earnings

**Fields**
1. Booking ID
2. Event Name
3. Amount
4. Date of Booking
5. Comment

---

## Table Reservation Earnings

**Availability:** Only for businesses with the restaurant option.

**Fields**
1. Reservation ID
2. Booking Date
3. Amount
4. Comment

---

## Transaction History

**Fields**
1. Total Earnings (event + restaurant)
2. Withdraw Amount
3. Balance Amount
4. Table of Transaction History
   - Txn ID (auto-generated on transfer)
   - Amount
   - Status (Credit/Withdrawn)
   - Comment
   - Created Date

---

## Transfer Timeline (Auto Payouts)

**Rules**
- Event earnings are transferred within 12-24 hours after the event finishes.
- Table reservation earnings are transferred within 12 hours after the booking time ends.
- Transfers are held if there is an active dispute.

---

## Features
- Transaction history
- Balance tracking
- Auto-generated transaction IDs

---

## Outputs

**Successful Completion**
- Earnings and transfer records visible with timestamps.

**Failure Scenarios**
- Transfer held due to dispute.
- Missing booking references.

# Module 13: Ratings & Reviews

## Purpose
Display customer feedback for business improvement and trust.

## Scope
This module provides a read-only list of ratings and reviews with chronological ordering.

## Features
- List of ratings & reviews
- Read-only access
- Chronological ordering

---

## Ratings & Reviews List

**Fields**
- Review Date
- Customer Name
- Rating (1-5)
- Review Comment
- Booking Reference (optional)

**Instructions**
- Default sort order is newest to oldest.
- Do not allow vendors to edit customer reviews.

---

## Outputs

**Successful Completion**
- Ratings and reviews are visible with timestamps.

**Failure Scenarios**
- Reviews unavailable due to moderation.

# Module 14: Contact Us

## Purpose
Enable vendors to reach platform support.

## Scope
This module provides a contact form and official Cluberz communication details for vendor support queries.

## Features
- Contact form
- Support communication details
- Social media links for Cluberz

---

## Contact Form

**Fields**
- Subject
- Message
- Attachment (optional)

**Instructions**
- Require subject and message before submission.
- Provide confirmation after successful submission.

---

## Support Communication Details

**Fields**
- Support Email
- Support Phone
- Office Address

---

## Social Media Links

**Fields**
- Instagram
- Facebook
- LinkedIn
- X/Twitter

---

## Outputs

**Successful Completion**
- Support request submitted and acknowledged.

**Failure Scenarios**
- Missing required message details.

# Module 15: Security & Password

## Purpose
Maintain account security.

## Scope
This module allows vendors to update passwords with verification and strength checks.

## Features
- Change password
- Old password verification
- Password strength validation

---

## Change Password

**Fields**
- Current Password
- New Password
- Confirm New Password

**Instructions**
- Verify current password before allowing changes.
- Enforce password strength rules (min 8 chars, 1 uppercase, 1 number).
- Block reuse of recent passwords if policy requires.

---

## Outputs

**Successful Completion**
- Password updated and session refreshed.

**Failure Scenarios**
- Incorrect current password.
- Weak password does not meet policy.

# Module 16: Logout

## Purpose
Securely end vendor session.

## Scope
This module handles user sign-out, session invalidation, and redirect to the login page.

## Features
- Logout confirmation
- Token/session invalidation
- Redirect to login page

---

## Logout Flow

**Steps**
1. Vendor clicks Logout.
2. Confirmation prompt appears.
3. On confirmation, invalidate session/token.
4. Redirect to login screen.

---

## Outputs

**Successful Completion**
- Session ended and user redirected to login.

**Failure Scenarios**
- Session invalidation failure.
