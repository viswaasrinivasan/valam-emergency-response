# VALAM - Emergency Response & Resource Management System

VALAM is a web application for reporting emergencies, prioritizing incidents, and dispatching nearby response teams. It connects citizens and emergency coordinators in one place.

## What It Does

- **Citizen & Admin Portals:** Separate views for citizens (`CITIZEN001` / `citizen123`) and coordinators (`ADMIN001` / `admin123`).
- **Public SOS Page:** Anyone can send an SOS without logging in. It supports auto GPS location, live camera capture, and voice-to-text recording.
- **Emergency Call Buttons (`112`, `101`, `108`):** Clicking Emergency, Fire, or Ambulance plays a male voice alert and sends an urgent notification to the Admin dashboard.
- **Priority Scoring:** Incidents are ranked automatically using Severity (35%), People Affected (30%), Time Elapsed (20%), and Category (15%). Admins can also override the priority manually.
- **Response Team Management:** Add and manage response teams with their specialty, contact info, base coordinates, and status (`AVAILABLE`, `BUSY`, `OFFLINE`).
- **Nearest-Team Dispatch:** Uses the Haversine distance formula to find and assign the closest available team for an incident.
- **Incident Status Tracking:** Tracks each incident through `REPORTED` -> `VERIFIED` -> `ASSIGNED` -> `IN PROGRESS` -> `RESOLVED` with a timestamped history.
- **Live Map View:** Uses Leaflet and OpenStreetMap to show incidents, response teams, routes, safe zones, hazard areas, and shelters.
- **Dashboard Stats & CSV Export:** Shows total incidents, critical cases, team availability, category charts, and lets you download a CSV report.
- **Community Tools:** Includes emergency broadcasts, family safety check-in, a shelters list, and an offline report queue.
- **12 Languages:** Translates the page into English, Tamil, Hindi, Telugu, Marathi, Urdu, Kannada, Tulu, Malayalam, Bengali, Odia, and Gujarati.
- **Sound Effects:** Plays a click sound on button taps and a spoken male voice alert for SOS and emergency calls.

## Tech Used

- HTML, CSS, JavaScript
- Leaflet + OpenStreetMap
- Browser `localStorage`
- Browser Geolocation, Camera (`getUserMedia`), Web Speech API, Web Audio API

## How to Run

1. Download the project files.
2. Open `index.html` in any modern web browser, or run:
   ```bash
   npm install
   npm run dev
   ```

## Note

This is a web-based emergency coordination project. Triggering an SOS or call button logs an alert in the VALAM dashboard and plays an audio alert, but does not place a real phone call.
