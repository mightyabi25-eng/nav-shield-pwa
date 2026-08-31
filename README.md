# NAV-SHIELD PWA

This folder contains the Progressive Web App version of the uploaded NAV-SHIELD prototype.

## Files
- `index.html` — original NAV-SHIELD prototype converted for PWA use
- `manifest.json` — installable-app metadata
- `service-worker.js` — offline app-shell caching
- `icons/` — PWA icons

## Run locally
For PWA installation/service workers, use HTTPS or localhost. Do not simply open `index.html` with `file://`.

Example with Python:
1. Open a terminal in this folder.
2. Run: `python -m http.server 8000`
3. Open: `http://localhost:8000`
4. For phone installation, deploy the folder to an HTTPS host.

## Important
The current prototype is a software simulation. It does not yet read real phone GPS, accelerometer, or gyroscope hardware. The original prototype itself describes this limitation.
