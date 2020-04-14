
1. Clone this repo
2. Go to repo root
3. Initialize:
    sudo docker-compose -f docker-compose-setup.yml run webinit django-admin startproject my_project .
4. To use postgres, change database section in my_project/settings.py to:
    DATABASES = {
        'default': {
            'ENGINE': 'django.db.backends.postgresql',
            'NAME': 'postgres',
            'USER': 'postgres',
            'PASSWORD': 'password',
            'HOST': 'db',
            'PORT': 5432,
        }
    }
5. Start:
    docker-compose up
6. http://localhost:8000/