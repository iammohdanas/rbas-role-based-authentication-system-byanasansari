# Django RBAC Authentication System

A complete open-source Django Role-Based Access Control (RBAC) Authentication System built using Django Templates, Bootstrap, HTML, CSS, and JavaScript.

This module provides:

* Authentication System
* Role & Permission Management
* Reusable Frontend Templates
* Dashboard UI
* Protected Routes
* User Management
* Modular App Structure

The project is designed in a plug-and-play manner so it can easily be integrated into any existing Django project.

---

# Features

* Django Authentication
* Role-Based Access Control (RBAC)
* User & Permission Management
* Bootstrap-based Responsive UI
* Django Template Engine Support
* Easy Integration
* Modular Structure
* Production-Friendly

---

# Installation Guide

## Step 1 — Clone the Repository

```bash
git clone https://github.com/your-username/your-repository-name.git
```

---

## Step 2 — Copy the Authenticator App

Copy the authenticator app folder into your existing Django project.

Example:

```bash
your_project/
│
├── authenticator/
├── manage.py
└── your_project/
```

---

## Step 3 — Add App to INSTALLED_APPS

Open:

```python
settings.py
```

Add the app:

```python
INSTALLED_APPS = [
    ...
    'authenticator',
]
```

---

## Step 4 — Include URLs

Open your main:

```python
urls.py
```

Add:

```python
from django.urls import path, include

urlpatterns = [
    path('', include('authenticator.urls')),
]
```

---

## Step 5 — Configure Templates Directory

Update template settings in:

```python
settings.py
```

Example:

```python
TEMPLATES = [
    {
        'DIRS': [BASE_DIR / 'templates'],
    },
]
```

---

## Step 6 — Configure Static Files

Update static configuration:

```python
STATIC_URL = 'static/'

STATICFILES_DIRS = [
    BASE_DIR / "static",
]
```

---

## Step 7 — Update Static Paths in Templates

Update static paths inside HTML templates.

Example:

Before:

```html
<link rel="stylesheet" href="css/style.css">
```

After:

```html
{% load static %}

<link rel="stylesheet" href="{% static 'css/style.css' %}">
```

Similarly update:

* CSS
* JS
* Images
* Icons

---

# Step 8 — Run Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

# Step 9 — Create Superuser

```bash
python manage.py createsuperuser
```

---

# Step 10 — Run the Server

```bash
python manage.py runserver
```

---

# Default Tech Stack

* Python
* Django
* Bootstrap 5
* HTML/CSS
* JavaScript
* Jinja/Django Templates

---

# Integration Notes

* The project is built using reusable Django apps.
* APIs and frontend are separated for future React/Vue migration.
* You can customize roles, permissions, and layouts as needed.
* Designed for ERP, Fintech, HRMS, CRM, and Enterprise Applications.

---

# Contribution

Contributions are welcome.

Feel free to:

* Fork the repository
* Create new features
* Improve UI/UX
* Optimize code
* Raise issues

---

## Author

Mohd Anas Ansari 
https://www.linkedin.com/in/iamanasansari/
https://iamanasansari.space/

## License

This project is licensed under the MIT License.
