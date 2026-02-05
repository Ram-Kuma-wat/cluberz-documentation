# Cluberz Documentation

This document combines the Admin Panel, Vendor Panel, and Customer Panel documentation into a single reference.

---

# Admin Panel Documentation

This document provides a module-wise overview of the Admin Panel for the Cluberz platform. It is derived from the vendor and customer panel workflows and focuses on governance, approvals, compliance, and operational oversight.

## Admin Panel Overview

The Admin Panel enables platform teams to:
- Approve vendor onboarding, profile updates, and content changes.
- Monitor events, venues, zones, restaurant setups, and promotions.
- Oversee bookings, payments, payouts, and platform fees.
- Manage customers, support requests, and review moderation.
- Maintain platform content, notifications, and analytics.

---

## 1. Admin Authentication & Role Management

**Purpose:** Securely manage admin access and permissions.

**Key Responsibilities:**
- Admin login and session management.
- Role-based permissions (super admin, manager, support, finance).
- Staff account provisioning and audit logs.

## 2. Vendor Onboarding & Approval

**Purpose:** Approve or reject vendor onboarding requests (Vendor Module 1).

**Key Responsibilities:**
- Review business information, documents, and verification status.
- Approve onboarding completion or request changes.
- Track pending approvals and onboarding progress.

## 3. Vendor Profile & Content Moderation

**Purpose:** Govern vendor profile updates and business content (Vendor Modules 1 & 6).

**Key Responsibilities:**
- Review profile edits, business descriptions, amenities, and policies.
- Approve profile image and cover image changes.
- Maintain compliance with platform guidelines.

## 4. Venue & Zone Governance

**Purpose:** Oversee venue listings and zone configuration (Vendor Modules 3, 17, 18).

**Key Responsibilities:**
- Validate zone types, pricing, occupancy, and amenities.
- Approve or restrict venue-level changes.
- Ensure inventory accuracy across venues.
- Ensure club/bar listings and detail pages reflect approved data:
  - Customer Module 4: [Night Clubs Listing Page](customer-panel-module-4-night-clubs-listing.md)
  - Customer Module 7: [Night Club Detail Page](customer-panel-module-7-night-club-detail.md)

## 5. Restaurant Setup Oversight

**Purpose:** Monitor restaurant-specific configurations (Vendor Module 4).

**Key Responsibilities:**
- Review menu uploads, cuisine lists, and best-selling items.
- Validate slot management and operational hours.
- Approve restaurant amenities and compliance items.
- Ensure restaurant listing/detail pages and reservation slots reflect approved data:
  - Customer Module 5: [Restaurants Listing Page](customer-panel-module-5-restaurants-listing.md)
  - Customer Module 8: [Restaurant Detail Page](customer-panel-module-8-restaurant-detail.md)

## 6. Event & Celebrity Management

**Purpose:** Review event creation and talent associations (Vendor Module 5).

**Key Responsibilities:**
- Approve event details, imagery, and scheduling.
- Validate DJ/celebrity associations.
- Ensure zone-wise pricing aligns with platform rules.
- Ensure event detail pages and booking flows reflect approved event data:
  - Customer Module 9: [Event Detail Page](customer-panel-module-9-event-detail.md)
  - Customer Module 10: [Event Booking Information & Checkout](customer-panel-module-10-event-booking-checkout.md)

## 7. Coupons & Promotions

**Purpose:** Manage event and restaurant discount programs (Vendor Module 8).

**Key Responsibilities:**
- Configure coupon types and scopes.
- Review promotional requests and validity windows.
- Monitor coupon usage and abuse.

## 8. Flairs & Videos Requests

**Purpose:** Process vendor marketing asset requests (Vendor Module 9).

**Key Responsibilities:**
- Review requests and internal discussions.
- Approve/reject requests and assign pricing.
- Upload finalized media and enable downloads.

## 9. Booking Oversight (Events & Tables)

**Purpose:** Monitor customer bookings across the platform (Vendor Modules 10 & 11, Customer Modules 9–14).

**Key Responsibilities:**
- View booking details, guest lists, and status.
- Manage cancellations, refunds, and disputes.
- Track booking trends and capacity usage.

## 10. Payments, Payouts & Platform Fees

**Purpose:** Track financial flows across vendors and customers (Vendor Modules 12 & 22).

**Key Responsibilities:**
- Monitor payment status and payout schedules.
- Review platform fee, tax, and commission breakdowns.
- Handle refunds, disputes, and transaction history.

## 11. Customer Management

**Purpose:** Support customer accounts and authentication (Customer Modules 12–14).

**Key Responsibilities:**
- Review customer profile and verification status.
- Resolve login or OTP issues.
- Track booking history and support interactions.
- Oversee password resets, logout sessions, and saved favourites:
  - Customer Module 12: [Authentication](customer-panel-module-12-authentication.md)
  - Customer Module 13: [User Profile](customer-panel-module-13-user-profile.md)
  - Customer Module 14: [My Bookings](customer-panel-module-14-my-bookings.md)
  - Customer Module 15: [My Favourites](customer-panel-module-15-my-favourites.md)
  - Customer Module 16: [Change Password](customer-panel-module-16-change-password.md)
  - Customer Module 17: [Logout](customer-panel-module-17-logout.md)

## 12. Ratings & Review Moderation

**Purpose:** Maintain review quality and reputation management (Vendor Modules 13 & 24).

**Key Responsibilities:**
- Moderate flagged reviews and content.
- Allow vendor responses where applicable.
- Monitor rating trends and abuse signals.

## 13. Static Pages & CMS

**Purpose:** Manage public-facing static content (Customer Module 11).

**Key Responsibilities:**
- Update About Us, Contact Us, Privacy Policy, Terms & Conditions.
- Publish announcements or platform updates.

## 14. Support & Helpdesk

**Purpose:** Provide platform-level support oversight (Vendor Module 27).

**Key Responsibilities:**
- Track support tickets and SLAs.
- Assign tickets to support teams.
- Maintain knowledge base references.

## 15. Notifications & Communication

**Purpose:** Coordinate platform-wide messaging (Vendor Module 28).

**Key Responsibilities:**
- Send announcements to vendors/customers.
- Configure email/SMS templates.
- Manage notification preferences.

## 16. Analytics & Reporting

**Purpose:** Provide cross-platform performance insights (Vendor Module 26).

**Key Responsibilities:**
- Monitor booking volume, revenue, and retention.
- Export reports for finance and operations.
- Track campaign and promotion performance.

## 17. System Settings & Security

**Purpose:** Configure global settings and security policies.

**Key Responsibilities:**
- Manage platform configurations, payment settings, and policies.
- Review audit logs and access history.
- Enforce password and security requirements.


---

# Vendor Panel Documentation

This document provides a module-wise overview of the Vendor Panel for the Cluberz multivendor booking platform. It is intended for product, engineering, and operations teams responsible for building and maintaining the vendor experience for clubs, bars, lounges, and restaurants.

## 1. Authentication & Onboarding (Profile Management)

**Purpose:** Enable vendor signup, verification, secure login, and complete business profile onboarding.

**Documentation:** See the detailed module guide in [Module 1: Authentication & Onboarding](vendor-panel-module-1-authentication-onboarding.md).

**Key Features:**
- Signup with OTP and email verification.
- Multi-step business profile completion.
- Admin approval workflow.
- Secure login and password recovery.

**Includes:**
- Signup (7-step onboarding).
- Login (password/OTP).
- Forgot password.
- Profile completion status tracking.

**Outcome:** Vendors can securely onboard, complete profiles, and move into review-ready status.

## 2. Dashboard

**Purpose:** Provide a quick overview of business performance and activity.

**Documentation:** See the detailed module guide in [Module 2: Dashboard](vendor-panel-module-2-dashboard.md).

**Key Metrics Displayed:**
- Total Earnings.
- Total Events.
- Event Booking Cancellation Ratio.
- Total Reviews.
- Total Table Reservations.
- Upcoming Table Reservations.
- Table Booking Cancellation Ratio.
- Reservation Combos.

**Outcome:** Vendors can quickly monitor performance and take timely action.

## 3. Zones Management

**Purpose:** Allow businesses to define seating/entry zones used for bookings.

**Documentation:** See the detailed module guide in [Module 3: Zones Management](vendor-panel-module-3-zones-management.md).

**Key Features:**
- Multiple zones per business.
- Zone types (Regular, VIP, VVIP, Couple, etc.).
- Pricing and occupancy configuration.
- Zone-level amenities.

**Includes:**
- Zones listing.
- Add/Edit/Delete zone.
- Zone pricing rules (Couple, Male Stag, Female Stag, Table).
- Smoking and amenities configuration.

**Outcome:** Vendors can configure bookable zones with clear pricing and capacity rules.

## 4. Restaurant Setup

**Purpose:** Configure restaurant-specific menus, amenities, and dining slots.

**Documentation:** See the detailed module guide in [Module 4: Restaurant Setup](vendor-panel-module-4-restaurant-setup.md).

**Key Features:**
- Food menu (multiple images upload).
- Bar menu (multiple images upload).
- Cuisine menu (multiple images upload).
- Best-selling items (rich text editor).
- Restaurant amenities (as defined in onboarding).
- Slot management (breakfast, lunch, dinner).

**Outcome:** Restaurant vendors can publish menus and manage dining slots for bookings.

## 5. Events Management (My Events)

**Purpose:** Allow vendors to create and manage events hosted at their venue.

**Documentation:** See the detailed module guide in [Module 5: Events Management](vendor-panel-module-5-events-management.md).

**Event Categories:**
- All Events.
- Ongoing Events.
- Upcoming Events.
- Past Events.

**Key Features:**
- Add/Edit/Delete events.
- Zone-wise pricing.
- Booking control per zone.
- Cancellation policies.
- DJ/Celebrity association.
- Event gallery and description.

**Outcome:** Vendors can publish events with zone-based pricing and manage bookings across event timelines.

## 6. Business Profile Management

**Purpose:** Allow vendors to view and update their approved business profile.

**Documentation:** See the detailed module guide in [Module 6: Business Profile Management](vendor-panel-module-6-business-profile-management.md).

**Sections:**
- Business Info.
- Contact Info.
- Location Info.
- Amenities.
- Zones Overview.
- Policies & Opening Hours.
- Finance Details.
- Social Media Links.

**Notes:**
- Critical edits may require re-approval.
- Phone number change requires OTP.

**Outcome:** Vendors keep profile information accurate while respecting approval workflows.

## 7. Photos & Gallery

**Purpose:** Manage visual content for business, zones, and events.

**Documentation:** See the detailed module guide in [Module 7: Photos & Gallery](vendor-panel-module-7-photos-gallery.md).

**Galleries:**
- Business Gallery.
- Zones Gallery.
- Event Gallery.

**Features:**
- Image upload.
- Preview.
- Categorization.

**Outcome:** Vendors can maintain up-to-date galleries across business, zone, and event listings.

## 8. Event Coupons

**Purpose:** Create and manage discount coupons for events.

**Documentation:** See the detailed module guide in [Module 8: Event Coupons](vendor-panel-module-8-event-coupons.md).

**Features:**
- Coupon creation.
- Usage limits.
- Validity dates.
- Enable/Disable coupons.
- Usage tracking.

**Event Coupons Fields:**
- Title.
- Uses per person (limit).
- Total uses (limit).
- Start Date.
- End Date.
- Status.
- Created Date.
- Actions (Edit/Delete/View uses).

**Outcome:** Vendors can configure event discounts with clear usage controls and tracking.

## 9. Flairs & Videos

**Purpose:** Allow vendors to request promotional materials from admin.

**Documentation:** See the detailed module guide in [Module 9: Flairs & Videos](vendor-panel-module-9-flairs-videos.md).

**Features:**
- New request submission.
- Status tracking.
- Preview with watermark.
- Paid download after admin approval.

**Outcome:** Vendors can request, review, and purchase approved promotional media.

## 10. Event Bookings

**Purpose:** Allow vendors to manage customer bookings for events.

**Documentation:** See the detailed module guide in [Module 10: Event Bookings](vendor-panel-module-10-event-bookings.md).

**Booking Categories:**
- Upcoming Bookings.
- Ongoing Bookings.
- Past Bookings.
- Cancelled Bookings.

**Features:**
- Booking details view.
- Guest list.
- Payment status.
- Check-in tracking.

**Outcome:** Vendors can monitor event booking status and guest attendance in one place.

## 11. Table Reservation Bookings (Conditional)

**Purpose:** Manage restaurant table reservations.

**Documentation:** See the detailed module guide in [Module 11: Table Reservation Bookings](vendor-panel-module-11-table-reservation-bookings.md).

**Reservation Categories:**
- New Reservations.
- Past Reservations.
- Cancelled Reservations.

**Features:**
- Reservation detail view.
- Slot & guest count.
- Payment & discount breakdown.
- Check-in status.

**Outcome:** Vendors can track restaurant reservations and payment details by slot.

## 12. Earnings & Transactions

**Purpose:** Track business earnings and withdrawals.

**Documentation:** See the detailed module guide in [Module 12: Earnings & Transactions](vendor-panel-module-12-earnings-transactions.md).

**Earnings Types:**
- Event Earnings.
- Table Reservation Earnings (restaurant-only).

**Features:**
- Transaction history.
- Balance tracking.
- Auto-generated transaction IDs.

**Outcome:** Vendors can review earnings and transfer timelines with transaction records.

## 13. Ratings & Reviews

**Purpose:** Display customer feedback for business improvement and trust.

**Documentation:** See the detailed module guide in [Module 13: Ratings & Reviews](vendor-panel-module-13-ratings-reviews.md).

**Features:**
- List of ratings & reviews.
- Read-only access.
- Chronological ordering.

**Outcome:** Vendors can monitor feedback trends without editing customer reviews.

## 14. Contact Us

**Purpose:** Enable vendors to reach platform support.

**Documentation:** See the detailed module guide in [Module 14: Contact Us](vendor-panel-module-14-contact-us.md).

**Features:**
- Contact form.
- Support communication details.
- Social media links for Cluberz.

**Outcome:** Vendors can submit support requests and access official contact channels.

## 15. Security & Password

**Purpose:** Maintain account security.

**Documentation:** See the detailed module guide in [Module 15: Security & Password](vendor-panel-module-15-security-password.md).

**Features:**
- Change password.
- Old password verification.
- Password strength validation.

**Outcome:** Vendors can keep their account secure with validated password changes.

## 16. Logout

**Purpose:** Securely end vendor session.

**Documentation:** See the detailed module guide in [Module 16: Logout](vendor-panel-module-16-logout.md).

**Features:**
- Logout confirmation.
- Token/session invalidation.
- Redirect to login page.

**Outcome:** Vendors can safely sign out from the platform.

## 17. Venue Management

**Purpose:** Allow vendors to manage venue listings, branding, and amenities.

**Key Capabilities:**
- Create and edit venue profiles (description, category, capacity).
- Upload venue photos, logos, and media galleries.
- Manage amenities (parking, smoking zone, live music, etc.).
- Define operational hours and holiday closures.
- Multi-branch support for vendors with multiple venues.

**Outcome:** Vendors maintain accurate venue listings that customers can discover and book.

## 18. Table / Space Inventory Management

**Purpose:** Configure booking units such as tables, sections, VIP zones, or private lounges.

**Key Capabilities:**
- Define inventory types (tables, rooms, zones, sections).
- Set capacity, minimum spend, and cover charges per inventory unit.
- Availability configuration by day/time slots.
- Inventory tagging (VIP, family, smoking, premium view).
- Bulk inventory creation and duplication for efficiency.

**Outcome:** Clear inventory setup ensures availability and pricing accuracy in customer bookings.

## 19. Pricing & Offers Management

**Purpose:** Provide flexible pricing rules and promotional tools.

**Key Capabilities:**
- Base pricing per table/space.
- Dynamic pricing by day/time/season.
- Discounts and promotional offers (flat/percentage).
- Coupon codes with validity windows.
- Minimum spend and service charge rules.

**Outcome:** Vendors can optimize pricing and attract customers through offers.

## 20. Booking Management

**Purpose:** Manage incoming reservations and booking workflows.

**Key Capabilities:**
- Real-time booking notifications (email/SMS/in-app).
- Booking approval/rejection with optional notes.
- Automatic booking confirmations for instant-book venues.
- Reschedule and cancellation handling.
- Walk-in booking creation by staff.
- Booking lifecycle status tracking (pending, confirmed, completed, cancelled).

**Outcome:** Vendors can effectively manage booking flow and service delivery.

## 21. Customer Management

**Purpose:** Provide vendors insight into customer details and booking history.

**Key Capabilities:**
- Customer profiles linked to bookings.
- Customer contact details and preferences.
- Booking history and spend overview.
- VIP tagging and loyalty segmentation.
- Notes and internal remarks.

**Outcome:** Vendors can personalize service and improve customer retention.

## 22. Payment & Payout Management

**Purpose:** Manage vendor earnings, settlements, and transaction history.

**Key Capabilities:**
- Booking payment tracking (paid, pending, failed).
- Commission and platform fee breakdown.
- Wallet balance and payout schedules.
- Transaction ledger with downloadable invoices.
- Refund processing rules and tracking.

**Outcome:** Transparent financial management builds vendor trust and operational clarity.

## 23. Staff & Role Management

**Purpose:** Allow vendors to manage internal staff access.

**Key Capabilities:**
- Create staff accounts (managers, reception, finance).
- Role-based permissions (view-only, bookings, finance).
- Access logs and activity tracking.
- Two-factor authentication for sensitive roles.

**Outcome:** Secure access control for internal vendor teams.

## 24. Review Responses & Moderation

**Purpose:** Manage vendor responses and moderation actions for customer feedback.

**Notes:**
- Read-only ratings & reviews list is in Module 13.

**Key Capabilities:**
- View ratings and customer reviews.
- Respond to reviews publicly.
- Review analytics (average rating trends).
- Flag inappropriate reviews for moderation.

**Outcome:** Vendors can manage reputation and improve service quality.

## 25. Promotions & Marketing Tools

**Purpose:** Enable vendors to run marketing campaigns and boost visibility.

**Key Capabilities:**
- Featured listing requests.
- Sponsored banner placements.
- Event promotion listings.
- Campaign analytics (impressions, bookings).

**Outcome:** Vendors can increase bookings through platform marketing tools.

## 26. Analytics & Reporting

**Purpose:** Provide insights into performance and operational metrics.

**Key Capabilities:**
- Booking volume trends and peak hours.
- Revenue and payout summaries.
- Customer repeat rate and retention.
- Offer performance reports.
- Exportable CSV/PDF reports.

**Outcome:** Vendors make data-driven decisions to grow business.

## 27. Support & Helpdesk

**Purpose:** Offer assistance and issue resolution for vendors.

**Key Capabilities:**
- Ticket creation and tracking.
- Knowledge base access.
- Live chat or support contact options.
- SLA and resolution tracking.

**Outcome:** Vendors receive timely support to minimize operational disruptions.

## 28. Notifications & Communication

**Purpose:** Keep vendors informed of bookings, payouts, and updates.

**Key Capabilities:**
- In-app notifications dashboard.
- Email and SMS alerts for critical updates.
- Broadcast announcements from admin.
- Notification preferences management.

**Outcome:** Vendors stay updated and can respond quickly to changes.

---

## Additional Notes

- This documentation is focused on the Vendor Panel (Business Panel) in the Cluberz platform.
- Admin Panel and Customer Panel documentation are maintained separately.
- See the [Admin Panel Documentation](admin-panel.md) for platform governance workflows.
- Modules can be expanded into detailed functional and technical specifications during development.


---

# Module 1: Authentication & Onboarding (Profile Management)

## Purpose
Enable vendor signup, verification, secure login, and complete business profile onboarding for clubs, bars, lounges, and restaurants.

## Scope
This module covers the entire authentication and onboarding journey, including registration, OTP/email verification, multi-step profile completion, admin approval, secure login, and password recovery.

## Roles Involved
- **Vendor Owner**: Primary account holder completing onboarding.
- **Vendor Staff**: Optional users added after approval (covered in Staff module).
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
- Accessibility Options (Wheelchair Access, Elevator)

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
- Limit 10 gallery images per venue, plus 1 profile image and 1 cover photo.
- Maximum file size: 5 MB per image.

### Step 7: Policies and Operation Hours
**Purpose:** Set venue policies and opening hours.

**Fields**
- Cancellation Policy (required)
- Entry Policy (optional)
- Opening Hours (per day)
- Holiday Closures (optional)

**Instructions**
- Validate opening hours format (e.g., 10:00-23:00).
- Apply closures to booking availability.

### Step 8: Finance & Legal
**Purpose:** Configure payout and legal compliance details.

**Fields**
- Business License (required, PDF/JPG)
- Owner ID Proof (required, PDF/JPG)
- Venue Permit (optional)
- Account Holder Name (required)
- Bank Name (required)
- Account Number (required)
- IFSC/SWIFT Code (required)
- Payout Currency (required)

**Instructions**
- File size limit: 5 MB per file.
- Accepted formats: PDF, JPG, PNG.
- Account number should be masked on display.

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


---

# Module 2: Dashboard

## Purpose
Provide a quick overview of business performance and activity for vendor owners immediately after login.

## Scope
This module focuses on the main dashboard landing experience, presenting key performance indicators, operational highlights, and actionable alerts related to events and table reservations.

## Roles Involved
- **Vendor Owner**: Views overall business performance.

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


---

# Module 3: Zones Management

## Purpose
Allow businesses to define seating/entry zones used for bookings and pricing control.

## Scope
This module manages all zone configuration for eligible venues, including zone types, capacity rules, pricing rules, and amenities (such as smoking). It drives how bookings are categorized and priced.

**Availability Rule:** Zones management is available only for businesses registered as clubs, bars, or lounges. Businesses registered solely as restaurants do not see or use this module.

## Roles Involved
- **Vendor Owner**: Configures business zones and pricing.

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


---

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


---

# Module 5: Events Management (My Events)

## Purpose
Allow vendors to create and manage events hosted at their venue.

## Scope
This module handles event creation, categorization, pricing per zone, booking controls, cancellation policies, and event media content.

## Roles Involved
- **Vendor Owner**: Creates and publishes events.

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


---

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
- Accessibility Options

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
- Opening hours use the format 10:00-23:00.

---

## Finance Details

**Fields**
- Account Holder Name
- Bank Name
- Account Number
- IFSC/SWIFT Code
- Payout Currency

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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

See the detailed module guide in [Module 1: Global Layout & Navigation](customer-panel-module-1-global-layout-navigation.md).

## Module 2: Location Selection

See the detailed module guide in [Module 2: Location Selection](customer-panel-module-2-location-selection.md).

## Module 3: Home Page

See the detailed module guide in [Module 3: Home Page](customer-panel-module-3-home-page.md).

## Module 4: Night Clubs Listing Page

See the detailed module guide in [Module 4: Night Clubs Listing Page](customer-panel-module-4-night-clubs-listing.md).

## Module 5: Restaurants Listing Page

See the detailed module guide in [Module 5: Restaurants Listing Page](customer-panel-module-5-restaurants-listing.md).

## Module 7: Night Club Detail Page

See the detailed module guide in [Module 7: Night Club Detail Page](customer-panel-module-7-night-club-detail.md).

## Module 8: Restaurant Detail Page

See the detailed module guide in [Module 8: Restaurant Detail Page](customer-panel-module-8-restaurant-detail.md).

## Module 9: Event Detail Page

See the detailed module guide in [Module 9: Event Detail Page](customer-panel-module-9-event-detail.md).

## Module 10: Event Booking Information & Checkout

See the detailed module guide in [Module 10: Event Booking Information & Checkout](customer-panel-module-10-event-booking-checkout.md).

## Module 11: Static Pages

See the detailed module guide in [Module 11: Static Pages](customer-panel-module-11-static-pages.md).

## Module 12: Authentication (Customer)

See the detailed module guide in [Module 12: Authentication (Customer)](customer-panel-module-12-authentication.md).

## Module 13: User Profile

See the detailed module guide in [Module 13: User Profile](customer-panel-module-13-user-profile.md).

## Module 14: My Bookings

See the detailed module guide in [Module 14: My Bookings](customer-panel-module-14-my-bookings.md).

## Module 15: My Favourites

See the detailed module guide in [Module 15: My Favourites](customer-panel-module-15-my-favourites.md).

## Module 16: Change Password

See the detailed module guide in [Module 16: Change Password](customer-panel-module-16-change-password.md).

## Module 17: Logout

See the detailed module guide in [Module 17: Logout](customer-panel-module-17-logout.md).


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

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


---

# Module 17: Logout

## Purpose

Securely log the user out of the customer panel.

## Features

- Logout confirmation modal
- Session/token invalidation
- Redirect to home page
