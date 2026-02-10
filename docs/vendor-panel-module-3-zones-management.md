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

## Add/Edit Zone

**Purpose:** Create or update zone details, pricing, and amenities used for bookings.

**Fields**
- Zone Name
- Zone Type (Regular, VIP, VVIP, Couple, etc. from admin masters)
- Number of this type of zone
- Zone Description
- Smoking Allowed (checkbox)
- Images (Pic 1, Pic 2, Pic 3)
- Zone Details: Base occupancy
- Base Price & Category Pricing
  - Checkboxes for Couple, Male Stag, Female Stag, Table
  - Price per Couple
  - Cover amount per Couple
  - Price per Male Stag
  - Cover amount per Male Stag
  - Male Stag Seats
    - Limit: No. of male stags allowed
    - Ratio: No. of couples vs no. of male stags
  - Price per Female Stag
  - Cover amount per Female Stag
  - Occupancy of table (number)
  - Price per table
  - Cover amount per table
- Zone Amenities (checkboxes for categorized zone amenities)

**Instructions**
- Require at least one booking category before saving pricing.
- Zone types must be selected from admin masters.
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

**Purpose:** Define base pricing, cover amounts, and seat limits per booking category.

**Fields**
- Base Price
- Category checkboxes (Couple, Male Stag, Female Stag, Table)
- Price and cover amount per enabled category
- Table occupancy
- Male Stag limits and ratio

**Instructions**
- Validate that each enabled category has both price and cover amount.
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
- Use categorized amenities from admin masters.
- Show amenities badges in customer booking UI.

---

## Outputs

**Successful Completion**
- Zone available in booking inventory.
- Pricing applied correctly for booking categories.

**Failure Scenarios**
- Duplicate zone name.
- Missing required pricing rules.
- Invalid capacity ranges.
