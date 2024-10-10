
# Setup Instructions

## Prerequisites
- Node.js v16+
- Docker and Docker Compose

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/TaskNTrack.git
   cd TaskNTrack
   ```

2. Install dependencies for the frontend:
   ```bash
   npm install
   ```

3. Start Docker containers:
   ```bash
   docker-compose up -d
   ```

4. Start the development server for Electron:
   ```bash
   npm run dev
   ```

## Running on Android
1. Build the APK using:
   ```bash
   npm run build:android
   ```
2. Install the APK on your Android device.

[Back to Overview](overview.md)
