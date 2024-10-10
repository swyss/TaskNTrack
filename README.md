# TaskNTrack

## Overview

**Project Name**: TaskNTrack  
**Purpose**:  
TaskNTrack is a combined solution for managing tasks and objects. It features a ToDo module for tracking and managing tasks and an Inventory module for recording and cataloging objects.

## Key Features

- **ToDo Module**:  
  Create, edit, and track tasks. Assign tasks to users, set priorities, and define due dates.

- **Inventory Module**:  
  Record objects with detailed descriptions, categories, and inventory numbers. Track location and condition of objects. Includes image integration, rating functionality, and import/export features.

- **Offline Capability**:  
  The application is designed to function completely offline, ensuring that all features are available without an internet connection.

- **Platform Compatibility**:  
  The application supports Windows (Electron) and Android, with a server hosted locally on a Raspberry Pi.

## Getting Started

### Prerequisites

- **Backend**: Requires Java (Spring Boot) or .NET (ASP.NET Core) and Docker for deployment.
- **Frontend**: Uses Vue.js with Vuetify for UI components, Electron for desktop clients, and a wrapper solution for Android.
- **Databases**: MongoDB and PostgreSQL for data storage.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repository/TaskNTrack.git
   ```
2. Follow the instructions in `docs/setup.md` for detailed setup and configuration.

### Running the Application

- **Backend**: Refer to `docs/backend_setup.md` for instructions on setting up the backend server on a Raspberry Pi using Docker.
- **Frontend**: Refer to `docs/frontend_setup.md` for instructions on setting up the Electron and Android clients.

## Documentation

### Requirements Specification

For a detailed description of the project's objectives, features, and system architecture, see the [Requirements Specification](docs/requirements.md).

### Developer Documentation

- **API Specifications**: See `docs/api.md` for details on available API endpoints and data models.
- **Module Descriptions**: Each module (ToDo, Inventory, User Management) is documented in `docs/`.
- **User Guide**: See `docs/user_guide.md` for step-by-step instructions on using the application.

## Contributing

We welcome contributions to improve TaskNTrack! Please see `CONTRIBUTING.md` for guidelines on how to contribute.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Support

For any issues or questions, please open an issue in the GitHub repository or contact us via email at support@example.com.

## Acknowledgments

Special thanks to all contributors who have helped make TaskNTrack possible.
