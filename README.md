# stride 🏃‍♂️ 🗺️

**stride** is a web-based GPS art generator that allows runners and cyclists to "type a word, run the route, share on Strava." It converts text into continuous geographic coordinates, snaps them to real-world footpaths, and allows the user to export the resulting route as a GPX file.

## Features

- **Text-to-Route Generation**: Converts a word (up to 10 characters) into a continuous, non-overlapping path using a custom single-stroke font algorithm.
- **Smart Routing (Road Snapping)**: Utilizes the OpenStreetMap Routing Machine (OSRM) to snap the generated path to actual, runnable footpaths and pedestrian roads.
- **Interactive Map**: Built with Leaflet.js, allowing you to drag the starting pin, search for locations globally, and preview the generated route in real-time.
- **Dynamic Scale**: Adjust the target distance of your run, and the text will automatically scale to match the desired distance (from 2km to 30km).
- **Pace & Time Estimation**: Input your average pace to get real-time estimates of how long the run will take. Supports both metric (km) and imperial (mi) units.
- **GPX Export**: Download the finished route as a `.gpx` file, ready to be uploaded to Strava, Garmin Connect, Apple Watch, or any other GPS tracking device.
- **Route Playback**: Watch an animated preview of your route being run directly on the map.

## Tech Stack

STRIDE is a zero-build, single-file web application (`index.html`) ensuring maximum portability and performance.

- **Frontend**: Vanilla HTML, CSS, and JavaScript. Zero bundlers, zero dependencies (except Leaflet via CDN).
- **Mapping**: [Leaflet.js](https://leafletjs.com/) with CARTO Dark Matter tiles.
- **Routing API**: [OSRM (OpenStreetMap Routing Machine)](http://project-osrm.org/) public API (`routing.openstreetmap.de`) for pedestrian route snapping.
- **Geocoding API**: Nominatim API for location search and reverse geocoding.

## How to Use

1. Open `index.html` in any modern web browser.
2. **Type your word**: Enter a word (e.g., "RUN").
3. **Pick a location**: Search for a city, drag the green pin on the map, or use your device's current location.
4. **Set a distance**: Use the slider to scale the total length of the run.
5. **Adjust pace**: Provide your running pace to see how long it will take.
6. **Export**: Click the download button to save the GPX file, send it to your device, and go start your run!

## Development

Everything is contained in a single `index.html` file, no build steps are required.