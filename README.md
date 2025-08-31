# E-commerce Product API

## Features

- Products and Categories (CRUD)
- Search by product name/description and category name
- Ordering by price or created date
- Auth: Session and Token (read-only for anonymous users; write requires login)
- Pagination (page size 10)

## Quickstart

```bash
python -m venv venv
# Windows (PowerShell):
venv\Scripts\Activate.ps1
# or Git Bash:
source venv/Scripts/activate

pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Open http://127.0.0.1:8000/api/ in your browser.

## API Examples

- `GET /api/products/?search=phone`
- `GET /api/products/?ordering=price` or `?ordering=-price`
- `POST /api/categories/` `{ "name": "Electronics", "slug": "electronics" }`
- `POST /api/products/` with `category_id`

## Project Structure

- `ecommerce_api/` — project (settings, urls, wsgi/asgi)
- `products/` — app with models, serializers, viewsets, and router
- `users/` — placeholder (using Django's auth)

## Environment

SQLite by default. Override with env vars: `DB_ENGINE, DB_NAME, DB_USER, DB_PASSWORD, DB_HOST, DB_PORT`.
