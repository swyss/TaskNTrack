# TaskNTrack - Requirements Specification

## 1. Objectives and Introduction
### Project Description
**Project Name**: TaskNTrack  
**Purpose of the Application**:  
"TaskNTrack aims to facilitate efficient management of tasks and objects through a ToDo module for tracking and managing tasks, and an Inventory module for recording and cataloging objects."

### Target Audience
**Primary User Groups**:  
Individuals seeking a combined solution for task management and object tracking.

### Scope
**Functionalities**:
- **ToDo Module**: Create, edit, and track tasks, assign tasks to users, set priorities, and due dates.
- **Inventory Module**: Record objects with detailed descriptions, categories, and inventory numbers, track the location and condition of objects, and provide export and import functionalities for easy data backup.

## 2. Functional Requirements
### 2.2 Inventory Module
- **Object Management**: Users can add new objects, edit existing ones, and provide information such as name, description, category, and inventory number.
- **Image Integration**: Users can upload an image for each object for visual identification, supporting common image formats (e.g., JPEG, PNG).
- **Location and Condition Tracking**: Users can record the location (e.g., "Living Room", "Basement") and condition (e.g., "new", "used", "damaged") of objects.
- **Categories and Tags**: Objects can be assigned to different categories (e.g., "Electronics", "Furniture"). Tags allow flexible assignment and filtering.
- **Rating Functionality**: Users can rate objects based on criteria like condition, quality, and usefulness. Ratings are aggregated into an overall rating that gives an overview of the object's value or condition.
- **Search and Filter Features**: Users can search for objects by name, category, location, condition, or overall rating.
- **Export and Import**: Data can be exported in formats like CSV for easy backup, and existing data can be supplemented through import functionalities.

## 3. Non-Functional Requirements
### 3.1 Performance
- **Response Times**: The application should respond to user actions within a maximum of 200 milliseconds (e.g., when creating or editing a task).
- **Load Times**: The initial loading time should not exceed 2 seconds.
- **Data Processing**: The export and import of data (e.g., inventory lists) should be completed within 5 seconds for up to 1,000 entries.

### 3.2 Security
- **Data Privacy**: The application must comply with data protection regulations (e.g., GDPR), storing only necessary data locally.
- **Encryption**: Sensitive information like user data should be stored encrypted.
- **Authentication and Authorization**: Access to user data is controlled by a secure login system with password hashing (e.g., Bcrypt).

### 3.3 Availability
- **Uptime**: The application should maintain 99.5% uptime, ensuring constant availability for users.
- **Offline Capability**: The application must be fully functional offline, allowing users to add tasks or objects without an internet connection. No cloud integration is required.

### 3.4 Scalability
- **User Scalability**: The application should support up to 1,000 concurrent active users on a shared device (e.g., multi-user scenarios on a desktop).
- **Data Volume**: Support for large datasets in the Inventory module, such as up to 10,000 recorded objects.

### 3.5 Maintainability
- **Code Quality**: The source code should adhere to Clean Code and SOLID principles to facilitate future maintenance.
- **Modularity**: The code should be organized into clearly separated modules for different functions (e.g., ToDo, Inventory, User Management).
- **Documentation**: Detailed developer documentation in the form of `.md` files will be provided. Each module should be thoroughly described.

### 3.6 Usability
- **Intuitive User Interface**: The application should offer a user-friendly interface that can be used without additional guidance.
- **Customization**: Users can customize the dashboard and widgets according to their preferences.
- **Multilingual Support**: Support for multiple languages, including English and German.

## 4. System Architecture and Technology Stack
### 4.1 Architecture Diagram
**Server-Client Architecture**:
- **Backend Server**: Runs on a small server in the local network and provides data to all clients.
- **Frontend Clients**:
  - **Electron App**: Acts as the main client and handles administrative tasks like data management.
  - **Android App**: Optimized version for mobile devices to display and edit tasks and inventory data.
  - **Windows Client**: Electron version for desktop environments to access all data and functionalities.
- **Network Communication**: Clients communicate with the backend server via a RESTful API to access centralized data.

### 4.2 Technologies
- **Frontend**:
  - **Framework**: Vue.js (with Vuetify for UI components).
  - **Electron**: Main client for Windows desktops with administrative functions.
  - **Android**: Using Vue Native or an Android wrapper solution for the mobile app.
  - **IndexedDB**: For local data storage and caching on end devices for better performance and offline access.
- **Backend**:
  - **Programming Language**: Java (Spring Boot) or .NET (ASP.NET Core).
  - **Storage Technologies**:
    - **NoSQL Database**: MongoDB for flexible, schema-less storage of inventory and task data.
    - **SQL Database**: PostgreSQL for relational data and complex queries.
  - **API**: RESTful API for communication between the backend and frontend, supporting all data queries and manipulations.
  - **Deployment**: The backend server is hosted on a local network server, requiring no internet connection.

### 4.3 Integrations and Interfaces
- **File Upload**: Support for uploading images (e.g., JPEG/PNG) for inventory objects, stored centrally on the server.
- **Export and Import**: CSV support for exporting and importing inventory and task data, managed through the Electron app.
- **Platform Compatibility**:
  - **Frontend**: Support for Windows and Android.
  - **Backend**: Can run on a Linux-based server for a stable and cost-effective solution.

## 5. User Interface (UI/UX) Requirements
### 5.1 Design Requirements
- **Clear and Minimalist Design**: The UI should be simple and intuitive, allowing users to navigate quickly.
- **Responsive Design**: The UI should adapt to different screen sizes and devices (desktop, tablet, smartphone).
- **Color Scheme**: A modern, friendly color scheme with accent colors for important elements (e.g., "Add" button, warnings).
- **Dark Mode Support**: Option to switch between a light and dark mode.

### 5.2 Navigation
- **Main Navigation**: Access to core modules (ToDo, Inventory, Dashboard) through a sidebar in the desktop version and a menu in the mobile version.
- **Breadcrumbs**: Display the current position within the application for better orientation.
- **Quick Access**: An "Add" button accessible from any page to quickly create tasks or inventory objects.
- **Dashboard**: Provides an overview of upcoming tasks and recently added inventory objects.

### 5.3 Views and Layouts
- **Dashboard**:
  - Overview of all open tasks and inventory.
  - Display filters (e.g., tasks by priority, inventory by category).
  - Customizable widgets to display important information at a glance.
- **ToDo Module**:
  - List view for tasks sorted by priority, due date, and status.
  - Detail view for editing tasks with options to adjust due dates and priorities.
- **Inventory Module**:
  - Grid and list views for inventory objects with filtering by category, location, and condition.
  - Detail view for each object, including image, description, location, condition, and ratings.
  - Ratings summary showing individual criteria and overall rating.

### 5.4 Interaction Design
- **Drag-and-Drop**: Support for drag-and-drop, e.g., for reordering tasks within lists.
- **Context Menus**: Right-click context menus for quick actions (e.g., edit, delete) for tasks and inventory objects.
- **Confirmation Messages**: Safety prompts before deleting important data, e.g., "Are you sure you want to delete this task?"

### 5.5 Accessibility
- **Keyboard Navigation**: The application should be fully navigable using a keyboard.
- **Screen Reader Support**: All key functions and content should be optimized for screen readers.
- **Contrast Adjustments**: Ability to adjust the interface contrast for better readability for users with visual impairments.

## 6. Quality Requirements and Testing
### 6.1 Testing Strategy
- **Unit Tests**:
  - Core functionalities like creating and editing tasks or adding inventory objects will be covered by unit tests.
  - Focus on the logic of the ToDo and Inventory modules.
- **Integration Tests**:
  - Ensure the proper interaction between frontend and backend, especially in API communication.
  - Verify database access (PostgreSQL, MongoDB) functions correctly.
- **End-to-End Tests**:
  - Scenarios that simulate typical user actions, e.g., "Add a new task and mark it as complete" or "Add a new inventory object and rate it."
  - Automated tests for operating the application on various platforms (Windows, Android).

### 6.2 Acceptance Criteria
- **Functional Completeness**: All features described in the functional requirements are implemented and tested.
- **Performance Requirements**: The application meets the response times and load times outlined in the non-functional

 requirements.
- **Offline Functionality**: Ensured that all data is accessible without an internet connection.

### 6.3 Testing Scenarios
- **ToDo Module**:
  - Scenario 1: "Create, edit, mark as complete, and delete a task."
  - Scenario 2: "Create a high-priority task and change the priority to low."
- **Inventory Module**:
  - Scenario 1: "Record a new inventory object, upload an image, and rate the object."
  - Scenario 2: "Change an object's status and verify the change in the overview."
- **User Management**:
  - Scenario 1: "Register a new user and log in."
  - Scenario 2: "Trigger a failed password entry and receive an error message."

### 6.4 Risk Analysis
- **Potential Risks**:
  - **Data Loss**: Risk of unsecured local databases. Solution: Regular local backups.
  - **Platform Differences**: Variations in appearance between desktop and mobile versions. Solution: Testing on multiple devices and platforms.
  - **Offline Synchronization**: Potential synchronization issues when data is edited offline. Solution: Define and test conflict resolution strategies.

### 6.5 Testing Environment
- **Automated Tests**: Use tools like Selenium for end-to-end tests and JUnit or PyTest for unit tests.
- **Manual Tests**: Verify the user interface through test users on different devices and platforms.
- **Test Database**: Set up a test instance for PostgreSQL and MongoDB to conduct integration and end-to-end tests.

## 7. Deployment and Operation
### 7.1 Deployment Environment
- **Backend Server**:
  - Hosted on a Raspberry Pi in the local network, providing the NoSQL database (MongoDB), PostgreSQL instance, and RESTful API for data exchange with clients.
  - **Containerization with Docker**: The server and its components (databases, API) are run in Docker containers for easy installation and maintenance.
  - **Docker Compose**: Use Docker Compose for orchestrating the services, ensuring that all required components start and run together.
- **Frontend Clients**:
  - **Electron App**: Installed on Windows desktops as the main client, providing direct access to administrative functions.
  - **Android App**: Provided via an APK file for manual installation on Android devices.
  - **Windows Client**: Through the Electron app, which receives the latest version directly from the server, enabling easy updates.

### 7.2 Update and Backup Strategy
- **Updates**:
  - **Backend**: Updates are provided as new Docker images and can be restarted on the Raspberry Pi using Docker Compose.
  - **Frontend**: The Electron app can notify users when a new version is available.
- **Backups**:
  - **Automated Backups**: Regular backup of Docker volumes (databases) to an external drive or NAS in the local network.
  - **Manual Exports**: Users can manually export data (e.g., inventory lists) through the Electron app for local backup.

### 7.3 Monitoring and Error Tracking
- **Logs**:
  - The Raspberry Pi server logs access, API calls, and errors to log files for quick issue identification.
  - Docker logs monitor the status of containers and the services running within them.
- **Performance Monitoring**:
  - Monitor server resources (CPU, memory) on the Raspberry Pi and API response times.
  - Regularly review database performance and integrity within the Docker environment.

### 7.4 Recovery Strategy
- **Data Recovery**:
  - In case of data loss, Docker volumes can be manually restored from backups.
  - The server supports rollback by applying older Docker images or database snapshots.
- **Fault Tolerance**:
  - The Raspberry Pi automatically restarts Docker containers if a critical error occurs.
  - The application is configured to continue running during temporary network outages until the connection is restored.

### 7.5 Operational Documentation
- **Installation Guide**: Step-by-step instructions for installing the Docker environment and configuring the Raspberry Pi server.
- **Update Guide**: Documentation on how to apply backend updates through new Docker images.
- **Maintenance Log**: Record of maintenance and update operations for an auditable history.

## 8. Documentation and Support
### 8.1 Developer Documentation
- **Code Documentation**:  
  - All major classes, methods, and functions are thoroughly documented in code (in English).
  - Use `.md` files in the Git repository to document modules (e.g., ToDo module, Inventory module, User management).
- **Documentation Structure in Git Repository**:
  - **readme.md**: Overview of the project and instructions for starting.
  - **docs/**: Contains detailed documentation for each component and guides (e.g., `api.md` for API specifications, `setup.md` for installation instructions, `user_guide.md` for user manuals).

### 8.2 User Guides
- **End-User Manual**:
  - Step-by-step guides for using key features of the Electron and Android apps, such as creating tasks and managing inventory.
  - Includes screenshots and example scenarios for better understanding.
  - All manuals are available as `.md` files in the `docs/` directory of the Git repository.
- **FAQ Section**:
  - Frequently asked questions and solutions for common problems (e.g., "How do I import an inventory list?").
  - Available as an `.md` file in the `docs/` directory.
- **Tooltips and Help Texts**:  
  - Tooltips and help texts are integrated into the user interface for quick guidance.

### 8.3 Support and Maintenance
- **Support Channels**:
  - Email support for technical questions and issues.
  - A GitHub repository where users can report issues, which are tracked and resolved by the developers.
- **Maintenance**:
  - Regular checks for security updates for backend and frontend components.
  - Planning and documentation of maintenance intervals for the Raspberry Pi server (e.g., checking Docker containers, database backups).
  - Maintenance logs and release documentation are also stored as `.md` files in the `docs/` directory.
- **Release Management**:
  - Version numbering and changelogs for each released version of the application.
  - **changelog.md**: Provides details about new features, bug fixes, and known issues, located in the `docs/` directory.