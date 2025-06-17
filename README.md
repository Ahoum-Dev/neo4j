# Neo4j Deployment

This repository contains the configuration to deploy Neo4j using Docker (for Coolify or other hosting platforms).

## Files

- `docker-compose.yml`: Defines the Neo4j service with recommended environment variables and volumes.
- `env.example`: Example environment variables file.

## Getting Started

1. Copy `env.example` to `.env` and customize:
   ```bash
   cp env.example .env
   ```
2. Deploy with Docker Compose:
   ```bash
   docker-compose up -d
   ```
3. Access the Neo4j Browser:
   - Web UI: http://localhost:7474
   - Bolt URL: bolt://localhost:7687
   - Use credentials from `NEO4J_AUTH` in your `.env` file.

## Environment Variables

- `NEO4J_AUTH`: Authentication in the form `username/password`.
- `NEO4J_HEAP_MAX`: (optional) Maximum heap size (e.g., `1G`, `2G`).
- `NEO4J_HEAP_INITIAL`: (optional) Initial heap size (e.g., `512M`, `1G`).

## Using Coolify

1. Create a new app in Coolify and select "Docker Compose".
2. Connect your repository or upload these files.
3. Set the environment variables in Coolify:
   - `NEO4J_AUTH`
   - `NEO4J_HEAP_MAX`
   - `NEO4J_HEAP_INITIAL`
4. Deploy the app.

## License

This repository is released under the MIT License. 