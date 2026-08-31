# NAV-SHIELD V3.2

V3 upgrades the V2 prototype from a simulated test track to a live phone navigation interface.

## What changed
- Live OpenStreetMap map using Leaflet.
- Real browser GPS position, accuracy, speed and heading.
- Real phone accelerometer and gyroscope telemetry.
- Manual **Simulate GPS loss** control for testing.
- Dead-reckoning estimate during simulated/actual GPS loss.
- GPS recovery and position correction.
- Separate GNSS, dead-reckoning and correction trails.
- PWA install support and service-worker caching.

## Deploy
1. Upload the contents of this folder to the root of a GitHub Pages repository.
2. Open the GitHub Pages HTTPS URL on the phone.
3. Allow location permission.
4. Tap **Enable phone sensors** and grant motion/orientation permission.
5. Tap **Start live navigation**.
6. For testing Stage 3–5, tap **Simulate GPS loss**, move with the phone, then tap **Restore GPS**.

## Important engineering limitation
A phone accelerometer cannot provide accurate long-duration latitude/longitude by itself. Integration of acceleration produces drift, and the phone's orientation changes with how it is held or mounted. V3 is therefore a demonstration/prototype of the fusion workflow, not a certified navigation system.

For a vehicle-grade implementation, use a fixed calibrated IMU, wheel-speed/odometry, magnetometer or GNSS heading where appropriate, and an EKF/UKF with proper coordinate-frame and bias estimation.

## Browser requirements
Use HTTPS (GitHub Pages is suitable) or localhost. iOS browsers may require permission requests from a user gesture. GPS and motion data also depend on device hardware and browser support.

## Map data
The interface uses Leaflet and OpenStreetMap tiles. Internet access is needed for map tiles unless a separate offline tile solution is added.
