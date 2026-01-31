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
- Multi-step business profile completion (7-step onboarding).
- Admin approval workflow.
- Secure login with password/OTP options.
- Password recovery and reset.
- Profile completion status tracking.

---

## Onboarding Flow (7-Step Signup)

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

### Step 3: Business Information
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

### Step 4: Location & Address
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

### Step 5: Legal & Compliance Documents
**Purpose:** Upload required licenses and verification documents.

**Fields**
- Business License (required, PDF/JPG)
- Owner ID Proof (required, PDF/JPG)
- Venue Permit (optional)
- Additional Certificates (optional)

**Instructions**
- File size limit: 5 MB per file.
- Accepted formats: PDF, JPG, PNG.
- Mark document verification status as Pending until admin review.

### Step 6: Bank & Payout Details
**Purpose:** Configure payout destination for earnings.

**Fields**
- Account Holder Name (required)
- Bank Name (required)
- Account Number (required)
- IFSC/SWIFT Code (required)
- Branch Name (optional)
- Payout Currency (required)

**Instructions**
- Account number should be masked on display.
- Payout details are locked after submission unless admin unlocks.

### Step 7: Review & Submit
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

### OTP Login
**Fields**
- Mobile Number
- OTP Code (6-digit)

**Instructions**
- OTP expires in 5 minutes.
- Maximum 3 OTP requests per 15 minutes.

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
- Show progress indicator (e.g., “Step 4 of 7”).
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
