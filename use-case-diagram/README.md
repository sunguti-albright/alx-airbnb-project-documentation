I'll create a detailed use case diagram description for the Airbnb Clone backend. Since I can't create visual diagrams, I'll provide a comprehensive text-based description that you can easily convert into a visual diagram using Draw.io.

# Airbnb Clone Backend - Use Case Diagram Description

[use-case-diagram.png](/use-case-diagram/use-case-diagram.png)
## Actors
1. **Guest** - User looking to book accommodations
2. **Host** - User offering properties for rent
3. **Admin** - System administrator
4. **Payment System** - External payment processing service

## Use Cases

### Authentication Module
- **Register Account**
  - Actors: Guest, Host
  - Description: New users create an account with email/password or OAuth
  - Includes: Verify Email, Set Password

- **Login to System**
  - Actors: Guest, Host, Admin
  - Description: Users authenticate with credentials
  - Includes: Validate Credentials, Create Session

- **Manage Profile**
  - Actors: Guest, Host
  - Description: Users update personal information and preferences
  - Extends: Upload Profile Photo, Update Preferences

- **Reset Password**
  - Actors: Guest, Host
  - Description: Users recover access to accounts
  - Includes: Send Reset Email, Verify Token

### Property Management Module
- **Create Property Listing**
  - Actors: Host
  - Description: Hosts add new properties to the platform
  - Includes: Add Photos, Set Pricing, Define Amenities

- **Edit Property Listing**
  - Actors: Host
  - Description: Hosts modify existing property details
  - Includes: Update Availability, Modify Pricing

- **Delete Property Listing**
  - Actors: Host
  - Description: Hosts remove properties from the platform

- **Search Properties**
  - Actors: Guest
  - Description: Guests find properties based on criteria
  - Includes: Filter Results, Sort Listings

- **View Property Details**
  - Actors: Guest
  - Description: Guests examine specific property information

### Booking Management Module
- **Make Reservation**
  - Actors: Guest
  - Description: Guests book available properties
  - Includes: Check Availability, Calculate Total
  - Extends: Process Payment

- **Manage Bookings**
  - Actors: Guest, Host
  - Description: Users view and modify reservations
  - Includes: View Booking History, Cancel Reservation

- **Confirm Booking**
  - Actors: Host
  - Description: Hosts accept or decline booking requests

### Payment Module
- **Process Payment**
  - Actors: Guest, Payment System
  - Description: Handle financial transactions for bookings
  - Includes: Validate Payment Method, Process Transaction

- **Issue Refund**
  - Actors: Host, Admin
  - Description: Process refunds for cancelled bookings
  - Includes: Calculate Refund Amount, Process Refund

- **Manage Payouts**
  - Actors: Host, Payment System
  - Description: Transfer funds to host accounts
  - Includes: Calculate Earnings, Initiate Transfer

### Review System Module
- **Write Review**
  - Actors: Guest
  - Description: Guests rate and review properties after stay
  - Includes: Submit Rating, Write Comments

- **Respond to Review**
  - Actors: Host
  - Description: Hosts reply to guest reviews

- **Report Review**
  - Actors: Guest, Host
  - Description: Users flag inappropriate reviews
  - Extends: Moderate Content (Admin)

### Admin Management Module
- **Manage Users**
  - Actors: Admin
  - Description: Administrators manage user accounts
  - Includes: Suspend Users, Verify Identities

- **Moderate Content**
  - Actors: Admin
  - Description: Review and manage platform content
  - Includes: Review Listings, Moderate Reviews

- **View Analytics**
  - Actors: Admin
  - Description: Access system performance data
  - Includes: Generate Reports, Monitor Metrics

## Relationships
- **Guest** can: Register, Login, Search Properties, View Details, Make Reservations, Manage Bookings, Write Reviews, Report Content
- **Host** can: Register, Login, Manage Properties, Confirm Bookings, Manage Payouts, Respond to Reviews, Report Content
- **Admin** can: Manage Users, Moderate Content, View Analytics, Issue Refunds
- **Payment System** participates in: Process Payment, Manage Payouts
