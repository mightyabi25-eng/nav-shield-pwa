# NAV-SHIELD PWA v2

Upload these files to the root of the GitHub Pages repository.

New features:
- In-app Install NAV-SHIELD button when the browser exposes the install prompt.
- Real phone accelerometer/gyroscope telemetry using DeviceMotionEvent.
- Permission handling for browsers that require a user gesture.
- Real phone GPS accuracy/status using Geolocation.
- Existing GNSS-denied simulation remains available.

Important: this is a prototype sensor layer, not a production navigation filter. Real dead-reckoning needs calibration, coordinate-frame handling and sensor fusion.
