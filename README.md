# Django-User-Account
Simple Django App to demo user account creation, login &amp; logout operations.

# Step 1 - Create python virtual environment
    python3 -m venv venv
    source venv/bin/activate

# Step 2 - Install Django package
    pip install django

# Step 3 - Create Django project
    django-admin startproject DjangoUserAccount

# Step 4 - Create Django App for account management
    django-admin startapp accounts

    Make entry for accounts aoo in the INSTALLED_APPS list of settings.py

    ** NOTE **

    *********************************************** IMPORTANT ******************************************
    Make sure you make this entry is before the 'django.contrib.admin' to avoid conflict in paths later.
    ****************************************************************************************************


# Step 5 - Create urls file and make entries for the accounts app.
    Create urls.py under accounts folder.
    Make entry of this urls file in the DjangoUserAccount project's urls.py file.

        `path('',include("accounts.urls")),`

    We will also add an extra entry in the DjangoUserAccount/urls.py to point to 
    Django auth urls provided by Django contrib's auth library.

        `path('accounts/',include('django.contrib.auth.urls'))`

# Step 6 - Create views for the created accounts app.

# Step 7 - Update accounts/urls.py to use newly created views.

# Step 8 - Create required authentication HTML template files

# Step 9 - Make an entry in settings.py to redirect to home upon login
    `LOGIN_REDIRECT_URL = 'home'`

# Step 10 - Migrate default database entries and run the app
    python3 manage.py migrate
    python3 manage.py runserver

## You can now register login or logout using the following paths:

### SignUp
    http://localhost/accounts/signup

### Login
    http://localhost/accounts/login

### Logout:
    http://localhost/accounts/logout