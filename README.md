---- Route Optimizer (OpenStreetMap) ----

A lightweight web-based tool for optimizing multi-stop driving routes using OpenStreetMap.
Enter a list of addresses (with optional names), and the app calculates an efficient route and displays it on an interactive map.

---- Features ----
- Multi-address route optimization
- Smart stop ordering (nearest-neighbor algorithm)
- Interactive map with route visualization
- Numbered stop markers
- Custom names for each stop
- Client-side only (no backend required)
- Local caching for faster repeat use
- Tech Stack
- Leaflet for map rendering
- OpenStreetMap tiles
- Nominatim (OSM) for geocoding
- OSRM (Open Source Routing Machine) for routing
- Vanilla JavaScript

---- Setup ----

Clone or download this repo
Open the file:
index.html
Run locally (recommended):
python3 -m http.server

or

npx serve
Open in browser:
http://localhost:8000

---- How to Use ----
Input Format:
Enter one stop per line in the textbox.

You can use:
- Address only:
123 Main St, Apex, NC 27502
456 Oak Ave, Raleigh, NC 27601
- Name + Address (recommended):
Customer A | 123 Main St, Apex, NC 27502
Warehouse | 456 Oak Ave, Raleigh, NC 27601

- Steps
Paste your list of stops
Click "Optimize Route"
View:
Optimized route line
Numbered stops
Click markers to see names

---- How It Works ----
Addresses are converted to coordinates (geocoding)
A nearest-neighbor algorithm determines stop order
OSRM generates the actual driving route
Leaflet renders everything on the map

---- Limitations ----
Best for 5–20 stops (up to ~50 with caching)
Optimization is based on straight-line distance, not traffic or real driving time
Public APIs may rate-limit heavy usage
Geocoding accuracy depends on address quality

---- Caching ----
The app uses browser localStorage to cache geocoded addresses:
Speeds up repeat usage
Reduces API calls
Stored locally (not on any server)

---- License -----

Free to use and modify.
