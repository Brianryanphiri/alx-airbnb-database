# ER Diagram for AirBnB Database

This ER diagram visualizes the main structure of the AirBnB database system.

![AirBnB ER Diagram](./airbnb_erd.png)

## Entities:
- **User**
- **Property**
- **Booking**
- **Payment**
- **Review**
- **Message**

## Relationships:
- A **User** can have multiple **Bookings**
- A **Host (User)** can list multiple **Properties**
- A **Property** can have multiple **Bookings** and **Reviews**
- A **Booking** has one **Payment**
- **Users** can send and receive **Messages**

