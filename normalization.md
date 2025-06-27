
# Database Normalization for AirBnB Schema

## Initial Observations

- The `Booking` table had customer contact details stored redundantly in each booking record.  
- The `Property` table stored host details along with property info, causing duplication when a host has multiple properties.

## Normalization Steps

1. **First Normal Form (1NF):**  
   Ensured atomicity by splitting multi-valued attributes like amenities into a separate `Amenities` table linked to `Property`.

2. **Second Normal Form (2NF):**  
   Removed partial dependencies by making sure all non-key attributes depend on the entire primary key.  
   For example, in the `Booking` table, moved customer personal details to a separate `User` table.

3. **Third Normal Form (3NF):**  
   Eliminated transitive dependencies by removing attributes that depended on non-key attributes.  
   For instance, host contact info was moved to the `Host` table rather than being repeated in `Property`.

## Final Schema Highlights

- Separate tables for `User`, `Host`, `Property`, `Booking`, `Payment`, and `Review`  
- Foreign key relationships ensure data integrity without redundancy  
- This structure prevents update, insert, and delete anomalies

## Conclusion

The database design now adheres to 3NF, improving data consistency, reducing redundancy, and enhancing maintainability.
