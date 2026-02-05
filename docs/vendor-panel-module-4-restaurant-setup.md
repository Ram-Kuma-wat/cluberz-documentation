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
