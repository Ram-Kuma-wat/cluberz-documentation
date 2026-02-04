# Cluberz Admin Panel Documentation

This document consolidates the admin panel responsibilities and workflows derived from the final vendor and customer panel documentation. It provides a detailed reference for governance, compliance, and operational oversight across the Cluberz platform.

## 1. Admin Panel Access

### 1.1 Login
- Email
- Password
- 2F authentication (if enabled from profile after login)

### 1.2 Forgot Password
- Enter email address
- Reset password using the link sent over mail

## 2. Dashboard

### 2.1 Box Counts at Top
- Total Clubs
- Total Customers
- Total Events
- Total Bookings

### 2.2 Recent Bookings (List)
- Snapshot of recent bookings with status and quick access to details.
- Booking ID, booking type (event/table), customer name, business name.
- Event/reservation date, booking status, payment status, and net amount.
- Quick actions: view booking detail, open customer profile, open business profile.

### 2.3 Upcoming Events
- Upcoming event list with dates and business references.
- Event name, business, city, start time, zone summary, and status.
- Quick actions: view event detail, edit/approve, mark featured.

## 3. Customers

### 3.1 Customer List
- Search, filter, and export controls (city, status, signup date).
- Name
- Email
- Phone Number
- Status (Enable/Disable toggle button)
- Created Date
- Actions
  - Delete
  - View Detail

### 3.2 Customer Detail
- Basic Info
- Verification status (email/phone)
- Saved favourites (clubs/bars/restaurants/events)
- Bookings (bookings of this user)
- Reviews (review given to businesses)

## 4. Manage Clubs

### 4.1 Business Clubs
List of business clubs (added by admin or admin users):
- Search, filter, and sort by type, city, status, or created date.
- Business Name
- Phone
- Type (lounge, bar, night club, restaurant)
- State
- City
- Status
- Created Date
- Actions (View detail/Approve/Reject/Disable/Delete)

#### 4.1.1 Business Club Detail View
- Profile summary (business name, type, status, premium flag)
- Contact info (business contact, authorized person, email, phone)
- Location info (state, city, address, map reference)
- Amenities, zones overview, and pricing summary
- Policies and opening hours
- Finance details and settlement configuration
- Social media links and gallery assets
- Approval history and admin notes

### 4.2 Add Clubs
Admin-created club form fields:
- Business Name
- Email
- Business Contact Number
- Authorized Person Name
- Authorized Person Contact Number
- Business Types (multi-select from night club, bar, lounge, restaurant)
- Business Founded Date
- State (dropdown)
- City (dropdown based on selected state)
- Property Address (auto complete Google locations)
- Password
- Confirm Password
- Status (Active/Inactive)

Post-creation actions:
- Send credentials to business contact
- Set initial approval status or mark as verified
- Assign internal admin owner

### 4.3 Claimed Clubs
List of claimed clubs:
- Business Name
- Claimed Property
- Email
- Phone
- State
- City
- Created Date
- Actions (View detail/Approve/Reject/Delete)

Claim review details:
- Claim reason and proof documents
- Ownership verification checklist
- Admin notes and approval history

### 4.4 New Listing Requests
List of new listing requests:
- Business Name
- Email
- Phone
- State
- City
- Created Date
- Actions (View detail/Approve/Reject/Delete)

Request detail view:
- Business info, contact info, and location
- Uploaded business proof (license, GST, ID)
- Requested business types and opening hours

### 4.5 Verified Clubs
List of verified clubs/businesses:
- Business Name
- Email
- Phone
- Status (enable/disable toggle)
- State
- City
- Is Premium (toggle)
- Created Date
- Actions (View detail/Edit/Disable/Delete)

Premium management:
- Toggle premium badge
- Configure premium start/end dates
- Track premium billing notes

## 5. Events & Promotions
### 5.1 Event Approvals
- Event title, venue, date/time, city, and status.
- Zone/ticket pricing (couple/stag/table), cover amounts, and capacity.
- Event gallery, banner assets, and lineup/DJ details.
- Actions: approve, reject, request edits, or disable.

### 5.2 Promotions & Coupons
- Coupon code, type (events/restaurants), and scope (all/specific).
- Validity windows, usage limits, and discount rules.
- Targeting (city, venue, event, customer segment).

### 5.3 Featured Content
- Manage featured events and promoted venues.
- Control homepage banners and promotional tiles.
- Schedule start/end dates for featured placements.

## 6. Bookings & Check-ins
### 6.1 Event Bookings
- Upcoming, ongoing, past, cancelled bookings with filters.
- Booking detail: booking ID, customer, event, zones, tickets, totals.
- Guest list verification and check-in logs.

### 6.2 Table Reservations
- Upcoming, past, cancelled reservations.
- Reservation detail: slot, guest count, pricing, discounts, taxes.
- Check-in status and no-show handling.

### 6.3 Disputes & Adjustments
- Flagged bookings, refund requests, and dispute notes.
- Actions: approve refund, partial adjustment, or reject.

## 7. Payments, Payouts & Platform Fees
### 7.1 Payments Overview
- Payment gateway status, success/failure logs.
- Transaction IDs, gross amounts, taxes, and fees.

### 7.2 Payouts & Settlements
- Auto-settlement timelines for events and table bookings.
- Settlement status (pending/processed/held).
- Commission, platform fee, and net pay breakdown.

### 7.3 Refunds & Chargebacks
- Refund requests, reasons, and approval status.
- Adjusted ledger entries and audit trail.

## 8. Ratings & Reviews
- Review list with rating, customer name, venue, and created date.
- Moderate flagged reviews or inappropriate content.
- Enable vendor responses where applicable.
- Track rating trends and abuse signals.

## 9. Content & CMS Management
- Update About Us, Contact Us, Privacy Policy, and Terms & Conditions.
- Publish announcements, banners, and policy updates.
- Maintain SEO-friendly content consistency.
- Manage FAQ entries and static help resources.

## 10. Support & Helpdesk
- Track support tickets and SLAs.
- Assign tickets to support teams.
- Maintain knowledge base references.
- Categorize tickets (booking, payment, account, listing).

## 11. Notifications & Communication
- Send announcements to vendors/customers.
- Configure email/SMS templates and templates for booking flows.
- Manage notification preferences and throttling.
- Schedule bulk notifications and targeted campaigns.

## 12. Analytics & Reporting
- Monitor booking volume, revenue, and retention.
- Export reports for finance and operations.
- Track promotion performance and customer engagement.
- City-level and category-level dashboards (clubs/bars/restaurants).

## 13. System Settings & Security
- Configure payment settings and platform policies.
- Manage role permissions, access history, and audit logs.
- Enforce security standards and compliance checks.
- Configure 2FA requirements, password policies, and session timeouts.
