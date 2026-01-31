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
- Event Image
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
- Validate image uploads (JPG/PNG, max 10 images + 1 cover).
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
