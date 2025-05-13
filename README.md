# Little Lemon Restaurant Django Project

This is a Django-based web application for **Little Lemon**, a family-owned Mediterranean restaurant. The application allows users to view the restaurant's menu, book a table, and learn more about the restaurant.

## Features

- **Home Page**: Overview of the restaurant and its offerings.
- **About Page**: Restaurant history and owners.
- **Menu Page**: List of all menu items with details.
- **Booking Page**: Table booking form.

## Project Structure
```
littlelemon/
├── db.sqlite3                  # SQLite database file
├── manage.py                   # Django management script
├── littlelemon/                # Main Django project folder
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py             # Project settings
│   ├── urls.py                 # Project-level URL configurations
│   ├── wsgi.py
│   └── __pycache__/
│
├── restaurant/                 # Restaurant app folder
│   ├── __init__.py
│   ├── admin.py                # Admin configurations
│   ├── apps.py                 # App configurations
│   ├── forms.py                # Form definitions
│   ├── models.py               # Database models
│   ├── tests.py                # Unit tests
│   ├── urls.py                 # App-level URL configurations
│   ├── views.py                # View functions
│   ├── migrations/             # Database migrations
│   ├── static/                 # Static files (CSS, JS, images)
│   └── templates/              # HTML templates
│       ├── base.html           # Base template
│       ├── index.html          # Home page template
│       ├── about.html          # About page template
│       ├── menu.html           # Menu page template
│       ├── menu_item.html      # Menu item details template
│       └── book.html           # Booking page template
```

## Models

### Booking
- `first_name`
- `last_name`
- `guest_number`
- `comment`

### Menu
- `name`
- `price`
- `description`

## Views

- `home(request)` → `index.html`
- `about(request)` → `about.html`
- `menu(request)` → `menu.html`
- `display_menu_item(request, pk)` → `menu_item.html`
- `book(request)` → `book.html`

## Templates

- `base.html`
- `index.html`
- `about.html`
- `menu.html`
- `menu_item.html`
- `book.html`

## Static Files

Located in:  
`restaurant/static/`  
Main CSS file:  
`style.css`

## Database

Uses SQLite. Models:
- Booking
- Menu

## How to Run the Project

```bash
# Clone the repository
git clone <repository-url>
cd littlelemon

# Install dependencies
pip install -r requirements.txt

# Apply migrations
python manage.py migrate

# Run the development server
python manage.py runserver
```

Open your browser at:
http://127.0.0.1:8000/

## URL Patterns
```
/                  → Home page
/about/            → About page
/menu/             → Menu page
/menu_item/<pk>/   → Menu item detail
/book/             → Booking form
```
