# System Architecture

## Overview
TaskNTrack uses a server-client architecture, with the backend running on a Raspberry Pi and multiple clients (Windows, Android) accessing the data.

## Components
- **Backend**: 
  - Runs on a Raspberry Pi using Docker.
  - Manages MongoDB and PostgreSQL databases.
- **Frontend**:
  - Electron client for Windows with admin capabilities.
  - Android client for mobile access.