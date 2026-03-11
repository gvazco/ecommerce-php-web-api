# ChatCenter Deployment

This project contains a WEB and API built with PHP, deployed using Docker Compose on Dokploy.

## Services

- **WEB**: Web interface at web-ecommerce.core-hub-plex.cloud
- **API**: REST API at api-ecommerce.core-hub-plex.cloud
- **MySQL**: Database service

## Setup

1. Ensure Docker and Docker Compose are installed.
2. Clone the repository.
3. Run `docker-compose up --build` to start the services.
4. Access the WEB at web-ecommerce.core-hub-plex.cloud and API at api-ecommerce.core-hub-plex.cloud (configure DNS accordingly).

## Environment Variables

Configure database connection in `.env`:

- DB_HOST=dbe
- DB_NAME=ecommerce
- DB_USER=gbvazco
- DB_PASS=EF300595

## Deployment on Dokploy

1. Upload the project to your Git repository.
2. In Dokploy, create a new project and connect to the repo.
3. Use the provided `docker-compose.yml`.
4. In Dokploy UI, configure custom domains:
   - For WEB service: web-ecommerce.core-hub-plex.cloud
   - For API service: api-ecommerce.core-hub-plex.cloud
5. Ensure DNS points to your Dokploy instance.

The database will be created and initialized automatically using the `ecommerce.sql` script.
