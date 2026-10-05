# Web Development Project

A collaborative travel agency website for browsing tours and booking visits to destinations.

This repository contains the project foundation only. Each page is intentionally minimal so team members can build features independently.

## Project structure and file guide

The files below are intentionally minimal placeholders. The descriptions explain
where each part will appear in the user interface and what its future
responsibility is.

```text
.
├── index.html
├── login.html
├── register.html
├── profile.html
├── bookings.html
├── admin.html
├── pages/
│   ├── about.html
│   ├── services.html
│   ├── details.html
│   ├── booking-form.html
│   └── confirmation.html
├── css/
│   ├── style.css
│   ├── responsive.css
│   └── admin.css
├── js/
│   ├── main.js
│   ├── auth.js
│   ├── validation.js
│   ├── items.js
│   ├── booking.js
│   ├── profile.js
│   └── admin.js
├── data/
│   └── seed.json
├── images/
│   └── items/
└── docs/
    ├── API.md
    ├── DESIGN-GUIDE.md
    ├── REQUIREMENTS.md
    └── ROADMAP.md
```

### Main HTML pages

| File | UI location | Purpose |
|---|---|---|
| `index.html` | Main landing page at `/` | The first page visitors see. It will introduce the travel agency, highlight popular tours, and link to the main user journeys. |
| `login.html` | Authentication area | A form page where returning users sign in to access their profile and bookings. |
| `register.html` | Authentication area | A form page where new users create an account before booking tours. |
| `profile.html` | User account area | The signed-in user’s personal account page. It will show account details and links to account actions. |
| `bookings.html` | User account area | The signed-in user’s booking history and current booking statuses. |
| `admin.html` | Admin dashboard | A private management page for managing tours, users, and bookings. |

### Tour and booking pages

| File | UI location | Purpose |
|---|---|---|
| `pages/about.html` | Public navigation | Explains the agency, its travel services, and its mission. |
| `pages/services.html` | Public tours section | Displays available tours and destinations as cards or a searchable list. |
| `pages/details.html` | Opened from a tour card | Shows one tour’s full description, destination information, price, itinerary, and a link to book it. |
| `pages/booking-form.html` | Opened from a tour details page | Collects the visitor’s tour date, number of travelers, contact details, and booking notes. |
| `pages/confirmation.html` | Immediately after booking submission | Confirms that a booking was created and provides the booking summary or next steps. |

### CSS files

| File | UI location | Purpose |
|---|---|---|
| `css/style.css` | Shared by all pages | Contains the global reset, colors, typography, layout, navigation, buttons, cards, forms, and other shared visual rules. |
| `css/responsive.css` | Shared by all pages | Adjusts the shared layout for mobile, tablet, and desktop screen sizes. |
| `css/admin.css` | `admin.html` | Contains styles specific to the admin dashboard, such as tables, controls, status labels, and admin panels. |

### JavaScript files

| File | UI location | Purpose |
|---|---|---|
| `js/main.js` | Shared by public pages | Handles shared navigation, footer content, common page behavior, and links between sections. |
| `js/auth.js` | `login.html` and `register.html` | Handles registration, login, logout, and the current user session. |
| `js/validation.js` | Shared form pages | Provides reusable validation for required fields, email, passwords, phone numbers, dates, and traveler quantities. |
| `js/items.js` | `pages/services.html` and `pages/details.html` | Loads and renders tour cards, search results, filters, and the selected tour’s details. |
| `js/booking.js` | `pages/booking-form.html`, `pages/confirmation.html`, and `bookings.html` | Creates bookings, validates booking data, displays confirmation details, and supports booking status display. |
| `js/profile.js` | `profile.html` | Loads and updates the signed-in user’s profile information. |
| `js/admin.js` | `admin.html` | Provides admin-only tour CRUD operations and management of users and bookings. |

### Data and media

| File or folder | UI location | Purpose |
|---|---|---|
| `data/seed.json` | Used by the tour listing and admin pages | Contains initial sample tour records for local development. It is the starting data set, not a server database. |
| `images/items/` | Tour cards and tour details pages | Stores images for destinations and tours. Use clear filenames and provide descriptive `alt` text when displaying them. |

### Documentation

| File | Audience | Purpose |
|---|---|---|
| `docs/API.md` | Developers | Defines the planned LocalStorage keys and shared data shapes so features use compatible records. |
| `docs/DESIGN-GUIDE.md` | Whole team | Defines the shared visual direction, colors, typography, spacing, components, responsive behavior, and accessibility basics. |
| `docs/REQUIREMENTS.md` | Whole team | Maps assignment requirements to pages and scripts and identifies the expected owner for each feature. |
| `docs/ROADMAP.md` | Whole team | Lists the implementation phases and the order in which the project should be completed. |

### Expected visitor flow

```text
Home → Tours → Tour Details → Booking Form → Confirmation
                       ↘ Login/Register → Profile → Bookings
```

## Getting started

1. Clone the repository.
2. Open the project in VS Code.
3. Run it with a local server such as Live Server.
4. Create a feature branch before making changes.

See [CONTRIBUTING.md](CONTRIBUTING.md) for the team workflow.

## Planned technology

- HTML5
- CSS3
- Vanilla JavaScript
- LocalStorage for the demo data layer
- GitHub Pages for deployment
