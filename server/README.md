# Blu Springfield local server

This setup runs the MIT-licensed [Springfield server](https://github.com/al1sant0s/springfield) behind nginx on your Mac. It uses Docker containers.

## First run

1. Install and start Docker Desktop.
2. Open Terminal in the `server` directory of this repository.
3. Run `cp .env.example .env`.
4. Open `.env`. Replace `REPLACE_WITH_LONG_RANDOM_SECRET` with your own long random secret. Do not upload the actual `.env`.
5. Run `mkdir -p data media static dlc`. Make these folders writable by UID 1000, as required by the upstream Docker image.
6. Run `docker compose up -d`.
7. Run `docker compose exec springfield-server python manage.py migrate`.
8. Run `docker compose exec springfield-server python manage.py collectstatic --noinput`.
9. Open http://localhost:8080/dashboard/ to check the dashboard.
10. Optionally create an admin user with `docker compose exec springfield-server python manage.py createsuperuser`. Follow upstream instructions to enable 2FA before using the admin dashboard.

## Saves

The `data`, `media`, `static` and `dlc` folders live outside the container. Keep backups of `data` and `media` before changing server versions or attempting client migrations. The `dlc` directory is initially empty. Include only content you are authorised to host.

## Limitations

This runs the **server only**, not the Android game. An authorised compatible Android client must be configured separately. It does not implement offline play.

This configuration binds port 8080 to localhost only. It is for testing on the Mac, not internet deployment. For remote devices, configure appropriate networking, HTTPS, credentials and backups rather than exposing this development setup.

If permissions or migrations fail, consult the [upstream setup guide](https://github.com/al1sant0s/springfield).
