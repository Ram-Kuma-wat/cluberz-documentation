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
- Opening hours use the hyphen-minus format (e.g., 10:00-23:00).

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
