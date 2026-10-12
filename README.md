# Marine Nav — Free OpenStreetMap iPhone GPS & Boat Navigation (PWA)

This version uses **OpenStreetMap as the default map** and does not require a Google Maps API key or Google Cloud billing. It keeps the purple HDG compass, iPhone GPS, SOG/COG, manual map-tap/coordinate waypoints, saved waypoints, track recording/export, and Man Overboard marker.

## Features
- OpenStreetMap default map using Leaflet; no Google API key.
- iPhone GPS via browser geolocation; compass via device orientation where supported.
- Purple HDG display/heading line, SOG/COG estimates, GPS accuracy.
- Tap the map or enter coordinates to set an active waypoint; bearing/distance update from GPS.
- Save named waypoints locally and export as GeoJSON.
- Record GPS track locally and export track JSON; clear recorded track.
- Optional OpenSeaMap seamark overlay (coverage varies).
- Optional GEBCO WMS bathymetry overlay where the service/coverage permits; indicative only.
- MOB marker and distance-to-MOB display.
- PWA manifest/service worker for Add to Home Screen.

## Publish to GitHub Pages
1. Download and unzip this package.
2. Upload the files inside `Marine_Nav_Google_Satellite_iPhone` to the root of your existing `marine-compass` repository, replacing the old files. No `config.js` or Google API key is needed.
3. Keep GitHub Pages enabled for your current deployment branch.
4. Open `https://eusuph2011-bit.github.io/marine-compass/` after deployment finishes.
5. On iPhone, open the site in Safari, tap **Share → Add to Home Screen**, then launch it.
6. Tap **ENABLE COMPASS + GPS** and allow location/motion permissions. Go outdoors for a better GPS fix.

## Map layer notes
- **OSM MAP** is the in-app base map. **OPEN OSM** opens the current area on OpenStreetMap.org.
- The standard OpenStreetMap tile service is community-funded and best-effort. Keep normal interactive use only, preserve visible attribution, and do not bulk-download tiles or add offline-prefetch functionality. See the official [Tile Usage Policy](https://operations.osmfoundation.org/policies/tiles/).
- OpenSeaMap coverage varies. GEBCO bathymetry is coarse/indicative and can be missing or unsuitable for local navigation. Neither is a certified nautical chart or depth sounder.

## Safety and limitations
- This is a web app/PWA, not a native App Store app. Browser backgrounding may pause location updates and track recording.
- A phone compass can be affected by magnets, metal, and calibration. COG is direction of travel, not the same as heading.
- No official ENC chart, tide/current, route safety, or depth-sounder integration is included. Do not use this app as the sole means of navigation; carry current official charts and required safety equipment.
- Saved waypoints and tracks live in browser storage on this device; export them regularly.
- Leaflet is loaded from the unpkg CDN, so the first map load requires internet access.
