# Create the project directory
mkdir tutorial
cd tutorial

# Create a virtual environment to isolate our package dependencies locally
pipenv install
pipenv shell 


# Set up a new project with a single application
django-admin startproject tutorial .  # Note the trailing '.' character
cd tutorial
django-admin startapp quickstart
cd ..

python manage.py migrate

python manage.py createsuperuser --email admin@example.com --username admin

python manage.py runserver