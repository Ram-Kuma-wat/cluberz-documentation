# Module 12: Earnings & Transactions

## Purpose
Track business earnings and withdrawals.

## Scope
This module provides earnings breakdowns for events and restaurant reservations, plus transaction history. Withdrawals are automatic based on booking completion timelines.

## Earnings Types
1. Event Earnings
2. Table Reservation Earnings (restaurant-only)

---

## Event Earnings

**Fields**
1. Booking ID
2. Event Name
3. Amount
4. Date of Booking
5. Comment

---

## Table Reservation Earnings

**Availability:** Only for businesses with the restaurant option.

**Fields**
1. Reservation ID
2. Booking Date
3. Amount
4. Comment

---

## Transaction History

**Fields**
1. Total Earnings (event + restaurant)
2. Withdraw Amount
3. Balance Amount
4. Table of Transaction History
   - Txn ID (auto-generated on transfer)
   - Amount
   - Status (Credit/Withdrawn)
   - Comment
   - Created Date

---

## Transfer Timeline (Auto Payouts)

**Rules**
- Event earnings are transferred within 12-24 hours after the event finishes.
- Table reservation earnings are transferred within 12 hours after the booking time ends.
- Transfers are held if there is an active dispute.

---

## Features
- Transaction history
- Balance tracking
- Auto-generated transaction IDs

---

## Outputs

**Successful Completion**
- Earnings and transfer records visible with timestamps.

**Failure Scenarios**
- Transfer held due to dispute.
- Missing booking references.
