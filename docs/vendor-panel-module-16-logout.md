# Module 16: Logout

## Purpose
Securely end vendor session.

## Scope
This module handles user sign-out, session invalidation, and redirect to the login page.

## Features
- Logout confirmation
- Token/session invalidation
- Redirect to login page

---

## Logout Flow

**Steps**
1. Vendor clicks Logout.
2. Confirmation prompt appears.
3. On confirmation, invalidate session/token.
4. Redirect to login screen.

---

## Outputs

**Successful Completion**
- Session ended and user redirected to login.

**Failure Scenarios**
- Session invalidation failure.
