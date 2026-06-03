# Frameworks

## Description

Framework notes for Laravel and future full stack application frameworks, including local setup, Docker workflows, environment files, queues, caches, and migrations.

## Common Commands

```bash
php artisan --version
php artisan serve
php artisan migrate
php artisan route:list
composer install
npm install
npm run dev
```

## Examples

Start a Laravel Docker Compose stack:

```bash
docker compose up -d
```

Stop a Laravel Docker Compose stack:

```bash
docker compose down
```

## Troubleshooting

- Laravel cannot connect to database: verify `.env` values and container hostnames.
- Composer install fails: check PHP version and required extensions.
- Frontend assets fail to build: delete `node_modules`, reinstall dependencies, and verify Node.js version.

## References

- [Laravel Documentation](https://laravel.com/docs)
- [Composer Documentation](https://getcomposer.org/doc/)
