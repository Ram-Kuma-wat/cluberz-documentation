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
