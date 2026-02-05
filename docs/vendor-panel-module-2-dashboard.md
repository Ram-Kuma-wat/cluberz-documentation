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
**Purpose:** Track discount-based bundled reservation combinations (e.g., 4% off for 3 couples, 6% off for 2 couples + 2 male stags).

**Fields**
- Combo Name (bundle definition)
- Discount Percentage
- Total Bookings
- Revenue Contribution

**Instructions**
- Sort by highest bookings first.
- Show at least top 5 combos.
- Display the discount rule alongside each combo.

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
