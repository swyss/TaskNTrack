
# System Architecture

## Overview
TaskNTrack uses a server-client architecture, with the backend running on a Raspberry Pi and multiple clients (Windows, Android) accessing the data.

## Components
- **Backend**: 
  - Runs on a Raspberry Pi using Docker.
  - Manages MongoDB and PostgreSQL databases for different types of data storage.
- **Frontend**:
  - Electron client for Windows with admin capabilities.
  - Android client for mobile access.
  - Uses IndexedDB for local caching on the client-side.

## Data Flow
- Clients interact with the backend through RESTful APIs.
- Data is stored centrally on the server and is accessible to all clients for consistency.

[Back to Overview](overview.md)
