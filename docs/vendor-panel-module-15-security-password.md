# Module 15: Security & Password

## Purpose
Maintain account security.

## Scope
This module allows vendors to update passwords with verification and strength checks.

## Features
- Change password
- Old password verification
- Password strength validation

---

## Change Password

**Fields**
- Current Password
- New Password
- Confirm New Password

**Instructions**
- Verify current password before allowing changes.
- Enforce password strength rules (min 8 chars, 1 uppercase, 1 number).
- Block reuse of recent passwords if policy requires.

---

## Outputs

**Successful Completion**
- Password updated and session refreshed.

**Failure Scenarios**
- Incorrect current password.
- Weak password does not meet policy.
