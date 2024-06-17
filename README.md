```markdown
# Network-STP-Simulator

## Project Description

The Network-STP-Simulator is an API developed in Node.js that simulates the Spanning Tree Protocol (STP), a crucial protocol in computer networks to prevent data traffic loops. This API allows users to submit network topologies and receive the minimum spanning tree, ensuring efficiency and stability in complex topologies.

## Prerequisites

Before running the project, make sure you have the following items installed on your machine:

- Node.js and npm

## Database Configuration

The Network-STP-Simulator does not require a database as it operates entirely in-memory to simulate network topologies and STP operations.

## Project Compilation and Execution

To compile and run the project, you can use npm. Simply run the following command in the project's root directory:

```sh
npm install
npm start
```

This will compile the project and start the application, which will be available at [http://localhost:3000](http://localhost:3000).

## API Endpoints

### Network Topology

#### POST /api/simulate

- **Description**: Create a new network topology simulation.
- **Request Body**: JSON object containing nodes and edges.
  ```json
  {
    "nodes": ["A", "B", "C", "D"],
    "edges": [["A", "B"], ["A", "C"], ["B", "D"], ["C", "D"]]
  }
  ```
- **Response**: JSON object containing the minimum spanning tree.
  ```json
  {
    "spanningTree": {
      "A": ["B", "C"],
      "B": ["D"],
      "C": [],
      "D": []
    }
  }
  ```

## Example JSON Response

Example JSON response containing a simulated network topology with minimum spanning tree information:

```json
{
  "spanningTree": {
    "A": ["B", "C"],
    "B": ["D"],
    "C": [],
    "D": []
  }
}
```

In this example, the node `A` is the root bridge, and it has direct connections to nodes `B` and `C`, with node `B` further connecting to node `D`.

## Dockerizing the Application

If you prefer to run the application in a Docker container, a Dockerfile is already configured in the project's root directory. To create a Docker image of the application, run the following command:

```sh
docker build -t network-stp-simulator .
```

Then, you can run the application in a Docker container with the following command:

```sh
docker run -p 3000:3000 network-stp-simulator
```

This will start the application in the container and make it available at [http://localhost:3000](http://localhost:3000).

## Tests

Unit tests are executed using Mocha and Chai.

### Running the Tests

Make sure you have all dependencies installed and configured correctly. Then, run the unit tests with the following command:

```sh
npm test
```

## Pending Tasks

### Todo

- [ ] Setup Development Environment
- [ ] Implement Graph Data Structure
- [ ] Develop STP Algorithm
- [ ] Setup Express Server
- [ ] Create Simulation Endpoint
- [ ] Write Unit Tests
- [ ] Document Project in README.md
- [ ] Dockerize the application with Dockerfile

## Contributing

Contributions are welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on how to contribute to the project.

## Authors

- Vinicius Batista (https://github.com/vinnydev-software) - Principal Developer

## License

This project is licensed under the [MIT License](LICENSE).


