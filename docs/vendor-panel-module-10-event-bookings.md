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
