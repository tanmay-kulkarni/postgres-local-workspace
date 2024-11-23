# PostgreSQL Local Workspace

A containerized PostgreSQL environment I use for local development and testing.
Modify the `.env` file to customize the database settings.

## Prerequisites

- Docker
- Docker Compose

## Setup

1. Clone the repository
2. Place your `data.dump` file in the root directory (if you have one)
3. Modify `.env` file with your preferred settings
4. Add any SQL scripts to `homework/*.sql` for automatic execution during initialization

## Usage

Start the container:
```bash
docker compose up -d
```

Connect to PostgreSQL:
```bash
psql -h localhost -p 2345 -U tanmay -d postgres
```

Remove the container:
```bash
docker compose down -v
```

## Features

- Automatic database initialization from dump file
- Custom SQL script execution on startup
- Persistent data storage
- Configurable through environment variables
- Port mapping for local access

## Environment Variables

See `.env` file for customizable settings:
- Database credentials
- Port mappings
- Container naming