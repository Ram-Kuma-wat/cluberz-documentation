# Module 1: Authentication & Onboarding (Profile Management)

## Purpose
Enable vendor signup, verification, secure login, and complete business profile onboarding for clubs, bars, lounges, and restaurants.

## Scope
This module covers the entire authentication and onboarding journey, including registration, OTP/email verification, multi-step profile completion, admin approval, secure login, and password recovery.

## Roles Involved
- **Vendor Owner**: Primary account holder completing onboarding.
- **Vendor Staff**: Optional users added after approval (covered in Staff module).
- **Admin Reviewer**: Approves or rejects vendor onboarding submissions.

## Key Features
- Signup with OTP and email verification.
- Multi-step business profile completion (9-step onboarding).
- Admin approval workflow.
- Secure login with password/OTP options.
- Password recovery and reset.
- Profile completion status tracking.

---

## Onboarding Flow (9-Step Signup)

### Step 1: Account Setup
**Purpose:** Create initial vendor account credentials.

**Fields**
- Full Name (required)
- Email Address (required, unique)
- Mobile Number (required, unique)
- Password (required, min 8 chars, 1 uppercase, 1 number)
- Accept Terms & Conditions (required checkbox)

**Instructions**
- Email and mobile must not already exist in the system.
- Password is stored hashed; never display it back to user.

### Step 2: OTP & Email Verification
**Purpose:** Verify ownership of contact details.

**Fields**
- OTP Code (SMS, 6-digit)
- Email Verification Link (auto-generated)

**Instructions**
- OTP expires in 5 minutes, max 3 resend attempts.
- Email verification link expires in 24 hours.
- Both SMS OTP and email verification are required before proceeding.

### Step 3: Business Info
**Purpose:** Capture core business details.

**Fields**
- Business Name (required)
- Business Type (club/bar/lounge/restaurant)
- Business Registration Number (optional)
- GST/VAT Number (optional)
- Primary Contact Name (required)
- Primary Contact Phone (required)

**Instructions**
- Business name should be displayed publicly.
- Validate phone number format per country.

### Step 4: Location Info
**Purpose:** Register venue location for discovery and compliance.

**Fields**
- Address Line 1 (required)
- Address Line 2 (optional)
- City (required)
- State/Province (required)
- Country (required)
- Postal Code (required)
- Map Pin / Geo Coordinates (required)

**Instructions**
- Use map pinning for accurate geo coordinates.
- Postal code must match the selected country format.

### Step 5: Amenities
**Purpose:** Capture core amenities offered by the venue.

**Fields**
- Amenity Checklist (Parking, Wi-Fi, Smoking, Live Music, Dance Floor, Outdoor Seating)
- Accessibility Options (Wheelchair Access, Elevator)

**Instructions**
- Use the same amenity list across modules for consistency.
- Amenities are visible on customer listings.

### Step 6: Photos
**Purpose:** Upload venue photos for listings and verification.

**Fields**
- Profile Image (required)
- Cover Photo (required)
- Gallery Images (multiple uploads)

**Instructions**
- Accept JPG/PNG uploads.
- Limit 10 gallery images per venue, plus 1 profile image and 1 cover photo.
- Maximum file size: 5 MB per image.

### Step 7: Policies and Operation Hours
**Purpose:** Set venue policies and opening hours.

**Fields**
- Cancellation Policy (required)
- Entry Policy (optional)
- Opening Hours (per day)
- Holiday Closures (optional)

**Instructions**
- Validate opening hours format (e.g., 10:00-23:00, using the hyphen-minus character "-").
- Apply closures to booking availability.

### Step 8: Finance & Legal
**Purpose:** Configure payout and legal compliance details.

**Fields**
- Business License (required, PDF/JPG)
- Owner ID Proof (required, PDF/JPG)
- Venue Permit (optional)
- Account Holder Name (required)
- Bank Name (required)
- Account Number (required)
- IFSC/SWIFT Code (required)
- Payout Currency (required)

**Instructions**
- File size limit: 5 MB per file.
- Accepted formats: PDF, JPG, PNG.
- Account number should be masked on display.

### Step 9: Review & Submit
**Purpose:** Confirm the details and submit for approval.

**Fields**
- Confirmation checkbox: “I confirm all details are accurate.”
- Submit button

**Instructions**
- Display a summary of all entered information.
- Once submitted, profile status changes to **Pending Review**.

---

## Login

### Password Login
**Fields**
- Email or Mobile Number
- Password

**Instructions**
- Lock account for 15 minutes after 5 failed attempts.
- Offer “Login with OTP” as an alternative.
- Restrict dashboard access until profile status is **Approved**; unapproved vendors are redirected to onboarding.

### OTP Login
**Fields**
- Mobile Number
- OTP Code (6-digit)

**Instructions**
- OTP expires in 5 minutes.
- Maximum 3 OTP requests per 15 minutes.
- Restrict dashboard access until profile status is **Approved**; unapproved vendors are redirected to onboarding.

---

## Forgot Password

**Flow**
1. User submits email or mobile number.
2. System sends OTP or reset link.
3. User sets a new password.

**Password Rules**
- Minimum 8 characters.
- Must include 1 uppercase letter and 1 number.
- Must be different from last 3 passwords.

---

## Profile Completion Status Tracking

**Status States**
- Draft
- Pending Review
- Approved
- Rejected

**Status Triggers**
- **Draft:** User has not completed all steps.
- **Pending Review:** User submits completed onboarding.
- **Approved:** Admin approves documents and profile.
- **Rejected:** Admin rejects with required correction notes.

**Instructions**
- Show progress indicator (e.g., “Step 4 of 9”).
- Persist the last completed step so returning vendors resume at the next pending step.
- Until approval, vendor logins always land on the onboarding flow with current status.
- Provide admin rejection reason and enable resubmission.

---

## Admin Approval Workflow

**Actions**
- Review business profile and documents.
- Approve or reject with reason.
- Unlock sections for re-edit if needed.

**Notifications**
- Email/SMS notification on approval or rejection.
- In-app notification in vendor panel.

---

## Security & Compliance Requirements

- Use HTTPS for all authentication endpoints.
- Store passwords with strong hashing (bcrypt/argon2).
- Apply rate limiting on OTP and login endpoints.
- Log authentication events for audit.

---

## Outputs

**Successful Completion**
- Vendor account created.
- Profile status set to Pending Review.
- Vendor notified of review status.

**Failure Scenarios**
- Duplicate email/mobile.
- OTP expired or invalid.
- Missing required documents or fields.
- Admin rejection due to invalid compliance documents.
