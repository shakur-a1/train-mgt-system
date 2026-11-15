# train-mgt-system
# Train Reservation System

A Django web application for managing train services and their operational records. The dashboard summarizes live data from the database, and staff can manage trains, schedules, routes, stations, passengers, reservations, and payments.

## Features

- User sign-up, username-based login, and logout
- Dashboard with live database summaries
- Create, view, edit, and delete records for trains, schedules, routes, stations, passengers, reservations, and payments
- Popup forms for adding, editing, and deleting records
- Passenger names stored as separate first and last names
- Reservation and payment forms connected to saved passengers and services
- Django admin for managing application records
- SQLite database for local development

## Requirements

- Python 3.9 or later
- Django 4.2.30
- django-crispy-forms 2.5
- crispy-bootstrap5 2026.3

## Run locally

Open a terminal in the project directory, where `manage.py` is located.

1. Create and activate a virtual environment:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

   On Windows, activate it with:

   ```powershell
   .venv\Scripts\activate
   ```

2. Install the Python packages:

   ```bash
   python -m pip install "Django==4.2.30" "django-crispy-forms==2.5" "crispy-bootstrap5==2026.3"
   ```

3. Apply database migrations:

   ```bash
   python manage.py migrate
   ```

4. Create an administrator account for `/admin/`:

   ```bash
   python manage.py createsuperuser
   ```

5. Start the development server:

   ```bash
   python manage.py runserver
   ```

Open <http://127.0.0.1:8000/>. Create a system account using the sign-up page, then log in. The Django admin is at <http://127.0.0.1:8000/admin/>.

## Main pages

| Page | URL |
| --- | --- |
| Dashboard | `/` |
| Trains | `/train/` |
| Schedules | `/schedule/` |
| Routes | `/route/` |
| Stations | `/station/` |
| Reservations | `/reservation/` |
| Passengers | `/passenger/` |
| Payments | `/payment/` |
| Sign up | `/register/add/` |
| Login | `/login/` |
| Django admin | `/admin/` |

Most data pages require a signed-in system account. The development database is `db.sqlite3` in the project directory. Static CSS, JavaScript, icons, and dashboard assets are under `traine/static/`.

## Project layout

```text
manage.py
train/                  Django project settings and URL configuration
traine/                 Application models, forms, views, and admin setup
traine/migrations/      Database schema and data migrations
traine/templates/       Page templates
traine/static/          CSS, JavaScript, and theme assets
db.sqlite3              Local development database
```

## Useful commands

```bash
python manage.py check
python manage.py makemigrations
python manage.py migrate
```
