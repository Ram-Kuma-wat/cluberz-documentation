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

## Add Event

**Purpose:** Create a new event listing.

**Required Fields**
- Event Name
- Event Category/Type
- Event Date
- Start Time / End Time
- Venue Location (auto-filled for venue)
- Base Description

**Optional Fields**
- DJ/Celebrity Name
- Event Gallery (multiple images)
- Cover Image
- Tags (e.g., DJ Night, Ladies Night)

**Instructions**
- Prevent overlapping event schedules for the same venue.
- Validate image uploads (JPG/PNG, max 10 images + 1 cover).

---

## Zone-wise Pricing

**Purpose:** Configure pricing per zone for the event.

**Fields**
- Zone Name
- Price per Category (Couple, Male Stag, Female Stag, Table)
- Minimum Spend (optional)
- Max Bookings per Zone

**Instructions**
- Use existing zone definitions from Zones Management.
- Enforce male stag limits and ratios if configured in zone rules.

---

## Booking Control Per Zone

**Purpose:** Limit availability per zone.

**Fields**
- Total Slots per Zone
- Reserved Slots
- Remaining Slots (auto-calculated)

**Instructions**
- Block bookings when zone capacity is reached.
- Allow vendors to close bookings manually.

---

## Cancellation Policies

**Purpose:** Define refund and cancellation rules.

**Fields**
- Cancellation Window (hours before event)
- Refund Percentage
- Non-refundable Flag

**Instructions**
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
