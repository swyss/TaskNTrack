
# Deployment Instructions

## Backend Deployment on Raspberry Pi
1. SSH into your Raspberry Pi.
2. Clone the repository and navigate to the backend folder.
3. Run:
   ```bash
   docker-compose up -d
   ```
4. Verify that the containers are running:
   ```bash
   docker ps
   ```

## Electron App Deployment
Instructions for building and running the Electron desktop client on Windows:
1. Run the following commands:
   ```bash
   npm install
   npm run build
   ```

## Android App Deployment
Instructions for generating and installing the APK:
1. Use `vue-native` for building the app.
2. Install the APK file manually on Android devices.

[Back to Overview](overview.md)
