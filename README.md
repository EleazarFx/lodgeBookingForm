# Lakeshore Lodge Booking

A responsive, browser-based lodge booking form built with HTML, CSS, and vanilla JavaScript. Guests can calculate an estimated stay total, validate their booking details, and manage a temporary list of confirmed bookings.

## Features

- Dynamic greeting based on the time of day
- Browser language display
- Personal, room, stay-date, and account-security fields
- Standard and deluxe room options
- Optional breakfast and boat-trip extras
- Automatic stay-duration and MWK cost calculation
- Name, phone, password, and date validation
- Responsive layout for desktop and mobile screens
- Booking list with individual removal controls
- HTML escaping before booking details are inserted into the page

## Room Rates

| Room | Rate |
| --- | ---: |
| Standard Room | MWK 50,000 per night |
| Deluxe Room | MWK 100,000 per night |

Extras:

- Breakfast: MWK 15,000
- Boat trip: MWK 25,000

The estimated total is calculated as the room nightly rate multiplied by the number of nights, plus all selected extras.

## Requirements

- A modern web browser
- No server, build step, package installation, or external dependency

## Getting Started

1. Open `lakeshoreLodgeBooking.html` in a browser.
2. Enter the guest and account details.
3. Choose a room type and any extras.
4. Select check-in and check-out dates.
5. Review the estimated total and confirm the booking.

You can also serve the folder locally from a terminal:

```powershell
python -m http.server 8000
```

Then visit `http://localhost:8000/lakeshoreLodgeBooking.html`.

## Validation Rules

- Name must contain at least two characters
- Guests must be between 1 and 20
- Phone number must contain at least seven digits
- Password must contain at least eight characters
- Confirmed password must match
- Check-out must be later than check-in
- Check-in and check-out cannot be before the current date
- A room type must be selected

## Data and Security Notes

Bookings remain only in browser memory and are cleared when the page is refreshed or closed. This project does not submit data to a server, use a database, process payments, or create a real reservation.

Passwords are used only for client-side validation; they are not stored or sent to a backend. The form should not be used to collect real passwords or sensitive personal information without adding secure server-side handling and authentication.
