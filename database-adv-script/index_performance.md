# Index Performance Report

## Indexes Created

- idx_bookings_user_id on bookings(user_id)
- idx_bookings_property_id on bookings(property_id)
- idx_bookings_booking_date on bookings(booking_date)

## Performance Testing

### Before Indexes

- Query used sequential scans.
- Execution time: [paste your before time].

### After Indexes

- Query used index scans.
- Execution time: [paste your after time].

---

*Note: Primary keys are indexed by default.*
