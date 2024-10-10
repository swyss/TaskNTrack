# API Documentation

## Base URL
`http://<your-local-server>:<port>/api`

### Endpoints

#### `GET /api/tasks`
Returns a list of all tasks.

#### `POST /api/tasks`
Creates a new task.
- **Body**: 
  ```json
  {
    "title": "Task title",
    "description": "Detailed description",
    "priority": "high"
  }
  ```

#### `GET /api/inventory`
Returns a list of all inventory items.

#### `POST /api/inventory`
Creates a new inventory item.
- **Body**: 
  ```json
  {
    "name": "Item name",
    "description": "Detailed description",
    "image": "base64encodedImage",
    "rating": {
      "criteria1": 4,
      "criteria2": 5
    }
  }
  ```
```