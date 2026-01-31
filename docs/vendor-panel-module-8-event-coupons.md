# Module 8: Event Coupons

## Purpose
Create and manage discount coupons for events.

## Scope
This module supports coupon creation, usage limits, validity windows, enable/disable controls, and usage tracking for event bookings.

## Features
- Coupon creation
- Usage limits
- Validity dates
- Enable/Disable coupons
- Usage tracking

---

## Event Coupons List

**Purpose:** Provide a list view of all coupons.

**Fields**
- Title
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
- Uses per person (limit)
- Total uses (limit)
- Start Date
- End Date
- Status (Enabled/Disabled)

**Instructions**
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
