# Blu Springfield server

This is a starter configuration for the independent MIT-licensed Springfield server at https://github.com/al1sant0s/springfield.

## Setup

1. Install Docker and Docker Compose.
2. Copy `.env.example` to `.env`. Replace the placeholder secret.
3. Create writable `data`, `static`, and `media` directories.
4. Start the container with `docker compose up -d`.
5. Follow upstream instructions to run `python manage.py migrate` and `python manage.py collectstatic`.
6. Configure nginx for reverse proxy, static files, media and licensed DLC, as documented upstream. nginx is required by the backend.
7. Test the server before connecting a compatible client.

This starter does not include nginx, an Android client or licensed game content. Do not expose it publicly without HTTPS, authentication and backups.
