# Mapty

<p align="center">
	Track running and cycling workouts directly on an interactive map.
</p>

<p align="center">
	<a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript"><img src="https://img.shields.io/badge/built%20with-Vanilla%20JS-F7DF1E?logo=javascript&logoColor=black" alt="Built with Vanilla JavaScript" /></a>
	<a href="https://leafletjs.com/"><img src="https://img.shields.io/badge/maps-Leaflet-199900?logo=leaflet&logoColor=white" alt="Leaflet map" /></a>
	<a href="https://developer.mozilla.org/en-US/docs/Web/API/Geolocation_API"><img src="https://img.shields.io/badge/location-Geolocation%20API-1e88e5" alt="Geolocation API" /></a>
</p>

Mapty is a browser app for logging workouts on a map using your current location. Click anywhere on the map, enter workout details, and save activities as Running or Cycling entries with map markers and summary cards.

---

## Features

- Detects your current position with the Geolocation API and centers the map there
- Renders an interactive map using Leaflet and OpenStreetMap tiles
- Adds workouts by clicking the map and submitting the form
- Supports workout-specific fields:
	- Running: cadence + calculated pace
	- Cycling: elevation gain + calculated speed
- Displays workouts as:
	- Map markers with custom popups
	- Sidebar cards with key stats
- Click-to-focus behavior: selecting a workout card pans/zooms the map to its marker
- Persists workouts in localStorage and restores them on reload
- Dynamic form fields that switch based on workout type

## Tech Stack

- HTML5 for application structure
- CSS3 for layout and UI styling
- Vanilla JavaScript (ES6 classes, private fields, DOM events)
- Leaflet.js for map rendering and marker/popups
- Browser Geolocation API for initial map position
- localStorage for client-side data persistence

## Quick Start

1. Clone or download this repository.
2. Open the project folder.
3. Run with one of these options:

```bash
# Option A: Open index.html directly in a browser

# Option B (recommended): use VS Code Live Server
# Right click index.html and choose "Open with Live Server"
```

App entry point: index.html

## How It Works

1. On load, the app requests your location.
2. After permission is granted, it initializes the map.
3. Clicking on the map opens the workout form.
4. Submitting creates a Running or Cycling object.
5. The app renders both a marker and a sidebar item.
6. Workouts are saved to localStorage for future sessions.

## Project Structure

- [index.html](index.html) - Main layout, workout form, and map container
- [style.css](style.css) - App styling, sidebar UI, workout cards, and Leaflet popup styles
- [script.js](script.js) - Domain models (Workout/Running/Cycling) and App logic
- [logo.png](logo.png) - Sidebar logo asset
- [icon.png](icon.png) - Browser tab icon
- [Mapty-flowchart.png](Mapty-flowchart.png) - Application workflow reference
- [Mapty-architecture-part-1.png](Mapty-architecture-part-1.png) - Architecture notes
- [Mapty-architecture-final.png](Mapty-architecture-final.png) - Final architecture view
- [project_screenshots](project_screenshots) - Project preview images

## Screenshot

![Mapty App Screenshot](project_screenshots/Screenshot%202026-03-21%20132120.png)

## Notes

- This project is fully client-side and has no build step.
- Data is stored per browser in localStorage.
- If you deny location permission, the map cannot initialize.

## Future Improvements

- Edit and delete existing workouts
- Better input validation messages in the UI
- Sort/filter workouts in the sidebar
- Export/import workout history
