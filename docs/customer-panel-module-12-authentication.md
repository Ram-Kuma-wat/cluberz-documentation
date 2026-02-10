# Module 12: Authentication (Customer)

## Purpose

Allow users to register and log in securely.

## Login Options

- Email login
- OTP-based login
- Google login

**OTP Flow Behavior**
- After OTP verification, if the user is already registered, complete login.
- If the user is not registered, automatically redirect to the signup form.

## Signup

**Fields**
- Name
- Email
- Phone Number
- Gender

**Notes**
- Validate email and phone number formats before account creation.
- Display terms/privacy links on the signup screen for consent.
