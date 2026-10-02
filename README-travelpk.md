# Travel.pk Mobile App (Prototype)

A mobile-first app prototype for [Travel.pk](https://travel.pk), designed to match the existing website's brand, content, and customer journey.

**Live demo:** `<add your live URL here>`

## Overview

Travel.pk helps travellers from Pakistan compare live flights, read fare conditions, and plan destinations, visas, and pilgrimage travel. This prototype brings that journey into a clean, touch-friendly app: search flights, explore destinations, plan stays and Umrah, and reach support. Live fares, booking, and payment continue on travel.pk.

## Brand Alignment

- Primary blue `#2563eb` (the site's theme color) with a deep-blue gradient header
- "Elevated Journeys" tagline, PKR pricing, and the same copy and tone as the website
- Bottom navigation mirrors the site's mobile menu: Home, Flights, Stay, Umrah, Trips
- Light theme with automatic dark mode

## Features

| Screen | What it does |
|---|---|
| **Home** | Hero message, flight search, recent searches, six top destinations, tips for comparing fares, airlines, and a reviews note |
| **Flights** | Round Trip, One Way, and Multi-City search (From, To, dates, travellers) with validation, popular route links, and a "Before you pay" checklist |
| **Stay** | Link to stay search, destination guides, packages, Trip Planner, airport services, and transport planning |
| **Umrah** | Pilgrimage planning, flights from Karachi, Lahore, and Islamabad to Jeddah and Medina, and a reminder to verify visa rules with the official authority |
| **Trips** | Sign in to My Trips, price alerts, loyalty, corporate travel, service status, call/WhatsApp/email support, help and policies |

Also included: light/dark toggle and recent searches saved on the device.

## Design Decisions

- **Search hands off to travel.pk:** the form validates the route and dates, then opens the matching live route page (for example Lahore to Dubai) or the general flight search. Live availability and prices are rechecked on the site before payment.
- **No invented data:** destinations, routes, airlines, support details, and policies come from the public site. No fares are shown because the site does not publish a fixed "from" price.
- **Honest reviews:** the app states that no booking-linked reviews are published yet, matching the site's own review standard, so no sample testimonials appear.
- **Recent searches:** stored locally on the device, which fills the empty "Recent Searches" area on the website.

## Tech

- Single-file HTML, CSS, and vanilla JavaScript (no build step, no dependencies)
- Plus Jakarta Sans via Google Fonts, with a system-font fallback
- Responsive with safe-area support for phones with notches
- `localStorage` for recent searches (wrapped in try/catch)
- Respects reduced-motion preferences

## Run Locally

```bash
git clone https://github.com/<your-username>/travelpk-mobile-app.git
cd travelpk-mobile-app
open index.html        # or double-click the file
```

For a phone-sized preview, open it in a browser with device emulation, or serve it with `npx serve .`.

## Deploy

- **GitHub Pages:** Settings, then Pages, then select the `main` branch and root folder.
- **Netlify / Vercel:** import the repo or drag and drop the folder.

## Known Limitations

- Prototype only: no login, bookings, or live fares in the app (these need access to the Travel.pk booking and account APIs).
- Search opens travel.pk for live results; the app does not display fares itself.
- Content is embedded and does not update automatically when the website changes.

## Roadmap

1. React Native (Expo) version for iOS and Android
2. Login with My Trips, e-tickets, and booking management
3. In-app live flight results and checkout
4. Price alerts and booking updates via push notifications
5. Urdu language support
6. WhatsApp support deep links with booking context

## Credits

Built for Travel.pk, operated by TechAbout Private Limited.
