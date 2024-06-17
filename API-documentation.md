### **API Documentation for Network-STP-Simulator**

Welcome to the API documentation for Network-STP-Simulator. This API allows you to simulate and study network topologies using the Spanning Tree Protocol (STP).

#### **Base URL**

All endpoints are relative to the base URL:

```
http://localhost:8080/api
```

#### **Authentication**

Currently, the API does not require authentication. All endpoints are publicly accessible.

#### **Endpoints**

##### **Network Nodes**

- **Create a Network Node**

  `POST /nodes`

  Creates a new network node in the system.

  **Request Body:**

  ```json
  {
    "name": "Node A",
    "type": "Router"
  }
  ```

  **Response:**

  ```json
  {
    "id": 1,
    "name": "Node A",
    "type": "Router",
    "createdAt": "2024-06-17T10:00:00Z"
  }
  ```

- **List All Network Nodes**

  `GET /nodes`

  Retrieves a list of all network nodes.

  **Response:**

  ```json
  [
    {
      "id": 1,
      "name": "Node A",
      "type": "Router",
      "createdAt": "2024-06-17T10:00:00Z"
    },
    {
      "id": 2,
      "name": "Node B",
      "type": "Switch",
      "createdAt": "2024-06-17T10:05:00Z"
    }
  ]
  ```

- **Get Network Node by ID**

  `GET /nodes/{id}`

  Retrieves details of a specific network node based on the ID.

  **Response:**

  ```json
  {
    "id": 1,
    "name": "Node A",
    "type": "Router",
    "createdAt": "2024-06-17T10:00:00Z"
  }
  ```

- **Update Network Node**

  `PUT /nodes/{id}`

  Updates data of an existing network node based on the ID.

  **Request Body:**

  ```json
  {
    "name": "Updated Node A"
  }
  ```

  **Response:**

  ```json
  {
    "id": 1,
    "name": "Updated Node A",
    "type": "Router",
    "createdAt": "2024-06-17T10:00:00Z",
    "updatedAt": "2024-06-17T10:10:00Z"
  }
  ```

- **Delete Network Node**

  `DELETE /nodes/{id}`

  Deletes a network node from the system based on the ID.

  **Response:**

  `204 No Content`

##### **STP Simulation**

- **Calculate Minimum Spanning Tree**

  `POST /stp/calculate`

  Initiates the calculation of the minimum spanning tree using the Spanning Tree Protocol.

  **Request Body:**

  ```json
  {
    "nodes": [1, 2, 3],
    "edges": [
      {"source": 1, "target": 2, "weight": 5},
      {"source": 2, "target": 3, "weight": 3},
      {"source": 1, "target": 3, "weight": 9}
    ]
  }
  ```

  **Response:**

  ```json
  {
    "edges": [
      {"source": 1, "target": 2},
      {"source": 2, "target": 3}
    ]
  }
  ```

  This API calculates and returns the edges of the minimum spanning tree for the given nodes and edges.


