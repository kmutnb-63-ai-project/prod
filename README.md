# Project Setup Guide

This guide will help you set up and run the project using Docker Compose.

## Prerequisites

- Docker
- Docker Compose

## Project Structure

The project consists of the following main components:

- `AI_Backend`: Backend service
- `make-sense`: Frontend service
- `.gitignore`: Git ignore file
- `.gitmodules`: Git submodules configuration
- `docker-compose.yaml`: Docker Compose configuration file

## Setup Steps

1. Clone the repository:
```
   git clone https://github.com/abc/def.git
   cd def
```
2. If the project uses Git submodules, initialize and update them:
```
   git submodule update --init --recursive
```
3. Build and start the Docker containers:
```
   docker-compose up -d
```
4. To view the logs of the running containers:
```
   docker-compose logs -f
```
5. To stop the containers:
```
   docker-compose down
```
## Additional Configuration

- You may need to configure volume mappings in the `docker-compose.yaml` file to persist data.
- Ensure that any required ports are exposed in the Docker Compose file and not conflicting with other services on your host machine.

## Troubleshooting

- If you encounter any issues, check the Docker logs for each service:

  docker-compose logs [service_name]

- Ensure all required environment variables are set correctly in your `.env` file or `docker-compose.yaml`.

## Maintenance

- To update the project, pull the latest changes and rebuild the Docker images:

  git pull
  docker-compose up -d --build

For more detailed information about each component, refer to their respective documentation if available.
