# AirBnB Clone Database Schema

This directory contains the SQL DDL script used to define the schema for the AirBnB clone project.

## Files

- `schema.sql` – SQL statements that create all necessary tables, constraints, and indexes.

## Tables and Relationships

1. **Users**
   - Stores all user accounts.
   - UUID primary key.
   - Roles: guest, host, admin.
   - Indexed email for quick lookup.

2. **Properties**
   - Listed by hosts (users).
   - Linked to Users via `host_id`.

3. **Bookings**
   - Users book properties.
   - Linked to Users and Properties.
   - Status must be one of: pending, confirmed, or canceled.

4. **Payments**
   - Linked to bookings.
   - Includes payment method: credit_card, paypal, or stripe.

5. **Reviews**
   - Users can rate and comment on properties.
   - Rating must be between 1 and 5.

6. **Messages**
   - Direct messages between users.
   - Includes sender_id and recipient_id.

## Constraints & Indexing

- Primary keys are UUIDs and indexed automatically.
- Foreign keys enforce relational integrity across tables.
- ENUM values enforced via `CHECK` constraints.
- Additional indexes on:
  - Users: email
  - Properties: property_id
  - Bookings: property_id, user_id
  - Payments: booking_id
  - Reviews: property_id

## Notes

- Timestamps are auto-generated with `DEFAULT CURRENT_TIMESTAMP`.
- The schema follows normalization rules up to 3NF.
