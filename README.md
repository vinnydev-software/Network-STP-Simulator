# Network-STP-Simulator

Welcome to the Network-STP-Simulator project repository!

## Overview

Network-STP-Simulator is a simulation tool for studying network topologies using the Spanning Tree Protocol (STP). It allows users to create virtual network nodes and edges, calculate minimum spanning trees, and simulate data traffic flow in complex network scenarios.

## Features

- Create and manage network nodes and edges.
- Calculate minimum spanning trees using the STP algorithm.
- Simulate data traffic to evaluate network efficiency and stability.

## Installation and Setup

### Prerequisites

Before running the simulator, ensure you have the following installed:

- Node.js (version 12 or above)
- npm (Node Package Manager)
- Docker (optional, for containerized execution)

### Clone the Repository

```bash
git clone https://github.com/seu-usuario/network-stp-simulator.git
cd network-stp-simulator
```

### Install Dependencies

```bash
npm install
```

### Start the Application

To start the simulator locally, run:

```bash
npm start
```

The simulator will be accessible at `http://localhost:8080`.

### Docker Setup (Optional)

If you prefer Docker for deployment, build and run the Docker image:

```bash
docker build -t network-stp-simulator .
docker run -p 8080:8080 network-stp-simulator
```

### API Documentation

For detailed API documentation, including endpoints and usage examples, refer to [API Documentation](https://github.com/vinnydev-software/Network-STP-Simulator/blob/main/API-documentation.md).

### Contributing

We welcome contributions to improve Network-STP-Simulator! Please read the [Contributing Guide](./CONTRIBUTING.md) for guidelines.

### License

This project is licensed under the MIT License. See the [LICENSE](./LICENSE) file for details.

---

### Notas sobre o Exemplo

- **Visão Geral**: Introduz o projeto, destacando suas funcionalidades principais e objetivos.

- **Instalação e Configuração**: Fornece instruções para configurar o ambiente de desenvolvimento, instalar dependências e iniciar o projeto localmente usando Node.js e npm.

- **Documentação da API**: Um link direto para o documento `API-documentation.md`, detalhando os endpoints da API e seu uso.

- **Contribuições**: Incentiva a colaboração no projeto, com um link para o guia de contribuição (`CONTRIBUTING.md`).

- **Licença**: Informa sobre a licença do projeto, com um link para o arquivo `LICENSE` para detalhes adicionais.

