# E-Commerce API

A secure RESTful backend for an online store, built with Django and Django REST Framework (DRF).

## Features

The project is split into focused Django apps:

- **users** - account registration and authentication
- **products** - product catalog and product management
- **cart** - shopping cart for each user
- **orders** - order creation and order history
- **payments** - payment handling for orders
- **config** - project settings and URL configuration

## Tech stack

- Python 3
- Django
- Django REST Framework
- SQLite (development) / PostgreSQL (production)

## Getting started

### 1. Clone the repository

```bash
git clone https://github.com/donfitex/ecommerce_api.git
cd ecommerce_api
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run migrations and start the server

```bash
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

The API runs at `http://127.0.0.1:8000/`.

## API endpoints

| Method | Endpoint | Description |
| --- | --- | --- |
| POST | `/api/users/register/` | Create an account |
| GET | `/api/products/` | List products |
| GET | `/api/cart/` | View the current cart |
| POST | `/api/orders/` | Place an order |

> Replace these example routes with your real ones from `config/urls.py`.

## Running tests

```bash
python manage.py test
```

## Project structure

```
ecommerce_api/
├── cart/
├── config/
├── orders/
├── payments/
├── products/
├── users/
├── manage.py
└── README.md
```

## License

Released under the Apache-2.0 license.
